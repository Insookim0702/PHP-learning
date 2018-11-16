## php_function
> ```nl2br($변수이름)```
<br>
문자열 편집을 위해 html의 <br>태그를 사용하지 않고 편집된 문자열 그대로를 web에 출력해주는 php의 function이다.

ex)
>```strlen($변수이름)```
<br>
문자열의 개수를 새서 출력하는 php의 function이다.<br>
ex) 

## php url에 parameter값을 받아서 동적인 web application 만들기

> 127.0.0.1/index.php?name=kakao
<br>


위의 주소로 입력을 주면 ```$_GET['name']```으로 param값을 받을 수 있다.
param값을 2개 이상 받을 경우엔 **"&"** 을 이용한다.
<br>
> 127.0.0.1/index.php**?name=kakao&age=13
