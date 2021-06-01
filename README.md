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
    - 미들웨어란 ? 라우트(유저)와 실행하는 콜백함수(응답) 사이에서 동작하는 함수.
    - 적용방법은, 전역으로 적용하는 = app.use() ;
    - 각각 적용하는 = 라우팅 과 콜백함수 사이에 쓰는방법; 두가지.

    - 모든 미들웨어함수는 유저- 응답 사이에서 동작하므로 미들웨어가 끝나고 난 뒤, 응답(콜백함수)를 실행하기 위해서 next() 가 필수적임. 혹은 미들웨어에서 중단시킬 수 있음.

    - 주요 미들웨어로는
        - Morgan - 로그를 남겨줌
        - helmet - 기초보안담당함
        - cookieParser - 쿠키를 다룰 수 있음
        - bodyParser - form데이터를 서버로 받아와서 활용가능함.
- #3.11 External Middlewares
    - npmjs.com npm i morgan
- #4.0 What are Routers?
    - Wetube Reloaded

        - / -> Home
        - /join -> Join
        - /login -> Login
        - /search -> Search

        - /users/:id -> See User
        - /users/logout -> Log Out
        - /users/edit -> Edit MY Profile
        - /users/delete -> Delete MY Profile

        - /videos/:id -> See Video
        - /videos/:id/edit -> Edit Video
        - /videos/:id/delete -> Delete Video
        - /videos/upload -> Upload Video

- #4.1 Making Our Routers
- #4.2 Cleaning the Code
- #4.3 Exports
- #4.4 Router Recap
- #4.5 Architecture Recap
- #4.6 Planning Routes
- #4.7 URL Parameters part One    
``` javascript
// 순서 중요
videoRouter.get("/:id", see);
videoRouter.get("/upload", upload);
// upload도 parameter로 인식
```
- #4.8 URL Parameters part Two
``` javascript
videoRouter.get("/:id(\\d+)", see);
videoRouter.get("/:id(\\d+)/edit", edit);
videoRouter.get("/:id(\\d+)/delete", deleteVideo);
// 정규식!! 
```

- #5.0 Returning HTML
- #5.1 Configuring Pug
    - 1단계 : pug를 설치한다.
    - 2단계 : pug를 뷰 엔진으로 설정한다. app.set("view engine", "pug");
    - 3단계 : 실제로 pug 파일을 생성한다.
    - 에러가 나는 이유!!
        - express는 기본적으로 cwd + /views에서 pug 파일을 찾는다.
        - node가 시작하는 곳은 package.json이 있는 곳
- #5.2 Partials
    - default 현재 작업 디렉토리(cwd)/views => app.set("views", process.cwd() + "/src/views");
- #5.3 Extending Templates
- #5.4 Variables to Templates
- #5.5 Recap
- #5.6 MVP Styles
- #5.7 Conditionals
- #5.8 Iteration
    - array의 모든 element에 대해 특정 행동을 취할 때
- #5.9 Mixins
    - data를 받을 수 있는 partial
- #5.10 Recap
- #6.0 Array Database part One
- #6.1 Array Database part Two
- #6.2 Edit Video part One
- #6.3 Edit Video part Two
- #6.4 Recap
- #6.5 More Practice part One
- #6.6 More Practice part Two
- #6.7 Introduction to MongoDB
- #6.8 Connecting to Mongo
- #6.9 CRUD Introduction
- #6.10 Video Model
- #6.11 Our First Query
- #6.12 Our First Query part Two
- #6.13 Async Await
- #6.14 Returns and Renders
- #6.15 Creating a Video part One
- #6.16 Creating a Video part Two
- #6.17 Exceptions and Validation
- #6.18 More Schema
- #6.19 Video Detail
- #6.20 Edit Video part One
- #6.21 Edit Video part Two
- #6.22 Edit Video part Three
- #6.23 Middlewares
- #6.24 Statics
- #6.25 Delete Video
- #6.26 Search part One
- #6.27 Search part Two
- #6.28 Conclusions