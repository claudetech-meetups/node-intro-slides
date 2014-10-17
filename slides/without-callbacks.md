## Example without callbacks

Without using callbacks, it would look like this.
The functions here are only use as an example.

```javascript
var response = http.get("http://myhttpserver.com");
// wait for response to be ready
var otherResponse = http.get("http://myotherhttpserver.com");
// wait for otherResponse to be ready
var someOtherResult = makeSomeComputation();
```

In the example above, the process would block at each step,
without using any CPU resource.
