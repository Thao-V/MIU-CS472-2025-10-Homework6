# Homework 6: Exploring the Node.js Event Loop
## Explain the output of the following code
```JavaScript
console.log("start");

setTimeout(() => console.log("timeout 0"), 0);
setImmediate(() => console.log("immediate"));
process.nextTick(() => console.log("nextTick"));

Promise.resolve().then(() => console.log("promise"));

console.log("end");
```
## Run multiple time the following code and explain the output
```JavaScript
const fs = require("fs");

fs.readFile(__filename, () => {
  setTimeout(() => console.log("timeout inside I/O"), 0);
  setImmediate(() => console.log("immediate inside I/O"));
});

```
## Answer the following in 3–5 sentences each:
1. What is the role of the poll phase in the event loop?
2. Why does process.nextTick run before Promises?
3. How does blocking the event loop affect the ability of Node.js to handle multiple requests concurrently?

## Submit your answers
