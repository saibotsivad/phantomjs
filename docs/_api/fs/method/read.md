---
layout: post
title:  read
section: fs
kind: method
permalink: api/fs/method/read.html
---

'read(string path, string/Object parameters)' (string)

The parameter object can contain :

 - mode: Open Mode. A string made of 'r', 'w', 'a/+', 'b' characters.
 - charset : An IANA, case insensitive, charset name.

Opens the path and returns the entire contents as a string.

When errors occur during a call, it will throw a 'Unable to open file PATH' and hang execution.

Note that the behavior of this method is closely related to [fs.open]({{ site.url }}/api/fs/method/open.html).

## Examples

```javascript
var fs = require('fs');

var content = fs.read('file.txt');
console.log('read data:', content);

phantom.exit();
```


