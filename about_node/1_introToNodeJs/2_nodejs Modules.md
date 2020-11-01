## Node.js Modules
### 들어가며
자바스크립트로는 주로 프론트엔드개발만 해오던 나로썬, 도당최, 자바스크립트를 브라우저 밖에서 우째 돌리겠단건지? 의아하지만 아래의 두가지 큰 차이가 있다고 한다. 

일단, nodejs -> 그냥 브라우저 밖에서 쓸수있는 자바스크립트로, 그 외에 뭐 암것도 없고, 커뮤니티에서 뭔가 만들어냈음


|브라우저에서..|node js(브라우저 밖에서, pure logic)| 설명 |
|------|------|------|
| Browser | 브라우저 없다, no browser based APIs (pure javascript) | node는 브라우저가 없으니, 브라우저기반의 api들을 쓸수없고, 진짜 로직이다. 뵈는것도 없다. |
| Build interactive apps for the web | Build server side apps and scripts | node는 서버나 스크립트를 구성할 수 있다. |
| DOM | No DOM(Nope, no GUI)(can virtualize) | 돔 없다. 근데 뭔가 비슷한건 할 수 있다고하는데 무슨말인지 잘모르겠다. | 
| Window | No window, but does have a global | window말고 global이라는 전역객체가 있다. |
| Fragmentation | Versioned, so no fragmentation | 브라우저에서는 자바스크립트의 어떤건 지원되고 안되고 난리인데, nodejs는 버전관리가 되는거라 되면 무조건 되는거고 안되면 안되는거고 그런식이다 |
| optional modules(es6) | Required modules(commonjs +) | 브라우저에서는 es6의 import/export 시스템으로 모듈관리하는데, node는 common js로 해놔가지고, 아직 require 사용해서 모듈을 가져온다. |
| cannot access filesystem | can access filesystem | 노드는 파일 시스템도 접근된다, 브라우저는 당연히 안되야한다. 되면 난리난다. |
| async | async | 둘다 됨~ |

** common js 관련 문서: https://d2.naver.com/helloworld/12864


## globals in nodejs
node js gives us helpful globals but just like the browser, you should not create your own: 노드는 브라우저처럼 전역객체를 가지고 있는데, 건들지마라진짜..

* process - has information about the environment the program is running in
* require - fucntion to find and use modules in current module ( how to import module )

... common js ... ?

* __dirname: the current directory path
* module - information about current module, methods or making module consumable( how to export) 
-> everything is module

- the difference between require and import
https://stackoverflow.com/questions/46677752/the-difference-between-requirex-and-import-x/46677972#:~:text=The%20major%20difference%20between%20require,from%20ES6%2C%20won't.&text=js'%20notes%2C%20import%20won',the%20path%20of%20the%20module.

* global - like window, its the "global" object, Almost never use this
 


## 번들링이란
https://velog.io/@bigbrothershin/Webpack-JS-ES6-%EB%AA%A8%EB%93%88%EC%8B%9C%EC%8A%A4%ED%85%9C-%EC%9D%B4%ED%95%B4


## node js 의 settimeout
https://nodejs.org/en/docs/guides/timers-in-node/ \ 
브라우저에서 사용하는 settimeout이랑 다르지만 비슷한 무언가이다. 