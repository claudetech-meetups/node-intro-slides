## Shorten function

The function will take

* the URL to shorten
* a configuration (containing OAuth token)
* a callback to call when done.
  * the callback takes an error as first argument and result as second

```javascript
// lib/index.js
var request = require('request');

module.exports.shorten = function (url, config, callback) {
    // TODO
}
```

* `module.exports` is what will be exported by the module
* if assigning to `exports.keyName`, `module.` can be omitted
* the content of `module.exports` will be available when using `require`
