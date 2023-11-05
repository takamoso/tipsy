## 038. Select with Horizontal Rules

The separator lines used in the menu bar of desktop applications can also be expressed on the Web.

![](https://github.com/takamoso/tipsy/assets/35029412/5e8006ef-dabd-48cf-8fcc-ec92d9c762c3)

<p align="center">
  <a href="https://codepen.io/takamoso/pen/xxmQVbg">CodePen Demo</a>
</p>

```html
<select>
  <option>元に戻す</option>
  <option>やり直す</option>
  <hr>  <!-- [1] -->
  <option>切り取り</option>
  <option>コピー</option>
  <option>貼り付け</option>
  <hr>  <!-- [1] -->
  <option>検索</option>
  <option>置換</option>
</select>
```

1. The HTML Living Standard now allows the inclusion of a `<hr>` element within a `<select>` element, Chrome 119 and Safari 17 support this, but both have accessibility issues. This is fine for decorative delimiters, but be careful if you are using meaningful delimiters.

- Chrome / Edge 119+, Opera 105+
  - Not displayed in the accessibility tree.
  - Cannot read out loud with PC-Talker, NVDA, JAWS, or TalkBack.
- Safari 17+
  - Not displayed in the accessibility tree.
  - Cannot read out loud with VoiceOver.
- Firefox
  - Not supported.
- Android Chrome
  - Not supported.
- iOS Safari
  - Not supported.
