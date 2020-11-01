## introduction

## node js로 할 수 있는 것
pretty much everything
1. tooling
2. APIs(rest, realtime..)
3. CDNs
4. Shareable libraries
5. Desktop applications

## 노드의 설치 및 버전관리를 어떻게 하는가?
1. node를 설치하는 방법은 2가지가 있다. 
- 공식 사이트에서 다운로드 받는 방법
  * 내가 사용했던 방법인데, 버전관리가 좀 난감한 면이 있다. 

- nvm을 이용하는 방법
  * node version manager(nvm)은 node 커뮤니티에서 만들어진거라, Node js foundation랑은 관계가 없긴하다. 근데 추천하는 방식이다.
  * [설치](https://github.com/nvm-sh/nvm#installation)


## [NVM 사용법(node version manager)](https://github.com/nvm-sh/nvm#installation)
- [잘 정리된 블로그 참고자료](https://velog.io/@mayinjanuary/NVM-%EC%9D%B4%EB%9E%80-%EB%85%B8%EB%93%9CNode.js-%EB%B2%84%EC%A0%84-%EA%B4%80%EB%A6%AC%ED%95%98%EB%8A%94-%EB%B2%95)

- nvm 설치하면 기존에 설치된 node는 어떻게 되나?
nvm 설치하기 전에 지워라고 하는 글도 있는데, 굳이 안지워도 

`which node` 라고 하면 `.../.nvm/versions/node/v10.6.0/bin/node` 이런 식으로 기존에는 .npm 경로에 있는 node를 사용하지만, nvm을 설치하고 나면 .nvm내의 node를 사용하게 된다. 

그리고 mac을 기준으로 bash_profile에 환경변수 설정이 들어간다. 

[here](https://madplay.github.io/post/nodejs-install-osx) 에 설명이 잘 되어있다. 
