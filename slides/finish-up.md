## Using the configuration

We can now use the configuration before calling the
`shorten` function, to get the saved `token`.

```javascript
if (argv.login) {
    ...
} else {
  var url = argv._[0];
  var config = nshorten.readConfig(function (err, config) {
    if (err) fail("Could not read config: " + err.message + "\nTry running 'nshorten --login'");
    nshorten.shorten(url, config, function (err, res) {
      if (err) fail(err.message);
      console.log(res);
    });
  });
}
```

* Try to read the configuration, print and fail on error
* Call shorten with the read configuration
* Print and fail on error
* Print the shorten URL if no error
