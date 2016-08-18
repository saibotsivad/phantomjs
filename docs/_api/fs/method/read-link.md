---
layout: post
title:  readLink
section: fs
kind: method
permalink: api/fs/method/read-link.html
---

'readLink(string)' (string)

This will return the absolute path of a file or folder pointed by a symlink (or shortcut on Windows). If the path is not an symlink or shortcut, it will return an empty string.

## Examples

```javascript
var fs = require('fs');

var path = '/Full/Path/To/test.txt';

if (fs.isLink(path)) {
  var absolute = fs.readLink(path);
  console.log('The absolute path of "'+path+'" is "'+absolute+'"');
}
else
  console.log('"'+path+'" is an absolute path');

phantom.exit();
```








