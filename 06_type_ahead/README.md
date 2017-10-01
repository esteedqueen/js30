# Day 6
What I learnt:

## Promises in JS
This led me to dig through the rabbit hole on [Promises](https://developers.google.com/web/fundamentals/primers/promises) where I learnt about the history (what, why & several JS libraries with different API implementation of Promises), [terminologies](https://github.com/domenic/promises-unwrapping/blob/master/docs/states-and-fates.md), and the official JS [Promises API references](https://developers.google.com/web/fundamentals/primers/promises#promise-api-reference).

Because JavaScript is single threaded, with Promises, you can write for asynchronous success or/and failure callbacks

### Creating a promise

```
var promise = new Promise(function(resolve, reject) {
  // do a thing, possibly async, then…

  if (/* it works */) {
    resolve("Yay, it worked!");
  }
  else {
    reject(Error("It did not work!"));
  }
});
```

### Using the promise
```
promise.then(function(result) {
  console.log(result); // "Yay, it worked!"
}, function(err) {
  console.log(err); // Error: "It did not work!"
});
```

## `var` vs `let` vs `const` similarities and differences for scoping variables in JS :eyes: smh

###  `var`
- function scoped
- globally scoped wherever it's declared, even in a block, except if in a function
- can be updated
- can be redefined

### `let`
- block scoped
- not globally scoped if in a block
- can be updated
- cannot be redefined

### `const`
- block scoped
- not globally scoped if in a block
- can be updated
- can not be redefined
- is not immutable. i.e. you can update its properties

From the above, you can tell that this can get pretty confusing real quick.

Maybe I'm missing something here but tbh, I'll propose that what is required is a `var` that is both function and block scoped. 

What I mean by this is - it's scoped in a way that when declared in a function it's available only in the function and when declared in a block it's available only in the block but it doesn't become globally scoped. Additional prototypes can be added to the `var` if we need it to not be redefined.

## `Array.prototype.push(el1, el2, etc.)` and `Array.prototype.push(el1,...[array])`

```
const buttons = [];

buttons.push("go", "next");

const more_buttons = ["back", "help", "forward"];

buttons.push(more_buttons); // ["go", "next", ["back", "help", "forward"]]
buttons.push(...more_buttons); // ["go", "next", "back", "help", "forward"]
```

## `RegExp`

```
new RegExp(pattern, flags)
```

[Reference](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/RegExp)
