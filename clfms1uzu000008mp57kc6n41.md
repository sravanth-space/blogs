---
title: "React Hooks part 1"
datePublished: Fri Mar 24 2023 16:49:13 GMT+0000 (Coordinated Universal Time)
cuid: clfms1uzu000008mp57kc6n41
slug: react-hooks-part-1
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/YJxAy2p_ZJ4/upload/df78ea86a4af8fd461b939db918db8c1.jpeg
tags: reactjs

---

# useState and useEffect

```javascript
import React from "react";
import { useState, useEffect } from "react";

function WindowSizeList({ url }) {
    const [windowWidth, setWindowWidth] = useState(window.innerWidth)
    const [items, setItems] = useState([])

    const updateWindowWidth = () => {
        setWindowWidth(window.innerWidth)
    }

    useEffect(() => {
        setItems(["abcd"])
    }, [url])

    useEffect(() => {
        console.log('This is my side effect')
        window.addEventListener('resize', updateWindowWidth)
        return () => {
            console.log('This is my clean up')  
            window.removeEventListener('resize', updateWindowWidth)
        }
    }, [])

    return (
        <>
            <div>Window Width: {windowWidth}</div>
            {items.map(item => {
                return <div key={item}>{item}</div>
            })}
        </>
    )
}

export default WindowSizeList
```

The first `useState` hook sets up a state variable called `windowWidth` and initializes it to the current width of the window using the `window.innerWidth` property. The second `useState` hook initializes an empty array called `items`.

The `updateWindowWidth` function is used to update the `windowWidth` state variable whenever the window is resized. This function is called by an event listener attached to the window in the second `useEffect` hook.

The first `useEffect` hook sets the `items` state variable to an array containing a single string "abcd". This effect is only executed when the `url` prop changes.

The second `useEffect` hook is responsible for attaching and removing the event listener for window resizing. The effect function adds an event listener to the `resize` event of the window, and returns a cleanup function that removes the event listener when the component unmounts. The `[]` dependency array passed as the second argument to this `useEffect` hook ensures that the effect is only executed once when the component mounts.

Finally, the component returns a JSX fragment that renders the current window width and a list of items, with each item rendered as a `<div>` element with a unique `key` prop.

Overall, this component demonstrates how the `useState` and `useEffect` hooks can be used to manage state and side effects in a React component. It also shows how to attach and remove event listeners using the `useEffect` hook.

---

# useContext

```javascript
import React from "react"
import { useState, useContext } from "react"
//context
const ThemeContext = React.createContext()

function App() {
    const [theme, setTheme] = useState('dark')

    return (
        // provider with obj with props theme and setTheme
        <ThemeContext.Provider value={{ theme, setTheme }}>
            <ChildComponent />
        </ThemeContext.Provider>
    )
}

function ChildComponent() {
    return <GrandChildComponent />
}

function GrandChildComponent() {
    const { theme, setTheme } = useContext(ThemeContext)

    return (
        <>
            <div>The theme is {theme}</div>
            <button onClick={() => setTheme('light')}>
                Change To Light Theme
            </button>
        </>
    )
}
```

The first step is to create a context object using the createContext() function from the React library. This creates a new context object that can be used to pass data down to child components.

The App component is the parent component and contains the state variable "theme" which is initialized to 'dark' using the useState() hook from the React library. The App component also provides a child component, ChildComponent, with access to the theme state by wrapping it in the ThemeContext.Provider component.

The ChildComponent is a simple component that renders a GrandChildComponent.

The GrandChildComponent uses the useContext() hook from the React library to access the "theme" and "setTheme" variables from the context. It then renders a div that displays the current theme value and a button that changes the theme to "light" when clicked.

Overall, this code shows how to use the React Context API to share state between components without the need for passing props down the component tree. It also demonstrates the power of the useContext() hook to access context values within child components.