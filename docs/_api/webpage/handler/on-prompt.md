---
layout: post
title:  onPrompt
section: webpage
kind: handler
permalink: api/webpage/handler/on-prompt.html
---

**Introduced:** PhantomJS 1.6

This callback is invoked when there is a JavaScript `prompt` on the web page. The arguments passed to the callback are the string for the message (`msg`) and the default value (`defaultVal`) for the prompt answer. The return value of the callback handler should be a string.

## Examples

```javascript
var webPage = require('webpage');
var page = webPage.create();

page.onPrompt = function(msg, defaultVal) {
  if (msg === "What's your name?") {
    return 'PhantomJS';
  }
  return defaultVal;
};
```








