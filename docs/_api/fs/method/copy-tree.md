---
layout: post
title:  copyTree
section: fs
kind: method
permalink: api/fs/method/copy-tree.html
---

'copyTree(string source, string destination)'

This will try to copy a directory tree from one path to another.

Parameter 1 is the source folder tree and parameter 2 is the destination path.

If the destination folder doesn't exist, it will be created. Then, every file and folder will be copied in the destination folder.
Folders will be recursively copied.

If one of the files or folders fails to be copied or created, it will throw a 'Unable to copy directory tree SOURCE at DESTINATION' and hang execution.

## Examples

```javascript
var fs = require('fs');

fs.copyTree("sourceFolder/", "destinationFolder/");

phantom.exit();
```








