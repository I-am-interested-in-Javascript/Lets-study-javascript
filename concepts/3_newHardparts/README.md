# MEMO
https://frontendmasters.com/courses/javascript-new-hard-parts/javascript-code-execution/

1. Foundations of Javascript
- global에서 함수가 실행되면, we create a global execution context

- thread of execution(parsing and executing the code line after line)

- live memory of variables with data(known as a global variable environment)

=> these two are execution context(in this case global execution context) \ 
=> thread is singular(no two stuff running at once) \
=> use stack to keep track of where an exeution context is created
top of call stack is where I am right now

2. Asynchronous Javascript
```
Asynchronicity is the backbone of modern web development in javascript

-javascript is single threaded (one command executing at a time) and has a synchronous execution model(each line is executed in order the code appears)

so what if we need to wait some time before we can execute certain bits of code? Perhaps we need to wait on freash data from an API/server request of for a timer to complete and then execute our code

- we have conundrum - a tenstion between wanting to delay some code execution but not wanting to block the thread from any further code running while we wait
-> 코드 실행을 지연시키고 싶지만(api콜같은걸 하고싶지만), 그럼서도 thread를 블락해서 다른코드가 실행되는걸 막고싶진않다. 

```

핵심 - 인트로에서 복습했듯이(hard parts 원래 강의 https://frontendmasters.com/courses/javascript-hard-parts-v2/ 여기에서 설명이 끝장난다) 자바스크립트는 무조건 한번에 하나만 실행할 수 있는 구조이다. call stack을 이용해서 execution context 를 추적하는 방식. 그런데 만약 한줄한줄 실행하고 다음으로 넘어갈때, 어떤 부분에서 멈춰야한다면??

like for example, 

```
const result = fetch(url...); -> what if it takes 3000 milli seconds to return from server? 
```
should we wait here, waiting until the fetch completes? My brower might stop working, and user might feel 'something is totall wrong with this website' and leave.
What can we do?

이런 문제때문에 asynchronous라는 개념을 배운다(해도해도 아직 뭔가 마음이 받아들이진 못한것 같다) 한번에 한줄만 실행하는 자바스크립트의 특성상 시간이 오래걸리는 줄을 실행한다고 그줄에서 멈춰서 값을 받아오는걸 대기하던, 연산을 기다리던 하면 그거말고 다른 급한걸 할수가 없으니까....!



pure javascript doesn't know how to talk to the internet. That feature is from browsers. 즉, 자바스크립트는 (facade) that we use to use features in web browsers. 









3. Iterators





4. Generators & Async/await

