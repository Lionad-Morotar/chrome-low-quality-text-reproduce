# Low text quality when using specific css props

Chromium Bugs Link: [#1471449](https://bugs.chromium.org/p/chromium/issues/detail?id=1471449)

## in short

Combining the use of these CSS styles and enable scrollbar leads to low-quality text rendering: `transform`、`border`、`border-radius`、`border`

```css
.selector {
  transform: translate(1px, 1px);
  border: solid 10px gray;
  border-right: unset;
  border-radius: 1px;
  overflow: hidden auto;
}
```

## how to reproduce

1. open `index.html`
2. open devtools using f12
3. remove `border-radius: 1px` declare on `.dialog`

（my computer screen is HiRes(3200 * 2000 16 inch)）

## screen shots

### normal quality text

![](./quality-normal.png)

### normal quality text

![](./quality-low.png)
