## 031. Search Element

A `<search>` element has been added to replace `<div role="search">`.

```html
<search role="search">  <!-- [1] -->
  <form>
    <label for="query">サイト内検索</label>
    <input id="query" type="search" name="q">
    <button>検索</button>
  </form>
</search>
```

1. It is mainly used for site search and refinement. Since there are few [supported browsers](https://caniuse.com/mdn-html_elements_search) at this time, `role="search"` should also be written as before.


```html
<search role="search">  <!-- [2] -->
  <label>
    商品検索
    <input type="search">
  </label>
  <label>
    <input type="checkbox">
    完全一致のみ
  </label>
  <section>
    <h3>検索結果</h3>
    <ul>
      <li>...</li>
      <li>...</li>
      <li>...</li>
      ...
    </ul>
    <output>検索結果がありません。</output>
  </section>
</search>
```

2. In a search screen of a web application that does not use the `<form>` element, enclosing the entire element with the `<search>` element means that the contents of the descendants will have search capabilities.

```html
<!doctype html>
<html>
<body>
  <header>
    ...
    <search>...</search>  <!-- [3] -->
  </header>
  <main>
    ...
    <search>...</search>  <!-- [3] -->
  </main>
</body>
</html>
```

3. Of course, you can have multiple `<search>` elements on a single web page. The `<search>` element in a `<header>` element means a search function for the whole web site, and the `<search>` element in a `<main>` element means a narrow search function within the web page.
