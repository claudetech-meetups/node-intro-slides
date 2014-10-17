## Sync vs Async

Small example to try. Run `npm install sleep` before running.

```javascript
// sync-sample.js
var sleep = require('sleep');

function slowFunction() {
  sleep.sleep(5);
  return "result";
}

var result = slowFunction();
console.log("do something else");
console.log(result);
```

Run with

```sh
$ node sync-sample.js
```

`do something else` is shown only after `slowFunction` finishes.
