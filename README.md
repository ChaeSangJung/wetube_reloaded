- #2.1 Installing Express
    - npm run win
    - npm i express
- #2.2 Understanding Dependencies
- #2.3 The Tower of Babel
    - babel : 최신의 js코드를 무난난 예전의 js코드로 변환
    - npm install --save-dev @babel/core
    - npm install @babel/preset-env --save-dev
``` javascript
{
    "presets": ["@babel/preset-env"]
}
```
- #2.4 Nodemon
    - npm install @babel/node --save-dev

- #3.0 Your First Server
    - request를 listenning
- #3.1 GET Requests
    
- #3.2 GET Requests part Two
    - request : 유저가 뭔가를 요청하거나,보내거나, 네게 무슨 행동을 한다.
- #3.3 Responses
    - req & res
        - req = POST 로 전달한 정보를 요청해서, 정보를 받음 !
        - res = 정보를 응답! ( res.send )
- #3.4 Recap
- #3.5 Middlewares part One
- #3.6 Middlewares part Two