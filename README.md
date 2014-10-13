# swinch.js

## A lightweight, customisable, horizontal touch detection script

swinch is a vanilla JavaScript plugin that detects horizontal swipes on the element you pass to it, and provides a callback with the direction of the swipe.

### Usage

```js
var swipeElem = new swinch(document.getElementById('swipe-elem'), {
  callback: function(direction) {
    if (direction === 'left') {
      doSomethingOnLeft();
    }
    else {
      doSomethingOnRight();
    }
  }
});
```

The sensitivity of the swipe can be adjusted per instance with `thresholdDuration` (default: 50 [ms]) and `thresholdDistance` (default: 30 [px]) options. For example:

```js
var swipeElem = new swinch(document.getElementById('swipe-elem'), {
  thresholdDuration: 150,
  thresholdDistance: 100,
  
  callback: function(direction) {
  }
});
```

---

Copyright (c) 2014 Matt Stow  
Licensed under the MIT license (see LICENSE for details)