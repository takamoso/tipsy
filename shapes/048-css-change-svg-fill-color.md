## 048. Change SVG Fill Color

You can freely change the color of the image specified by `url()` in the background.


![](https://github.com/takamoso/tipsy/assets/35029412/8af40600-8ed6-4b45-a4b5-7c886d7b493f)

<p align="center">
  <a href="https://codepen.io/takamoso/pen/vYbGLyQ">CodePen Demo</a>
</p>

```html
<span class="icon"></span>
```
```scss
.icon {
  background-image: linear-gradient(#ffc703, #f42e00);
  mask-image: url('data:image/svg+xml,\
    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512">\
      <path d="M394.23 197.56a300.43 300.43 0 00-53.37-90C301.2 61.65 249.05 32 208 32a16 16 0 00-15.48 20c13.87 53-14.88 97.07-45.31 143.72C122 234.36 96 274.27 96 320c0 88.22 71.78 160 160 160s160-71.78 160-160c0-43.3-7.32-84.49-21.77-122.44zm-105.9 221.13C278 429.69 265.05 432 256 432s-22-2.31-32.33-13.31S208 390.24 208 368c0-25.14 8.82-44.28 17.34-62.78 4.95-10.74 10-21.67 13-33.37a8 8 0 0112.49-4.51A126.48 126.48 0 01275 292c18.17 24 29 52.42 29 76 0 22.24-5.42 39.77-15.67 50.69z"/>\
    </svg>'
  );  // [1]
}
```

1. If you write it as inline SVG on HTML, you can use `fill` or `stroke` attribute to change the color, but the `url()` function is treated as an external resource, so you cannot overwrite it from CSS. You can use the `mask-image` property to crop the image in the form of an icon, and specify the color you want to change in the background color.

### For Reference

- [Change the color of icons specified by inline SVG on background with CSS - X(Twiiter)](https://twitter.com/takamosoo/status/1719178961555767447)

### Compatibility

- [CSS property: mask-image | Can I use... Support tables for HTML5, CSS3, etc](https://caniuse.com/mdn-css_properties_mask-image)
