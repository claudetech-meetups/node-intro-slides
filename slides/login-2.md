## Modules used to login

Start editing `lib/index.js`

```javascript
var request    = require('request'),
    fs         = require('fs'),
    path       = require('path'),
    qs         = require('querystring'),
    prompt     = require('prompt'),
    shortenUrl = "https://api-ssl.bitly.com/v3/shorten?",
    configPath = path.join(process.env.HOME || process.env.USERPROFILE, ".nshortenrc");

...
```

* `fs` is the filesystem module, used to read and write the config file
* `path` is the module to normalize path (to work with both Windows and Unix-like OSs)
* `configPath` is the path of the file we will use to save config
