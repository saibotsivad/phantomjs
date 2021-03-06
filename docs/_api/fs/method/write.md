---
layout: post
title:  write
section: fs
kind: method
permalink: api/fs/method/write.html
---

'write(string source, string content, string/Object parameters)'

The parameter object can contain :

 - mode: Open Mode. A string made of 'r', 'w', 'a/+', 'b' characters.
 - charset : An IANA, case insensitive, charset name.

 If the source file can't be opened then it will throw a 'Unable to open file SOURCE' and hang execution.

## Examples

```javascript
var fs = require('fs');

var path = 'output.txt';
var content = 'Hello World!';
fs.write(path, content, 'w');

phantom.exit();
```
