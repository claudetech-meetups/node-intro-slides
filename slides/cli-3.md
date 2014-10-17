## Parse CLI arguments

To parse CLI arguments, we will use `minimist`:

```bash
$ npm install --save minimist
```

```javascript
// bin/nshorten.js
...

var argv = require('minimist')(process.argv.slice(2), {
  boolean: ['login', 'help'],
  alias: {l: 'login', h: 'help'}
});
```

Here, we make `help` and `login` booleans, to make sure
they are not attributed any value, and we alias them
to make the command more friendly.

`process.argv.slice(2)` are the arguments provided by the
user when calling the command.

You can try logging the arguments and see what goes to `argv`.
