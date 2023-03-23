---
title: "JS Mini Challenges Week 1"
datePublished: Thu Mar 23 2023 23:15:25 GMT+0000 (Coordinated Universal Time)
cuid: clflqeob8000609maek8i5z0s
slug: js-mini-challenges-week-1
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/Jxi526YIQgA/upload/7fef2564897bb75e26b81332203a2b55.jpeg
tags: javascript

---

### Guess the outputs without executing the code

```javascript
var foo = function(){
	var args = Array.prototype.slice.call(arguments);
	console.log(args[1])
}
foo(1,2,4) //?
```

```javascript
const obj1 = {
    a: 5,
    b: {
        c: 6
    }
}

const obj2 = Object.assign({}, obj1)
const obj3 = { ...obj1 }
obj1.b.c = 8
console.log(obj2)  //?
console.log(obj3)  //?
console.log(Object.assign({}, obj1, obj2, obj3)) //?
```

```javascript
console.log(null == undefined) //?
console.log(null === undefined) //?
```

```javascript
var power = "100"
function getPowerNumber() {
    var power = "10"
    function f() {
        return power
    }
    return f
}
console.log(getPowerNumber()()) //?
```

```javascript
var obj = { hasOwnProperty: 1, foo: 2 }
console.log(obj.hasOwnProperty('foo')) //?
```

```javascript
function person(id, name) {
    var id = id
    var name = name
}

function student(id, name) {
    person.call(this, id, name)
}

console.log(new student(50, "Sravanth").id);//?
```

```javascript
console.log(Boolean("false") === Boolean(false)); //?
```

```javascript
let foo = (a = 3, b = 5) => {
    console.log(a + b);
}

foo(7, 4) //?
```

```javascript
function foo() {
    console.log(a); //?
    var a = 4;
    console.log(a); //?
}

foo()
```

```javascript
function foo() {
    console.log(a); //?
    let a = 4;
    console.log(a); //?
}

foo()
```