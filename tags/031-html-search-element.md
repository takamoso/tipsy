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
