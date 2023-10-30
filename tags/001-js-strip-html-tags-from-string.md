## 001. Strip HTML Tags from String

Remove all HTML tags in the string.

```js
const string = '<h1>文字列から<strong>HTMLタグ</strong>を除去</h1>'
const html = new DOMParser().parseFromString(string, 'text/html')  // [1]

html.body.textContent  // [2]
// => "文字列からHTMLタグを除去"
```

1. Parses a string as DOM and returns an HTMLDocument (document root element).
1. Get only text in the `textContent` property of the `body` element.

### Compatibility

- [DOMParser API: parseFromString: HTML (text/html) support | Can I use... Support tables for HTML5, CSS3, etc](https://caniuse.com/mdn-api_domparser_parsefromstring_html)
