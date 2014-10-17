## About callbacks

A callback is a function to be executed when the
result of an operation is ready.

Callbacks are usually used for operations
taking time, but not using CPU a lot.

NodeJS uses callbacks extensively.

Example use case

* We want to access a remote HTTP server
* Requests takes time
* We do not want to block the program
