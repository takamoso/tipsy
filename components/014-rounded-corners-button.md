## 014. Rounded Corners Button

Conventionally, large values such as `9999px` were used to create rounded corner buttons.

![](https://github.com/takamoso/tipsy/assets/35029412/71be12d6-459f-4988-b41f-6091ec2ac60e)

<p align="center">
  <a href="https://codepen.io/takamoso/pen/ZEqGKgY">CodePen Demo</a>
</p>

```html
<a class="button" href="#">ボタン</a>
```
```scss
.button {
  border-radius: calc(infinity * 1px);  // [1]
}
```

1. `calc(infinity * 1px)` can be used instead of `9999px`. By the way, you can also write `calc(1px / 0)`, since the calculated value in `calc()` should be `infinity`.
  Other numerical constants that were added are as follows.

- Euler's Number `e`
- Pi `pi`
- Positive Infinity `infinity`
- Negative Infinity `-infinity`
- Not a Number `NaN`

### For Reference

- [CSS Values and Units Module Level 4 - 10.7. Numeric Constants](https://www.w3.org/TR/css-values-4/#calc-constants)

### Compatibility

- [types: <calc-constant>: e constant | Can I use... Support tables for HTML5, CSS3, etc](https://caniuse.com/mdn-css_types_calc-constant_e)
- [types: <calc-constant>: pi constant | Can I use... Support tables for HTML5, CSS3, etc](https://caniuse.com/mdn-css_types_calc-constant_pi)
- [types: <calc-constant>: infinity & -infinity constants | Can I use... Support tables for HTML5, CSS3, etc](https://caniuse.com/mdn-css_types_calc-constant_infinity)
- [types: <calc-constant>: NaN constant | Can I use... Support tables for HTML5, CSS3, etc](https://caniuse.com/mdn-css_types_calc-constant_nan)
