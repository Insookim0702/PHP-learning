## php_function
> ```nl2br($변수이름)```
<br>
문자열 편집을 위해 html의 <br>태그를 사용하지 않고 편집된 문자열 그대로를 web에 출력해주는 php의 function이다.
ex)
![](https://user-images.githubusercontent.com/42515875/48600037-9bf5ee80-e9ad-11e8-932f-9d2fd4d06529.png)
![](https://user-images.githubusercontent.com/42515875/48600215-630a4980-e9ae-11e8-8a26-046e9b8a6dc9.png)

>```strlen($변수이름)```
<br>
문자열의 개수를 새서 출력하는 php의 function이다.<br>
ex) 

## php url에 parameter값을 받아서 동적인 web application 만들기

> 127.0.0.1/index.php?name=kakao
<br>
![](https://user-images.githubusercontent.com/42515875/48600036-9ac4c180-e9ad-11e8-96a8-d0039eaf7be4.png)
![](https://user-images.githubusercontent.com/42515875/48600214-61d91c80-e9ae-11e8-8670-749127a6ccc4.png)

![](https://user-images.githubusercontent.com/42515875/48600034-98fafe00-e9ad-11e8-9f84-c85a504f65f2.png)
![](https://user-images.githubusercontent.com/42515875/48600219-64d40d00-e9ae-11e8-83c7-a2d362b62c12.png)
위의 주소로 입력을 주면 ```$_GET['name']```으로 param값을 받을 수 있다.
param값을 2개 이상 받을 경우엔 **"&"** 을 이용한다.
<br>
> 127.0.0.1/index.php**?name=kakao&age=13
