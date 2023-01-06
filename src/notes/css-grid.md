---
title: CSS Grid
emoji: 🍱
tags:
  - css
created: 2020-02-27T23:02:00.000Z
modified: 2020-04-11T06:27:27.000Z
---

```css
.grid {
  display: grid;
  grid-gap: 30px;
  grid-template-columns: repeat(auto-fill, 112px);
  /* or this */
  grid-template-columns: repeat(auto-fill, minmax(112px, 1fr));
}

/* To select modern Grid browsers and IE 11 */
@supports (display: grid) {
  grid-gap: 20px;
}

/* Else */
@supports not (display: grid) {
  li {
    padding: 10px;
  }
}

/* Edge 16 and higher */
@supports (display: -ms-grid) and (display: grid) {
  div {
    width: auto;
  }
}

/* Edge 15 and lower */
@supports (display: -ms-grid) and (not (display: grid)) {
  div {
    margin: 0;
  }
}

// To select only Grid browsers without IE 11
@supports (grid-gap: 0) {
  grid-gap: 20px;
}
```
