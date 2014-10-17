## Login function explanations

```javascript
  prompt.get(['token'], function (err, result) {
    if (err) return callback(err);
    var dummyUrl = "http://claudetech.com";
    exports.shorten(dummyUrl, result, function (err) {
      if (err) return callback(err);
      fs.writeFile(configPath, JSON.stringify(result, null, 4), callback);
    });
  });
```

* Prompt for the token
* If error, call the callback with the error and return
* Else, the result will be `{token: USER_INPUT}`
  * Try to shorten a dummy URL
  * If fails, call the callback with an error
  * Else save the config as JSON to `$HOME/.nshortenrc`

