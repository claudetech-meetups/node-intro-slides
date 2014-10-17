## About callbacks

```js
function slowFibo(n) {
    if (n <= 1) return n;
    return slowFibo(n - 1) + slowFibo(n - 2);
}
var res = slowFibo(40);
console.log("computing");
console.log(res);
function slowFiboCb(n, cb) {
  process.nextTick(function() {
    var res = slowFibo(40);
    if (cb) cb(res);
  });
}
slowFiboCb(40, function (res) {
  console.log(res);
});
console.log("computing");
```

* `slowFibo` returns immediately, blocking the process.
    * Can use the return value. `console.log`  executed after computation
* `slowFiboCb` does not return immediately
    * Use result in the callback. `console.log` executed before computation.
