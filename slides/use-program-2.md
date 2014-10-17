## Use your program better

Modify `package.json` to add the following

```json
...
  "bin": {
    "nshorten": "bin/nshorten.js"
  }
...
```

and run (with `sudo` if you get a permission error)

```bash
$ npm install -g .
```

You can now use your new command.


```bash
$ nshorten --login
nshorten: token:  MY_SUPER_SECRET_OAUTH_TOKEN
Successfully logged in.
$ nshorten https://blog.claudetech.com
http://bit.ly/1svXFdY
```
