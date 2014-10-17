## Call the login function

We now need to use the login function in `bin/nshorten.js`.

```javascript
....
function fail(msg) {
  console.warn(msg);
  process.exit(1);
}

if (argv.login) {
  nshorten.login(function (err, result) {
    if (err) fail("Unable to login: " + err.message);
    console.log("Successfully logged in.");
  });
} else {
  // shorten url
}
```

Here, we simply print a success message if we could login,
or print the error message and exit with status code 1 otherwise.
