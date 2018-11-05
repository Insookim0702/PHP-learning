## 1. 윈도우 web server 설치하기
  - bitnami 프로그램 설치
  - bitnami manage는 bitnami를 통해apache, mysql, php를 통합해서 관리할 수 있는 도구이다.
  
  
 ## 2. bitnami > apache > htdocs의 경로에 접근한다.
  - htdocs driectory는 web browser가 우리가 bitnami를 통해 설치한 web server에 접속해서 web page를 요청하면 web server는 이 htdocs directory에서 web page를 찾는다.
  - 실습파일은 다 htdocs directory에 위치하면 된다.
  - 처음 깔았을 때 있는 directory들은 다 지워도 된다.
  
  
  
## php의 원리
- 일반 html문서는 web server(apache)가 직접 실행해서 응답한다.
- php page를 요청하면 web server는 자신이 처리하지 않고 php프로그램에게 처리를 넘긴다.
- 그리고 web server는 web page가 존재하는 **htdocs** directory에 존재하는 php page를 열어 ```<?php ?>``` 를 해석해서 문서를 만들어 낸다.
- web server는 php코드가 해석된 html문서를 받아 브라우저에 응답한다.



## 환경설정
1. bitnami > wampstack > php > php.ini
https://user-images.githubusercontent.com/42515875/47993894-1dd75380-e134-11e8-986b-dceb3a8a9df6.png
> **display_errors = On**으로 바꿔준다. 
- 화면에 error내용이 출력되게 한다.
- 개발환경에서는 화면에 error가 보이게 해서 개발하는 편이 수월하다.
- attcker에게는 공격수단이 된다.
2. php.ini에서 
> **opcache.enable = 0**으로 바꿔준다.
- 1 : 활성화 상태, 개발 시 내용 수정 후 30초 후에 변경이 적용된다.
- 0 : 비활성화 상태, cash를 사용하지 않겠다는 설정, 개발 시 내용 수정이 바로 됨. 

3. php.ini의 수정이 완료되었으면, manager-windows.exe를 실행해서 apache를 **restart**한다. 
