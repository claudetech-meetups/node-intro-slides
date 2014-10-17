## Try shorten function

From the project directory:

```bash
$ node
> var nshorten = require('./lib/index');
undefined
> nshorten.shorten("http://claudetech.com", {token: "OAUTH_TOKEN"}, function (err, url) {
...   if (err) console.log(err.message);
...   else console.log(url);
... });
undefined
> http://bit.ly/ZHgn8y
```

`...` is shown on new line.

Of course, replace `OAUTH_TOKEN` with your own token.
