web server - apache

web browser에서 index.html을 요청하면 web server는 html을 직접 처리할 수 있다.
server 컴퓨터에 있는 ssd나 하드디스크에 있는 hdoc 디렉토리에서 index.html을 읽어서 web browser에 다시 전송해주면 web browser에 화면에 띄워준다.


web browser에서 index.php를 요청하면 web server는 php는 자신의 소관이 아니라는 것을 안다. 그리고 php라는 프로그램에게 일을 넘긴다. hdoc에 있는 index.php를 문법에 따라 읽어서 html로 해석해서 web browser에 전달한다.
html은 동적이지 않은 정보를 web browser에 전달한다. php는 동적인 정보를 web browser에 전달한다.


web browser를 reload할 때마다 동적으로 화면이 표시된다.
html은 정적인 문서이다.
