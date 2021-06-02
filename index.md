## Lab 4

This lab helped us create a Fastify Node.js server, initialize it as a prject folder using Node Package Manager, and then alter it accordingly.

### Steps 
- Create initial Fastify Node.js web server
- Initialize as a Node.js project folder using Node Package Manager (npm)
- Add Fastify to project using npm
- Add git repo, exclude node_modules folder from git, make commits
- Fix MIME error, test, and commit
- Add a second route with query parameters, test, and commit

The following is an example of the starter code for initializing a fastify server:
```
// Require the Fastify framework and instantiate it
const fastify = require("fastify")();
// Handle GET verb for / route using Fastify
// Note use of "chain" dot notation syntax
fastify.get("/", (request, reply) => {
  reply
    .code(200)
    .header("Content-Type", "text/text; charset=utf-8")
    .send("<h1>Hello from Lab 4!</h1>");
});
// Start server and listen to requests using Fastify
const listenIP = "localhost";
const listenPort = 8080;
fastify.listen(listenPort, listenIP, (err, address) => {
  if (err) {
    console.log(err);
    process.exit(1);
  }
  console.log(`Server listening on ${address}`);
});
```
