## 045. Sticky Footer

When there is little content on the page, the footer is fixed at the bottom of the browser; when there is enough content, it is pushed straight to the bottom.

https://github.com/takamoso/tipsy/assets/35029412/2d9d833f-d31e-4f12-94c0-3a6f264004a7

<p align="center">
  <a href="https://codepen.io/takamoso/pen/ZEwYzjO">CodePen Demo</a>
</p>

```html
<!doctype html>
<html>
<body>
  ...
  <footer class="footer">...</footer>
</body>
</html>
```
```scss
body {
  min-height: 100dvh;  // [1]
}
.footer {
  position: sticky;        // [2]
  top: 100%;               // [2]
  will-change: transform;  // [3]
}
```

1. Make `body` at least the full height of the browser to anchor `.footer` to the bottom.

2. Use `position: sticky;` to fix it at `100%` of the full browser height from the top of the screen.

  > **CSS Positioned Layout Module Level 3 - 3.4. Sticky positioning**
  > For each side of the box, if the corresponding inset property is not auto, and the corresponding border edge of the box would be outside the corresponding edge of the sticky view rectangle, then the box must be visually shifted (as for relative positioning) to be inward of that sticky view rectangle edge, insofar as it can while its position box remains contained within its containing block.

3. Currently MacOS Chrome 118 renders a gap of `0.5px` under the footer as shown below. So, if you specify `will-change: transform;` it will be rendered correctly with GPU acceleration and stacking context.

  ![](https://github.com/takamoso/tipsy/assets/35029412/3ca30363-5c50-48af-b92e-88e91b568fb1)

### Compatibility

- [Small, Large, and Dynamic viewport units | Can I use... Support tables for HTML5, CSS3, etc](https://caniuse.com/viewport-unit-variants)
- [CSS position:sticky | Can I use... Support tables for HTML5, CSS3, etc](https://caniuse.com/css-sticky)
- [CSS will-change property | Can I use... Support tables for HTML5, CSS3, etc](https://caniuse.com/will-change)
