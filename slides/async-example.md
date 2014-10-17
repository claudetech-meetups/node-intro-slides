## Sync vs Async

The same example with callback.

```javascript
// async-sample.js
var sleep = require('sleep');

function slowFunctionAsync(callback) {
    process.nextTick(function () {
        sleep.sleep(5);
        callback("result");
    });
}

slowFunctionAsync(function (result) {
    console.log(result);
});
console.log("do something else");
```

Run with

```sh
$ node async-sample.js
```

`do something else` is shown straight away.

Note : This `sleep` blocks completely, so do not use it in real world app.
