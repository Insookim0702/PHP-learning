## PHP Global Variables - superglobals

superglobals는 PHP안에 미리 정의되어 있는 몇몇 변수들이며, 어떤 함수, 클래스 그리고 파일에 바로 사용할 수 있다. 범위와 상관없이 항상 접근이 가능하다.

### PHP Superglobals(전역변수)
- $_REQUEST
- $_GET
- $_POST
- $_SESSION
- $_COOKIE
- $_FILES
- $_SERVER

### $_SERVER

- $_SERVER['PHP_SELF'] : return the **filename** of the currently executing script
- $_SERVER['SERVER_ADDR'] : Return the **IP address** of the host sever

### $_REQUEST
PHP $_REQUEST는 HTML form을 제출한 다음 데이터를 수집하는데 사용한다.<br>
input필드와 submit버튼을 갖는 form을 사용해서 사용자가 submit버튼을 누르면 데이터가 제출된다. <br>
form 데이터는 <form>태그에 action속성에 지정된 파일로 보내진다. <br>

input필드 값을 수집하는데 superglobals변수 **$_REQUEST** 를 사용할 수 있다.
```
<html>
<body>

<form method="post" action="<?php echo $_SERVER['PHP_SELF'];?>">
Name: <input type="text" name="fname">
<input type="submit">

</form>

<?php
$name = $_REQUEST['fname'];
echo $name;
?>

</body>
</html>
```
