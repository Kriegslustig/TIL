# DOM - addEventListener The Third Argument

`useCapture` is one of the most confusing parts about the DOM API. It's the optional third argument to `addEventListener`. It's used to reverse the order in which an event bubbles.

```html
<main>
  <article>
    <div>Click here for profit!</div>
  </article>
</main>
```

```js
  document.getElementsByTagName('DIV')[0]
    .addEventListener('click', e => console.log('Inner element'))

  document.getElementsByTagName('ARTICLE')[0]
    .addEventListener('click', e => console.log('Outer element'))
```

When `div` is clicked `Inner element\nOuter element` will be logged. If we use `useCapture`:

```js
  document.getElementsByTagName('DIV')[0]
    .addEventListener('click', e => console.log('Inner element'), true)

  document.getElementsByTagName('ARTICLE')[0]
    .addEventListener('click', e => console.log('Outer element'), true)
```

`Outer element\nInner element` will be logged.

