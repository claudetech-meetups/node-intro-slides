## About `require`

Then create `lib/index.js` with

```javascript
var request = require('request');
```

* `require` loads modules present in `node_modules` (local or global)
* with relative path, `require` loads module current module path
* `require` returns everything exported by the module
* it only returns, so we need to put the result in a variable
* quite different from `import` in Java or `include` in C.
