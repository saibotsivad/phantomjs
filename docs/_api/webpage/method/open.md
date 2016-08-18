---
layout: post
title:  open
section: webpage
kind: method
permalink: api/webpage/method/open.html
---

`open(url, callback)` {void}
`open(url, method, callback)` {void}
`open(url, method, data, callback)` {void}
`open(url, settings, callback)` {void}

Opens the `url` and loads it to the page. Once the page is loaded, the optional `callback` is called using `page.onLoadFinished`, and also provides the page status to the function (`'success'` or `'fail'`).

## Examples

### GET google.com and report "success" or "fail"

```javascript
var webPage = require('webpage');
var page = webPage.create();

page.open('http://www.google.com/', function(status) {
  console.log('Status: ' + status);
  // Do other things here...
});
```

### POST data to google.com and report "success" or "fail"

As of PhantomJS 1.2, the open function can be used to request a URL with methods other than GET. This syntax also includes the ability to specify data to be sent with the request. In the following example, we make a request using the POST method, and include some basic data.

```javascript
var webPage = require('webpage');
var page = webPage.create();
var postBody = 'user=username&password=password';

page.open('http://www.google.com/', 'POST', postBody, function(status) {
  console.log('Status: ' + status);
  // Do other things here...
});
```

### POST json data to your.custom.api in utf-8 encoding
As of PhantomJS 1.9, the open function can get an object of settings. and with a use of "encoding" key, you can set the custom encoding to your app.
In this example, we've set the encoding to `UTF8`, and set the `Content-Type` header to `application/json` for making our server know the request has information in `json` format and not in `urlencoded` format.

```javascript
var webPage = require('webpage');
var page = webPage.create();
var settings = {
  operation: "POST",
  encoding: "utf8",
  headers: {
    "Content-Type": "application/json"
  },
  data: JSON.stringify({
    some: "data",
    another: ["custom", "data"]
  })
};

page.open('http://your.custom.api', settings, function(status) {
  console.log('Status: ' + status);
  // Do other things here...
});
```






