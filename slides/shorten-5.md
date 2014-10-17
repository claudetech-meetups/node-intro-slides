## Shorten function explanations

```javascript
  if (!config.token) {
    return callback(new Error("you need a token"));
  }
```

If no token given, call the callback with an error, and
`return` to avoid executing the rest of the function.

```javascript
  var data = {access_token: config.token, longUrl: longUrl},
      url  = shortenUrl + qs.stringify(data);
```

* `data` is defined to match the bitly documentation.
* `data` is then transformed in query string (`access_token=....&longUrl=....`)
  and appended to the URL. Note that the URL ends with `?` to accept the query string.
