---
layout: post
title:  remove
section: fs
kind: method
permalink: api/fs/method/remove.html
---

'remove(string)'

This will try to delete the specified file.

When errors occur during a call, it will throw a 'Unable to remove file PATH' and hang execution.

## Examples

```javascript
var fs = require('fs');
var toDelete = 'someFile.txt';

fs.remove(toDelete);

phantom.exit();
```








