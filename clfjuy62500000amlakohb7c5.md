---
title: "Things to remember about JavaScript ForEach Loop"
datePublished: Wed Mar 22 2023 15:47:01 GMT+0000 (Coordinated Universal Time)
cuid: clfjuy62500000amlakohb7c5
slug: things-to-remember-about-javascript-foreach-loop
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/u2d0BPZFXOY/upload/ea81e9d75f0e3a8c82c4828084090043.jpeg
tags: javascript

---

**Can’t Skip an Iteration with "Continue"**

```javascript
const arr = [1, 2, 3, 4, 5, 6, 7]

arr.forEach((val) => {
    if (val === 3) {
        continue;
    }
    console.log("current: ", val)
}
)
// SyntaxError: Unsyntactic continue
```

**Can’t End A Loop Early with "Break"**

```javascript
const arr = [1, 2, 3, 4, 5, 6, 7]

arr.forEach((val) => {
    if (val === 3) {
        break;
    }
    console.log("current: ", val)
}
)
// SyntaxError: Unsyntactic break 
```

**Always Returns "Undefined"**

```javascript
const arr = [1, 2, 3, 4, 5, 6, 7]

arr.forEach((val) => {
    if (val === 3) {
        return val;
    }
}
)
//Undefined
```