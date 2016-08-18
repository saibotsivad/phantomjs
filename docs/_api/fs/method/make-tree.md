---
layout: post
title:  makeTree
section: fs
kind: method
permalink: api/fs/method/make-tree.html
---

'makeTree(string)' (BOOL)

Creates all necessary directories to be able to create the directory.

This will returns true if the creation was successful, otherwise false. If the directory already exists, it will returns true.

## Examples

```javascript
var fs = require('fs');

var path = '/Full/Path/To/Test/';

if(fs.makeDirectory(test))
  console.log('"'+path+'" was created.');
else
  console.log('"'+path+'" is NOT created.');

phantom.exit();
```








