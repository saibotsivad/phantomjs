---
layout: post
title:  move
section: fs
kind: method
permalink: api/fs/method/move.html
---

'move(string source, string destination)'

This will try to move a file from one path to another.

Parameter 1 is the source file and parameter 2 is the destination path with the file name.

If the source file can't be found then it will throw a 'Unable to copy file SOURCE at DESTINATION' and hang execution.

If the destination can not be created then it will throw a 'Unable to copy file SOURCE at DESTINATION' and hang execution. It will not overwrite existing files.

If the source file can not be deleted then it will throw a 'Unable to delete file SOURCE' and hang execution.

## Examples

```javascript
var fs = require('fs');
fs.move("A.txt", "folder/A.txt");
```








