# Shower speech control plugin for Shower
## Install
```html
…
<script src='node_modules/shower-core/shower.min.js'></script>
<!-- Add plugin script -->
<script
src='node_modules/shower-speech-control/shower-speech-control.js'></script>
```

Then you have 2 ways for run plugin:
1. From slide or other place.

```js
shower.modules.require(['shower'], function (sh) {
    var showerInstance = sh.getInited()[0];
    var plugin = sh.plugins.get('shower-speech-control', showerInstance);
    plugin.start();
    // ...
    // plugin.stop();
});
```

2. Autoinit.
```
// Before shower.js
window.showerOptions = {
    'plugin_shower-speech-control': {
        autoInit: true
    }
};
```

## How to example
```html
<section class="slide" data-speech-bookmark="the end">
    <h2>THE END</h2>
</section>
```

Now when you say `the end` Shower open this slide.

## Browsers
// todo: now works in chrome.
