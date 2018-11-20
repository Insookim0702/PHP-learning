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
if($_SERVER["REQUEST_METHOD"] =="POST"){
  if(empty($name)){
      echo "Name is empty";
  } else{
      echo $_REQUEST['fname'];
  }
}
?>

</body>
</html>
```

### $_POST
PHP $_POST는 HTML form이 method="post"로 제출되었을 때 form 데이터를 수집하는데 널리 사용된다.<br>
$_POST는 또한 변수를 전달할 때도 널리 사용된다.<br>

form태그를 사용하면 사용자가 submit버튼을 눌러 데이터를 제출하면, 폼 데이터는 <form>태그의 action 속성에 지정된 파일로 보내진다.
form데이터를 처리하기 위해 이 **파일자신-> $_SERVER['PHP_SELF']**를 지정한다.
  
```
<html>
<body>
<form method="post" action="<?php echo $_SERVER['PHP_SELF']?>">
name : <input type="text" name="fname">
<input type="submit">
</form>

<?php
  $name=$_POST['fname'];
  echo $name;
?>
```

### $_GET
```
<html>
<body>
<a href="test_get.php?subject=PHP&web=W3schools.com">Test$GET</a>

<?php
    echo "subject:".$_GET['subject']."  web : ".$_GET['web'];
?>
```



## GET vs POST

