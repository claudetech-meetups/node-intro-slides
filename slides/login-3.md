## Login function

The login function takes a single callback function,
which takes an error as argument.

```javascript
// lib/index.js
...
exports.login = function (callback) {
  prompt.start();
  prompt.message = "nshorten";
  prompt.get(['token'], function (err, result) {
    if (err) return callback(err);
    var dummyUrl = "http://claudetech.com";
    exports.shorten(dummyUrl, result, function (err) {
      if (err) return callback(err);
      fs.writeFile(configPath, JSON.stringify(result, null, 4), callback);
    });
  });
}
```

Here, we first initialize the prompt and set the prompt message
to `nshorten`.
