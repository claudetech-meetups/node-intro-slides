## Parse CLI arguments

First, we will write a small `usage` function, to explain how the
command works:

```javascript
#!/usr/bin/env node

var nshorten = require('../lib');

function usage (msg) {
  if (msg) console.warn(msg);
  console.log("usage: nshorten [--login] URL")
  process.exit(msg ? 1 : 0);
}
```

When the command is not used properly, print a message
and exit with status 1 (error), else exit with status 0.
