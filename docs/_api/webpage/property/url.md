---
layout: post
title:  url
section: webpage
kind: property
permalink: api/webpage/property/url.html
---

`url` {string}

**Introduced:** PhantomJS 1.7
Read-only. This property gets the current URL of the web page (main frame).

## Examples

```javascript
var webPage = require('webpage');
var page = webPage.create();

page.open('http://phantomjs.org', function (status) {
  var url = page.url;
  console.log('URL: ' + url);
  phantom.exit();
});
```








