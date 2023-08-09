# Low text quality when using specific css props

## in short

use these css props together causing low text quality:

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

## screen shots

### normal quality text

![](./quality-normal.png)

### normal quality text

![](./quality-low.png)