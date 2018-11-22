# PHP Form Validation

```
Name:<input type="text" name="name>
web:<input type="text" name="web>
```

## Radio Buttons
```
Gender:
<input type="radio" name="gender" value="female"> Female
<input type="radio" name="gender" value="male"> Male
```

## Form PHP형식
```
<form method="post" action="<?php echo htmlspecialchars($_SERVER["PHP_SELF"]);?>">
```

## $_SERVER["PHP_SELF"] 변수 무엇?
$_SERVER["PHP_SELF"]는 슈퍼전역변수이다. 현재 실행중인 스크립트의 파일이름을 변환한다.
<br>

$_SERVER["PHP_SELF"]는 다른 페이지로 이동하는 대신에, 페이지 자신에 제출한 form 데이터를 전송한다. 사용자는 form과 같은 페이지에 에러 메시지를 갖는다.

## htmlspecialchars()함수 무엇?
- htmlspecialchars()는 특수문자를 HTML entitles로 변환한다. <, >같은 HTML문자를 **$lt;**과 **&gt;** 등으로 바꾸는 함수이다.
- 악성사용자로부터 XSS공격을 방지할 수 있다.
<br>
> 사이트 간 스크립팅 (Cross-site scripting) XSS
> 웹어플리케이션에서 많이 나타나는 취약점이다.
> 웹사이트 관리자가 아닌 해커가 웹 페이지에 악성 스크립트를 삽입할 수 있는 취약점이다.
> 이 취약점으로 해커는 사용자의 정보(cookie, session)를 탈취하거나, 자동으로 비정상적인 기능을 수행하게 한다.
> xxs는 공격자들이 웹페이지에 클라이언트측 스크립트를 주입하는 것을 가능하게 해준다.

<br>

- 변환문자
<br>

 특수문자   | 변환문자  
---|---
  &(앰퍼샌드) | \&amp;
 ""(겹따옴표)  |  \&quot;  
 ''(홑따옴표)   | \&#039; 
  \<(미만)  |  \&lt;
 \>(이상)  |    \&gt;

<br>

URL이 www.exp.com/test.php 의 페이지에 다음과 같은 폼이있다.
```
<form method="post" action="<?php echo $_SERVER['PHP_SELF'];?>">

정상적으로 해석되면
<form method="post" action="test.php">
```
<br>



```
<?php

$tor = htmlspecialchars("<a href="index">Test</a>". ENT_QUOTES);

echo $tor;

결과
$tl;a href=&#039;index&#039;&gt;index&lt;/a&gt;
```
<br>
악용으로 form으로 HTML이나 JavaScript코드를 xxs(Cross-site Scripting attacks)주입하는 공격자를 방지할 수 있다.
<br>

## PHP로 form 데이터 유효성 검사
1. 모든 입력받는 변수는 PHP의 **htmlspecialchars()** 함수로 전달한다.
xss공격을 할 때 script코드입력을 막기 위해서 htmlspecialchars()는 유효하다.

2. PHP의 **trim()함수** 사용 - 사용자가 입력한 데이터에서 불필요한 문자(space, tab, newline)등을 제거한다.
3. PHP의 **stripslashes()함수** 사용 - 사용자가 입력한 값중에 backslash(\\)를 제거한다.


