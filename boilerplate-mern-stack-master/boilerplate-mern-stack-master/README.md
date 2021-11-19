Hello, My Friends  
Thank you for having interest in this repository ! 

To use this application, 

1. make dev.js file inside config folder 
2. put mongoDB info into dev.js file 
3. Type  " npm install " inside the root directory  ( Download Server Dependencies ) 
4. Type " npm install " inside the client directory ( Download Front-end Dependencies )


If you have problem, feel free to ask me ^^ 

You can watch the tutorial for this app.

https://www.youtube.com/channel/UCFyXA9x8lpL3EYWeYhj4C4Q?view_as=subscriber


-- 내 노트..
# react_youtube_clone
유튜브 클론코딩


mongoDB설치
https://www.mongodb.com/try/download/enterprise

1. mongodb설치는 설치 파일 받아서 디폴트로설치.(custom 설치시 설치할 경로정도는 선택후 디폴트로 next...광클...)
 -  windows 시스템 환경 변수 등록(ex: C:\설치한경로\bin\  -->bin폴더까지 잡아 줘야 한다.)

 
2. mongodb용 data폴더 생성
  C:\data\db\


3. 윈도우shell 실행.


4. mongodb 실행.(실행한 shell창을 닫으면 mongodb도 종료 됨.)
  ```
  > mongod --dbpath="C:\data\db\"
```

5. 윈도우shell 하나더 실행.


6. mongodb 접속.
 ```
 > mongo
```
 

7. admin DB선택후 관리용 계정 생성.
```
> show databases   -->모든database 보여줌.

admin   0.000GB 
config  0.000GB 
local   0.000GB 


>use admin   -->admin DB선택
switched to db admin

>db  -->현재 선택한 DB확인
admin

>db.createUser({user:"root",pwd:"패스워드",roles:["root"]}) -->관리계정 생성.
Successfully added user: { "user" : "root", "roles" : [ "root" ] } 
```


8. mongodb 보안설정 및 외부접근 환경 설정

mongodb설치폴더\bin\mongod.cfg 파일 수정.
```
# network interfaces
net:
  port: 27017  -->mongodb접근 포트 변경 해도된다.
  bindIp: 0.0.0.0  -->모든IP허용인가?


#processManagement:
security:
  authorization: enabled   -->인증옵션 활성.
```
 

9. mongodb 재시작
 - Windows mongoDB 재시작
 ```
  > net stop MongoDb
  > net start MongoDb
```
 

10. 사용할DB 생성 및 계정 설정.
```
>use content -->database 생성.
switched to db content 
>db -->현재database 확인
content 
>db.createUser({user:"daview",pwd:"패스워드",roles:["readWrite"]}) -->현재 DB에 일기, 쓰기권한으로 사용자 등록
Successfully added user: { "user" : "daview", "roles" : [ "readWrite" ] }
```
 

11. 이후 compass로 접근하여 콜렉션 생성등 하면된다.

외부에서 접근 방법.

mongodb://daview:패스워드@localhost:27017/content   -->mongodb://계정:패스워드@도매인또는IP:포트/db명






VS Code
rfce =>> react 기본폼 만들기


npm install시에 --save옵션을 주어야 package.json에 명시가 됨
