---
layout: post
title:  absolute
section: fs
kind: method
permalink: api/fs/method/absolute.html
---
'absolute(string)' (string)

Gets the absolute path to where the phantomjs is been run from.
If you use relative addresses then you can get the actual address of directories above and below the phantomjs program.

## Examples

```javascript
var fs = require('fs');

// Print the directory from which phantomjs was run:
var cwd = fs.absolute(".");
console.log(cwd);

// The parent directory:
var parent = fs.absolute("../");
console.log(parent);

// Absolute path of a child directory:
var kid = fs.absolute("/below");
console.log(kid);
```








