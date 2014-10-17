## Read the configuration

Reading the configuration is easy, we only need
to read the file and parse the result to JSON.

```javascript
exports.readConfig = function (callback) {
  fs.readFile(configPath, 'utf8', function (err, data) {
    if (err) return callback(err);
    try {
      var config = JSON.parse(data);
      callback(null, config);
    } catch (e) {
      callback(new Error("could not parse configuration"));
    }
  });
};
```

As `JSON.parse` throws an exception on failure,
we use `try/catch` to be able to handle the error properly.
If we could read the configuration properly, we call the callback
with a `null` error and the parsed config.
