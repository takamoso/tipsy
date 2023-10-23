## 035. Footer Slides Out from the Bottom

Scroll to the bottom of the page, and the footer slides out from under the main content.

https://github.com/takamoso/tipsy/assets/35029412/36712972-4d25-404e-bef4-b2cb2008ad85

<p align="center">
  <a href="https://codepen.io/takamoso/pen/BavrgoO">CodePen Demo</a>
</p>

```html
<!doctype html>
<html>
<body>
  <main class="main">...</main>
  <footer class="footer">...</footer>
</body>
</html>
```
```scss
.main {
  position: relative;      // [1]
  min-height: 100dvh;      // [2]
  background-color: #fff;  // [3]
  z-index: 1;              // [1]
}
.footer {
  position: sticky;  // [4]
  top: 0;            // [5]
  left: 0;           // [4]
  bottom: 0;         // [4]
  width: 100%;       // [6]
}
```

1. Display `.main` before `.footer`.
1. Make `.main` at least the full height of the browser to hide `.footer`.
1. Specify a background color of `#fff` since the `.footer` is transparent underneath.
1. Use `position: sticky;` to fix it in the lower left corner.
1. Prevent `.footer` from being hidden under `.main` when `.footer` is larger than the browser height.
1. Fill the `.footer` to the full width of the browser.

### Compatibility

- [Small, Large, and Dynamic viewport units | Can I use... Support tables for HTML5, CSS3, etc](https://caniuse.com/viewport-unit-variants)
- [CSS position:sticky | Can I use... Support tables for HTML5, CSS3, etc](https://caniuse.com/css-sticky)
