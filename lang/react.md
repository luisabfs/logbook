## [WARNING] Refs: *Stateless function components cannot have refs*

This means that refs don't work in functional/stateless components. But, we can pass them as **props** if we need this kind of access:

```javascript
function ComponentWithInput({ inputRef }) {
  return <div><input ref={inputRef} /></div>
}

function Parent() {
  return <ComponentWithInput inputRef={input => input && input.scrollIntoView()} /> // or whatever
}
```

It’s breaking encapsulation but it’s pretty much an explicit equivalent of `findDOMNode(this).children[2].firstChild` which is breaking encapsulation in a worse way.
