1. promise chaining 관련 글
https://javascript.info/promise-chaining

2. 프로미스 관련 글 
https://joshua1988.github.io/web-development/javascript/promise-for-beginners/

3. fetch는 웹 api이다
https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch#:~:text=The%20Fetch%20API%20provides%20a,such%20as%20requests%20and%20responses.&text=Fetch%20also%20provides%20a%20single,CORS%20and%20extensions%20to%20HTTP.

4. async await 동작원리
https://javascript.info/async-await

`let’s emphasize: await literally suspends the function execution until the promise settles, and then resumes it with the promise result. That doesn’t cost any CPU resources, because the JavaScript engine can do other jobs in the meantime: execute other scripts, handle events, etc.`


5. locale
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Intl/Locale#:~:text=Locale%20object%20was%20created%20to,language%20identifier%20and%20extension%20tags.&text=Traditionally%2C%20the%20Intl%20API%20used,locales%2C%20just%20as%20Unicode%20does.

React 에서 locale 
https://www.smashingmagazine.com/2017/01/internationalizing-react-apps/

6. 깊은 복사 , 얕은 복사
- ramda: https://ramdajs.com/docs/#equals
- 왓챠 https://medium.com/watcha/%EA%B9%8A%EC%9D%80-%EB%B3%B5%EC%82%AC%EC%99%80-%EC%96%95%EC%9D%80-%EB%B3%B5%EC%82%AC%EC%97%90-%EB%8C%80%ED%95%9C-%EC%8B%AC%EB%8F%84%EC%9E%88%EB%8A%94-%EC%9D%B4%EC%95%BC%EA%B8%B0-2f7d797e008a
- https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Global_Objects/Array/slice

7. es5, es6 차이
https://yngmanie.space/posts/es5_vs_es6

8. react 만들기 
https://github.com/textuel/Woowa_Tech_Learning_React_Typescript/blob/master/ms/week_2/Tuesday.md

전체코드 https://gist.github.com/ibare/c736f63fba835c172e60aa98a996dada

```
export function createElement(type, props, ...children) {
  // jsx 처리
  if (typeof type === "function") {
    return type.apply(null, [props, ...children]);
  }
  return { type, props, children };
}
```

react의 createelement
https://reactjs.org/docs/react-without-jsx.html

apply 함수
https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Global_Objects/Function/apply
9. 리덕스 만들기
https://github.com/textuel/Woowa_Tech_Learning_React_Typescript/blob/master/ms/week_1/Thursday.md


10. Lint 와 prettier
튜토리얼 : https://www.youtube.com/watch?v=Y3kjHM7d3Zo&ab_channel=%EA%B9%80%EC%A0%95%ED%99%98
카카오 글: https://tech.kakao.com/2019/12/05/make-better-use-of-eslint/
공식문서의 룰: https://eslint.org/docs/rules/

eslint - 포맷팅  + 코드 품질 체크 /  수정은 개발자가
prettier - 포매팅 only / 수정을 자동으로 이쁘게

둘다 통합해서 사용을 함: https://prettier.io/docs/en/integrating-with-linters.html

npm run lint 이런식으로 매번 사용할 수 없기 때문에, 깃 훅을 사용하거나(깃 커밋이나 스테이지 할때 검사), 에디터 확장자 사용(코딩할때바로검사)


11. package.json 캐럿과 틸트의 차이
https://blog.outsider.ne.kr/1041


12. 스코프와 클로져
https://medium.com/@khwsc1/%EB%B2%88%EC%97%AD-%EC%9E%90%EB%B0%94%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8-%EC%8A%A4%EC%BD%94%ED%94%84%EC%99%80-%ED%81%B4%EB%A1%9C%EC%A0%80-javascript-scope-and-closures-8d402c976d19

https://velog.io/@bathingape/%EC%8A%A4%EC%BD%94%ED%94%84Scope%EC%99%80-%ED%81%B4%EB%A1%9C%EC%A0%80Closure-%EC%9D%B4%ED%95%B4

클로저란?
```
내부함수는 외부함수의 지역변수에 접근 할 수 있는데 외부함수의 실행이 끝나서 외부함수가 소멸된 이후에도 내부함수가 외부함수의 변수에 접근 할 수 있다.
이러한 메커니즘을 클로저라고 한다
```

그리고 그 내부함수도 
```
내부함수에서 외부함수에서 선언된 변수를 사용한다면 그 내부함수는 클로저이다.
```


13. DOM vs Virtual Dom: https://reactkungfu.com/2015/10/the-difference-between-virtual-dom-and-dom/
