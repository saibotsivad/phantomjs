---
layout: post
title:  exists
section: fs
kind: method
permalink: api/fs/method/exists.html
---

'exists(string)' (BOOL)

This will return true if the file exists, otherwise it will return false. This follows symlinks to determinate if a file exists.

## Examples

```javascript
var fs = require('fs');

var path = 'output.txt';

if (!fs.exists(path))
  fs.write(path, 'Hello World', 'w');

phantom.exit();
```

```javascript
var fs = require('fs');

var path = '/Full/Path/To/test.txt';

if (fs.exists(path))
  console.log('"'+path+'" exists.');
else
  console.log('"'+path+'" doesn\'t exist.');

phantom.exit();
```








