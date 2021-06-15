# Bulma-Addons
## Some addons for Bulma
Bulma is a wonderful CSS library. Even though it's very extense, you could need some JS in order to enjoy it.
Here I will put a small collection of some useful ones.

## bulma-panel.js
It contains a simple solution to sort by JS the panel-blocks clicking panel-tabs (function _panelDigger_).

```
CSS classes of a basic panel

panel
├── panel-tabs
│   ├── panel-tab
│   ├── panel-tab
│   ┊
│   └── panel-tab
├── panel-block
├── panel-block
┊
└── panel-block
```

1. Add `onclick="panelDigger([label])"` to `panel-tab`-classed elements, chosing a unique replacement for `[label]`; i.e.: `<a class="panel-tab">e-books</a>` will become `<a class="panel-tab" onclick="panelDigger(ebook);">e-books</a>`.
2. Add both `panel-tab`s and `panel-block`s a new class `panel-[label]` choosing the fitting `[label]` replacement according to the `panel-tab` it is depending from; i.e.: 
```html5
<p class="panel-tabs">
  <a class="panel-tab panel-ebook" onclick="panelDigger('ebook')">e-books</a>
</p>
<a class="panel-block panel-ebook">Kobo</a>
```
4. Add `bulma-panel.js` to your page, i.e.: `<script src="path/to/myScript.js"></script>`
5. Bonus-track 1: if you want to show a `panel-block` in more categories, just add new `panel-[label]` classes to `panel-block` element. I.E.: `<a class="panel-block panel-ebook panel-hardware panel-linux panel-eink">Kobo</a>`
6. Bonus-track 2: if you want to reset the panel, simply add a `panelDigger(reset)` and `panel-reset` to a `panel-tab` and a `panel-reset` to each `panel-block` you want to show on a resetted panel.
