## Shorten function explanations

```javascript
  request.get({url: url, json: true}, function (err, response, body) {
    if (err) return callback(err);
    if (body.status_code !== 200) return callback(new Error(body.status_txt));
    callback(null, body.data.url);
  });
```

Send the request with the formed URL, and tell `request` to parse
response as JSON.

When response comes

* If an error has occured, call the callback with the error and return.
* If the body content is an error, do the same with the error message
* Otherwise, call the callback with a `null` error and return the compressed URL.

Note : Error handling is a bit creepy here because of bitly API which returns 200 even on error.
