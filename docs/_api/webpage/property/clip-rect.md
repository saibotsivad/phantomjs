---
layout: post
title:  clipRect
section: webpage
kind: property
permalink: api/webpage/property/clip-rect.html
---

`clipRect` {object}

This property defines the rectangular area of the web page to be rasterized when `page.render` is invoked. If no clipping rectangle is set, `page.render` will process the entire web page.

## Examples

```javascript
var webPage = require('webpage');
var page = webPage.create();

page.clipRect = {
  top: 14,
  left: 3,
  width: 400,
  height: 300
};
```








