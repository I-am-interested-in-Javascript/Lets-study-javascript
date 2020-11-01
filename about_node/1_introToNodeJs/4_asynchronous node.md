# async code
node js is single threaded and event based, just like the browser \ 
unlike the browser, your nodejs app will be shared by all clients \

자바스크립트에서는 비동기처리가 더욱 중요하다고 한다. 왜냐하면 브라우저는 뭐 자기꺼 자기만 돌리니까 망해도 사용자 한명만 망하는데, 서버는 여러 사용자가 다 같이 쓰는거라 얘가 죽으면 모든 사용자에게 영향을 끼치기 때문이다. 

# async patterns
async/ await !!

- callback pattern
doAsyncThing((error, result) => {}) // callback takes error as first arg, and result as second

- promises
doAsyncThing().then(result => {}).catch(error => {})

- async/await
const run = async () => {
    const results = await doAsyncThing()
    console.log("hello")
}


# promise all
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise/all


# servers
one server, handling many requests from clients

a server's job is to handle a request from some sor of client(browser, mobile app, another server etc)

<strong> without considering scaling, one server instance will handle many client requests. Compared to a client app where that code only cared about itself on the host machine. </strong> -> this concept is super important. 

nodejs has build in and community packages for build all types of servers(API's, static, realtime etc)