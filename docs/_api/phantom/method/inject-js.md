---
layout: post
title:  injectJs
section: phantom
kind: method
permalink: api/phantom/method/inject-js.html
---

`phantom.injectJs(filename)` {boolean}

Injects external script code from the specified file into the Phantom outer space. If the file cannot be found in the current directory, [`libraryPath`]({{ site.url }}/api/phantom/property/library-path.html) is used for additional look up. This function returns `true` if injection is successful, otherwise it returns `false`.

## Examples

```javascript
var wasSuccessful = phantom.injectJs('lib/utils.js');
```








