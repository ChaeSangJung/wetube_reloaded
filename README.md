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
    - 라우팅 후, 콜백함수 사이에서 동작할 함수. 즉, 사이에 있는 함수.
    - 주의 : next()가 꼭 필요하다 !! 안그럼 다음에 실행할 콜백함수가 실행하지 못할거야!!
    - 각개적용 = 라우팅 - 콜백 사이에 직접 위치해줌.
    - 모두적용 = app.use () 로 적용해주고, 해당 코드 아래에 있는 모든 코드에 적용됨

    - Middleware : 유저와 마지막 응답 사이에 존재하는 것
    - 1. 처리가 끝날 때까지 연결되어 있는 것
        - 시작 : browser에서 접속하려 할 때 그때가 "시작"
        - index 파일 실행
            - route가 존재하는지 살펴봄(/)
            - route 찾음 => handleHome 실행
            - handleHome 응답을 전송
- #3.6 Middlewares part Two