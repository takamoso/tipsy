## 019. Override Form Attribute

Attributes of the `<form>` element can be overridden individually by child elements `<input>` and `<button>`.

<p align="center">
  <a href="https://codepen.io/takamoso/pen/yLQqdgM">CodePen Demo</a>
</p>

```ejs
<form
  method="get"
  action="/initial-endpoint"
  target="_blank"
  enctype="multipart/form-data">
  <label>
    メールアドレス
    <input type="email" name="email" required>
  </label>
  <label>
    パスワード
    <input type="password" name="password" required>
  </label>
  <button
    name="submit"
    formmethod="post"                                <%# [1] %>
    formaction="/other-endpoint"                     <%# [1] %>
    formtarget="_self"                               <%# [1] %>
    formenctype="application/x-www-form-urlencoded"  <%# [1] %>
    >登録する</button>
  <button
    name="save"
    formmethod="post"                                <%# [1] %>
    formaction="/other-endpoint"                     <%# [1] %>
    formtarget="_self"                               <%# [1] %>
    formenctype="application/x-www-form-urlencoded"  <%# [1] %>
    formnovalidate>入力内容を保存する</button>
</form>
```

1. For example, in a registration form, the `required` attribute is specified for the email address and password because they are required fields, but for a button to save the input, the `required` attribute should be ignored and the button should be saved regardless of whether or not the input is entered. Therefore, you can specify the `formnovalidate` attribute on the button to save the input so that only this button will not be validated.  
The corresponding attributes are as follows.

| `<form>` Attribute | Corresponding Attribute |
| ---- | ---- |
| `method` | `formmethod` |
| `action` | `formaction` |
| `target` | `formtarget` |
| `enctype` | `formenctype` |

### For Reference

- [Override <form> element attributes with <input> or <button> elements - X(Twitter)](https://x.com/takamosoo/status/1683394515997196288)
