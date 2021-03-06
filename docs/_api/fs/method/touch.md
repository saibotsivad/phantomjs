---
layout: post
title:  touch
section: fs
kind: method
permalink: api/fs/method/touch.html
---

'touch(string)'

This will try to create an empty file at the specified path.

When errors occur during a call, it will throw a 'Unable to open file PATH' and hang execution. The call **won't** throw an error if the file already exists.

Note that the behavior of this method is closely related to [fs.open]({{ site.url }}/api/fs/method/open.html) and [Stream.write]({{ site.url }}/api/stream/method/write.html).

## Examples

```javascript
var fs = require('fs');
var path = 'test.txt';

// Creates an empty file
fs.touch(path);

var text = fs.read(path);

// If the test.txt didn't already exist, this will print an empty string
console.log(text);

phantom.exit();
```








