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

1. The HTML Living Standard now allows the inclusion of a `<hr>` element within a `<select>` element; as of October 30, 2023, Chrome 119 and Safari 17 support this, but both have accessibility issues. This is fine for decorative delimiters, but be careful if you are using meaningful delimiters.

- Chrome 119+.
  - Not showing up in the accessibility tree.
  - Not being read out loud in JAWS or TalkBack.
- Safari 17+
  - Not displayed in the accessibility tree.
  - Cannot be read out loud with VoiceOver.

### For Reference

- [Allow <hr> to add a separator line within <select>! - X(Twitter)](https://x.com/takamosoo/status/1710108534023823649)
- [4.10.7 The select element - HTML Living Standard](https://html.spec.whatwg.org/multipage/form-elements.html#the-select-element)
- [Splitting within Selects — Adrian Roselli](https://adrianroselli.com/2023/10/splitting-within-selects.html)

### Compatibility

- [Select element: now with horizontal rules - Chrome for Developers](https://developer.chrome.com/blog/hr-in-select)
- [Safari 17 Release Notes | Apple Developer Documentation](https://developer.apple.com/documentation/safari-release-notes/safari-17-release-notes#New-Features)
