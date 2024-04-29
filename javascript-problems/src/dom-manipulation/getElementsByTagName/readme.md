# getElementsByTagName

## Introduction

`getElementsByTagName()` is a method which exists on the `Document` and `Element` objects and returns an `HTMLCollection` of descendant elements within the `Document`/`Element` given a tag name.

Let's implement our own `Element.getElementsByTagName()` that is similar but slightly different:

- It is a pure function which takes in an element and a tag name string.
- Like `Element.getElementsByTagName()`, only descendants of the specified element are searched, not the element itself.
- Return an array of `Elements`, instead of an `HTMLCollection` of `Element`s.

## Example

```js
const document = new DOMParser().parseFromString(
  `<div id="foo">
    <span>Span</span>
    <p>Paragraph</p>
    <div id="bar">Div</div>
  </div>`,
  'text/html',
);

getElementsByTagName(document.body, 'div');
// [div#foo, div#bar] <-- This is an array of elements.
```

## Resources

[Element.getElementsByTagName() - MDN](https://developer.mozilla.org/en-US/docs/Web/API/Element/getElementsByTagName)