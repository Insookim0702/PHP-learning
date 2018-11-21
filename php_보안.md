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
- 악성사용자로부터 XSS공격을 방지할 수 있다.
- 변환문자
<br>

 특수문자   | 변환문자  
---|---
  &(앰퍼샌드) | \&amp;
 ""(겹따옴표)  |  \&quot;  
 ''(홑따옴표)   | \&#039; 
  \<(미만)  |  \&lt;
 \>(이상)  |    \&gt;



htmlspecialchars()는 특수문자를 HTML entitles로 변환한다. <, >같은 HTML문자를 **$lt;**과 **&gt;**로 바꾸는 것을 말한다.
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

PHP_SELF가 내 페이지에서 사용되면, 사용자는 \/를 xxs명령을 입력할 수 있다.
Cross-site scripting(xss)은 웹 응용프로그램에서 쉽게 사용되는 악성 공격이다.

xxs는 공격자들이 웹페이지에 클라이언트측 스크립트를 주입하는 것을 가능하게 해준다.
