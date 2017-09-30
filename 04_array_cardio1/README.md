# Day 4
What I learnt:

## `filter()`

_[Array.prototype.filter()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter)_ is a method used on an array that creates a new array which matches the value of the function passed into it.

## `console.table()`

-[console.table()](https://developer.mozilla.org/en-US/docs/Web/API/Console/table)- displays data such as arrays and objects as a table in the console. This could greatly help with debugging and visualisation of objects and arrays.

I didn't know about this before today, so *mindblown! 

## `map`
_[Array.prototype.map()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map)_ is a method used on an array that creates a new array with the results of calling the provided function on each element of the array.

## `sort`
_[Array.prototype.sort()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/sort)_ is a method used on an array that sorts the array in place with the provided function.

syntax:
`arr.sort()` - this sorts by unicode code point order
or
`arr.sort(compareFunc)` - this sorts by compareFunc

## _conditional (ternary) operator_
A conditional operator usually used as a shortcut for if statement. It takes 3 operand.

syntax:
`condition ? exp1 : exp2` 

Interesting to note that javascript ternery operator syntax is quite similar to ruby's

## `reduce`
_[Array.prototype.reduce()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/reduce?v=b)_ is a method that applies a function against and accumulator and each item of an array from left to right to reduce it to a single value

syntax:
`arr.reduce(callback[, initialValue])`

```
arr.reduce(function(accumulator, currentValue){
  ...
}, initialValue)
```

## Converting a NodeList to an Array
- using `Array.from(nodeList)`
- using ES6 spreads `[...nodeList]`

