---
layout: post
title:  readLine
section: stream
kind: method
permalink: api/stream/method/read-line.html
---

## Stream objects

Stream objects are returned from the [fs.open]({{ site.url }}/api/fs/method/open.html) method.

## Examples

```javascript
var fs = require('fs');
var stream = fs.open('data.xml', 'r');

while(!stream.atEnd()) {
    var line = stream.readLine();
    console.log(line);
}

stream.close();
```








