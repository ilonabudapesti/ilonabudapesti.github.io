---
layout: post
title: Return Statements
published: true
---




There is a set of common mistakes that I see Hack Reactor students make with regards to return statements and I thought it would be helpful to list them out, see what is causing these mistakes and how they could be improved upon/eliminated.

We will look at the following cases in this post.

- return values with true/false
- return values with ternary operators
- return values with assignment operator
- return values with functions that return a value
- return values with callbacks
- return values with closures

### return values with true/false

```javascript
// students often write out true and false cases with explicit if/else statements
if (result > 5) {
  return true;
} else {
  return false;
}

// instead
return result > 5;
```

The confusion or lack of understanding probably stems from the fact that students don't realize that the order of evaluation of the code. Let's look at that.

```js
return result > 5;
```

Whatever is to the **right** of `return` will evaluate first.

```js
result > 5;
```

We have the greatern than operator here which will **return a boolean** implicitly. 

### return values with ternary operators

```javascript

```

### return value with assignment operator

```js
return a = b = 5;
```

An interesting operator to note here is the `=` assignment operator which works right to left and returns the value that was assigned. 

```js
a = b = 5;
b; // 5
a; // 5
```

The assignment works right to left and first assigns the value 5 to `b`. It returns the value 5. Then it will assign 5 to `a`. Thus we can have assignments in return statements too.

Get real good with operators:

- [MDN on Operator Precedence](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Operator_Precedence)

### return values with functions that return a value
```javascript

```

### return values with callbacks
```javascript

```

### return values with closures
```javascript

```
