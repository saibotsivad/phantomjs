---
layout: post
title:  cookies
section: webpage
kind: property
permalink: api/webpage/property/cookies.html
---

Get or set Cookies visible to the current URL (though, for setting, use of `page.addCookie` is preferred). This array will be pre-populated by any existing Cookie data visible to this URL that is stored in the CookieJar, if any.

Cookies is an array of objects: 
```javascript
{ 
  domain: 'example.com',
  expires: 'Sat Oct 11 2014 21:44:33 GMT+0200 (CEST)',
  expiry: 1476128618,
  httponly: false,
  name: 'cookieName',
  path: '/',
  secure: false,
  value: cookieValue
}
```

## Examples

```javascript
var webPage = require('webpage');
var page = webPage.create();

page.open('http://phantomjs.org', function (status) {
  var cookies = page.cookies;
  
  console.log('Listing cookies:');
  for(var i in cookies) {
    console.log(cookies[i].name + '=' + cookies[i].value);
  }
  
  phantom.exit();
});

```








