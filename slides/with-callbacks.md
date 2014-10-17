## Example with callbacks

The same example using callback would look like this.

```javascript
http.get("http://myhttpserver.com", function (response) {
    // use reponse here
});
http.get("http://myotherhttpserver.com", function (otherResponse) {
    // use otherReponse here
});

// no need to wait for HTTP requests to be ready
var someOtherResult = makeSomeComputation();
```

Here, we can run the HTTP request, without having to care
of when the result will come back, and continue executing the
rest of the program.
