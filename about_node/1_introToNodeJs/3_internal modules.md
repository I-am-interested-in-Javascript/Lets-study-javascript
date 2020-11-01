# Internal modules and npm

## shipped modules 

모듈은 크게 node깔았을때 무조건 같이 오는 애들이 있다. 

* fs: filesystem module to interacting with files on a machine
* http: low level-ish module for creating network based programs like APIs
* path: useful for manipulationg path strings and handling differences across many OS's


## Three module types, one require 
모듈의 타입에 따라 require할때 경로 지정하는 방법이 다르다. 

- custom local modules
  - var lib = require('./rel/to/lib') # always starting with .
- remote modules
  - var lib = require('lib') # the same name you need to install it with npm
- shipped modules
  - var fs = require('fs') # internal module, remote module with the same name takes it

리모트 모듈과 내장 모듈이름이 겹치는 경우도 있는데 이런일은 만들지 마라. 

## npm(cli to mange remote modules)
- ships with nodesjs
- allows you to publish download, and update modules
- uses pacakage.json file in your nodejs project to determine dependencies
- stores remote modules in the node_modules folder
- ...whole bunch of other stuff