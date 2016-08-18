---
layout: post
title:  size
section: fs
kind: method
permalink: api/fs/method/size.html
---

'size(string)' (int)

This will return the specified file size in bytes, if it exists.

When errors occur during a call, it will throw a 'Unable to read file PATH size' and hang execution.

## Examples

```javascript
var fs = require('fs');
var path = 'someFolder/';

// Go through every element in the folder
fs.list(path).forEach(function(file) {
    file = path + file;
    // Remove every file that are larger than 100 bytes
    if(fs.isFile(file) && fs.size(file) > 100)
        fs.remove(file);
});

phantom.exit();
```








