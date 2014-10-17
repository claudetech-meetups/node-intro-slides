## Shorten function

```javascript
// lib/index.js
var request    = require('request'),
    qs         = require('querystring'),
    shortenUrl = "https://api-ssl.bitly.com/v3/shorten?";

exports.shorten = function (longUrl, config, callback) {
  if (!config.token) return callback(new Error("you need a token"));
  var data = {access_token: config.token, longUrl: longUrl},
      url  = shortenUrl + qs.stringify(data);

  request.get({url: url, json: true}, function (err, response, body) {
    if (err) return callback(err);
    if (body.status_code !== 200) return callback(new Error(body.status_txt));
    callback(null, body.data.url);
  });
}
```
