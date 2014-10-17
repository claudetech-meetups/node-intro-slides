## Use CLI arguments

Then, we check what to do depending on arguments.

```javascript
// bin/nshorten.js
....

if (argv.h) usage();
if (!argv.login && argv._.length === 0) usage("No URL given");

if (argv.login) {
  // make login
} else {
  // shorten url
}
```

If asked for help, call usage without message.
Print usage if no URL given, and exit with error.

If the arguments are correct, run the program.
