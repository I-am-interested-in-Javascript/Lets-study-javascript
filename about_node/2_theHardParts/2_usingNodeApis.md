1. Libuv
https://github.com/libuv/libuv

## Node auto-runs the code (function) for us when a request arrives from a user
```
function doOnIncoming(incomingData, functionsToSetOutgoingData){
  functionsToSetOutgoingData.end("welcome!");
}
const server = http.createServer(doOnIncoming)
server.listen(80)

```

1. we don't know when the inbound request would come - we have to rely on node to trigger js code to run

2. javascript is single-threaded & synchronous. All slow work(speaking to a database) is done by node in the background



### two parts to calling a function - executing its code and inserting input(arguments)
Node not only will auto-run our function at the right moment, it will also automatically insert whatever the relevant data is as the argument(input)

Sometimes it will even insert a set of functions in an object(as an argument) which give us direct access to the message(in Node)
being sent back to the user and allows us to add data to that message



### creating  a server under the hood
```
function doOnIncoming(incomingData, functionsToSetOutgoingData){
  functionsToSetOutgoingData.end("welcome!");
}
const server = http.createServer(doOnIncoming)
server.listen(80)
```

two auto created on

