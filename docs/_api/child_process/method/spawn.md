---
layout: post
title:  spawn
section: child_process
kind: method
permalink: api/child_process/method/spawn.html
---

## Examples

```javascript
var page  = require('webpage').create();
var spawn = require('child_process').spawn;

page.open('http://google.com', function(status){
  if( status == 'success' ) {
    page.render('/tmp/google-snapshot.jpg');
    spawn('/usr/bin/sensible-browser', 'file:///tmp/google-snapshot.jpg');
  }
  setTimeout(function(){
    phantom.exit();
  },2000);
});

```








