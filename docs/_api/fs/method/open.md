---
layout: post
title:  open
section: fs
kind: method
permalink: api/fs/method/open.html
---

'open(string path, string/Object parameters)' ([Stream]({{ site.url }}/api/stream/))

The parameter object can contain :

 - mode: Open Mode. A string made of 'r', 'w', 'a/+', 'b' characters.
 - charset : An IANA, case insensitive, charset name.

[Stream objects]({{ site.url }}/api/stream/) are returned from the [fs.open]({{ site.url }}/api/fs/method/open.html) method. Don't forget to close the stream.

When errors occur during a call, it will throw a 'Unable to open file PATH' and hang execution.

## Examples

```javascript
var fs = require('fs');

var file = fs.open('/path/to/file', 'r'); //Open Mode. A string made of 'r', 'w', 'a/+', 'b' characters.

var otherFile = fs.open('/path/to/otherFile', {
  mode: 'r' //(see Open Mode above)
});

var yetAnotherFile = fs.open('/path/to/yetAnotherFile', {
  mode: 'w', //(see Open Mode above)
  charset: 'US-ASCII' //An IANA, case insensitive, charset name.
});

file.close();
otherFile.close();
yetAnotherFile.close();
```








