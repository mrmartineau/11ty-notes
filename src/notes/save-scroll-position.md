---
title: Save sidebar scroll position
tags:
  - javascript
link: 'https://twitter.com/hakimel/status/1262337514741706752'
date: git Last Modified
---

```ts
let sidebar = document.querySelector('.sidebar')

let top = sessionStorage.getItem('sidebar-scroll')

if (top !== null) {
  sidebar.scrollTop = parseInt(top, 10)
}

window.addEventListener('beforeunload', () => {
  sessionStorage.setItem('sidebar-scroll', sidebar.scrollTop)
})
```
