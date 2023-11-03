## 033. Get Input Associated with Label

To get a `<label>` element with `<input>` as a child element, or a `<label>` element linked with the `for` attribute.

```html
<label>
  入れ子のラベル
  <input id="input">
</label>
<label for="input">紐づいたラベル</label>
```
```js
document.querySelector('#input')?.labels  // [1]
// =>
// NodeList(2)
// [
//   <label>
//     入れ子のラベル
//     <input id="input">
//   </label>,
//   <label for="input">紐づいたラベル</label>,
// ]
```

1. If you use the `document.querySelector('#input')?.closest('label')` or `document.querySelector('label[for="#input"]')`, you can use the `labels` property to get `<label >` elements linked as a NodeList.
