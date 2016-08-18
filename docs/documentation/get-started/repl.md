---
layout: post
title: REPL
categories: docs docs-get-started
permalink: repl.html
---

From version 1.5 PhantomJS will provide an Interactive Mode, also known as REPL: Read-Eval-Print Loop.

### Why a REPL?

Sometimes you feel the urge to test out some little/medium size Javascript code, to see how `x` or `y` works (or if they do at all). So, usually the choice would be to jump on [Firebug](http://getfirebug.com/) (or the [Webkit Inspector](http://trac.webkit.org/wiki/Web%20Inspector) or [Opera Dragonfly](http://www.opera.com/dragonfly/) or...) and type away.

Well, PhantomJS is a commandline tool. It's designed for the commandline; its habitat is your console. So, as such, a way was missing to have a ready to go mode. Even Node.js has one!

So, that's where the idea of the REPL came from.

### How does it work

As mentioned above, REPL stands for READ-EVAL-PRINT LOOP: every line you type (READ) (i.e. type than click ⏎) is sent to the interpreter for immediate interpretation (EVAL) and provide feedback (PRINT).

This is (from version 1.5 onward) the new default mode in which PhantomJS starts if you don't provide any parameter.

Here is an example use that will probably explain better than many words:

```bash
$ phantomjs⏎
phantomjs> phantom.version⏎
{
  "major": 1,
  "minor": 5,
  "patch": 0
}
phantomjs> console.log("phantom is awesome")⏎
phantom is awesome
undefined
phantomjs> window.navigator⏎
{
  "cookieEnabled": true,
  "language": "en-GB",
  "productSub": "20030107",
  "product": "Gecko",
  "appCodeName": "Mozilla",
  "mimeTypes": {
    "length": 0
  },
  "vendorSub": "",
  "vendor": "Apple Computer, Inc.",
  "platform": "MacIntel",
  "appName": "Netscape",
  "appVersion": "5.0 (Macintosh; Intel Mac OS X) AppleWebKit/534.34 (KHTML, like Gecko) PhantomJS/1.6.0 (development) Safari/534.34",
  "userAgent": "Mozilla/5.0 (Macintosh; Intel Mac OS X) AppleWebKit/534.34 (KHTML, like Gecko) PhantomJS/1.6.0 (development) Safari/534.34",
  "plugins": {
    "length": 0
  },
  "onLine": false
}
```

Every command gets evaluated on the spot, and the actual return value is printed.

To exit? The usual: either type `phantom.exit()` or CTRL+C or CTRL+D.

### Auto-completion

One of the feature that we saw could bring a lot of value is auto-completion. Sometimes, as much as people like documentation, if they could get a list of methods or properties by just tapping TAB (i.e. `→|`) it could make all the difference:

```bash
phantomjs> phantom.→|
phantomjs> phantom.injectJs→|
phantomjs> phantom.exit→|
phantomjs> phantom.version→|
phantomjs> phantom.outputEncoding⏎
"UTF-8"
phantomjs>
```

So, if you remember there was a method that did just x but can't just remember what it was called, now the fastest way to the answer can be just few characters away.

### Command History

And, of course, the REPL couldn't be one without history support: just use your UP and DOWN arrow keys to navigate through the list of commands you typed before, for quick reference.

The history file is saved at:

```bash
QDesktopServices::DataLocation + "/phantom_repl_history"
```

where DataLocation is defined by Qt and it depends on the operating system. On Mac, for example, it is at:

```bash
"~/Library/Application Support/Ofi Labs/PhantomJS/phantom_repl_history"
```

### Is it bug free?

Ehm, no. This is a new functionality and it's built making all sorts of Javascript manipulation: there are bugs and we are listening (or waiting for a pull request).

### Credits

We couldn't have built the REPL and all it's nice console-like features without [Linenoise](https://github.com/tadmarshall/linenoise) project (an improved fork of [the original](https://github.com/antirez/linenoise)).
