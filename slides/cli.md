## Create CLI

Create the file `bin/nshorten.js` and make it executable.

```bash
$ touch bin/nshorten.js
$ chmod +x bin/nshorten.js
```

then make it execute with Node using the shebang:


```javascript
#!/usr/bin/env node

console.log("test executable");
```

and try it:

```bash
$ ./bin/nshorten.js
test executable
```
