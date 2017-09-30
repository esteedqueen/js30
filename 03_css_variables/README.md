# Day 3
What I learnt:

- using `:root` selector
This selects the highest parent element in the document. In HTML, this is equivalent to the html selector but with a higher [specificity](https://developer.mozilla.org/en-US/docs/Web/CSS/Specificity)

- The syntaxes for setting variables in pure CSS and using the variables.
```
:root{
  --yc-orange: #F26522;
}

.btn{
  color: var(--yc-orange);
}

```

-  You can already set variables in SASS, but I think doing this in pure CSS is pretty cool and CSS variables can be updated in JavaScript.

- `filter` property for bluring.
```
filter: blur(10px);
```

- [NodeList](https://developer.mozilla.org/en/docs/Web/API/NodeList) vs [Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array) in JS (similarities and differences)
When you use `document.querySelectorAll`, the objects returned are a collection of nodes known as a NodeList.
NodeList are not Arrays but they are similar in the sense that they are both a collection of objects. In modern browsers, you can iterate on a NodeList using `forEach` just like you would an array. 

The methods in NodeList are quite limited so developers usually convert a NodeList to an Array for access to Array methods for manipulating the collection of objects.

- `mousemove` event

- `HTMLElement.dataset`
[HTMLElement.dataset](https://developer.mozilla.org/en/docs/Web/API/HTMLElement/dataset) returns all the custom data attributes in the referenced element as accessible objects
