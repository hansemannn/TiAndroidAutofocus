# TiAndroidAutofocus

Prevents TextFields in Android to auto-focus.

> **NOTE**: When using Titanium SDK 7.3.0+, Android matches the iOS / Windws behavior and does not auto-focus
the first text field when a window opens. See [TIMOB-24138](https://jira.appcelerator.org/browse/TIMOB-24138) for details!

### Usage
Simply create a View using this module above the first TextField occurence to prevent autofocus.
That's it!

**JS Usage**

```js
var autofocus = require('de.marcelpociot.autofocus');
var win = Ti.UI.createWindow({
    backgroundColor: 'white'
});

var textField = Ti.UI.createTextField({
    width: 100,
    value: 'I do not auto-focus'
});

win.add(autofocus.createView());
win.add(textField);

win.open();
```

**Alloy usage**

```xml
<View platform="android" module="de.marcelpociot.autofocus" />
<TextField value="No more ugly autofocus!" />
```
