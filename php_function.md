> var_dump(); 
<br>

괄호 안에 들어가는 값은 타입과 문자 개수를 나타내준다.

![](https://user-images.githubusercontent.com/42515875/48656079-67dd0500-ea63-11e8-93f8-b764e56af9b0.png)

<br>

> file_get_contents("파일경로".$GET['parameter값']);
<br>


파일경로에 있는 $GET['parameter값'] 이름을 가진 파일 내용을 출력한다.
<br>

![](https://user-images.githubusercontent.com/42515875/48656141-4c262e80-ea64-11e8-9bac-b37dbe06f8c3.png)


<br>



> isset(확인할 변수명);

<br>


![](https://user-images.githubusercontent.com/42515875/48656209-2fd6c180-ea65-11e8-83af-ebae03d0a092.png)

<br>


isset()함수는 변수에 값이 **있고 없음**을 불리언(boolean)값으로 반환해주며 만약 갑이 존재하며 null값이 아니라면 **true**를 반환한다. 


<br>

> empty(확인할 변수명);


<br>

empty()함수는 존재하는 값이 없거나 변수의 값이 0 또는 false, null값일 경우에는 true를 반환한다.


<br>

> scandir('data');

<br>


디렉토리 정보, 즉 엔트리(Entry)를 얻고자 할때의 방법은 몇 가지있습니다. <br>
dir클레스를 이용하거나 readdir, scandir을 이용하는 것입니다.

<br>


```
<?php
  $list = array('a','b','c','d');
  $array = scandir($list);
  var_dump($array);
?>


 결과: 
 array ( 
  0 => '.', 
  1 => '..', 
  2 => 'Mail', 
  3 => 'Mail.php', 
  4 => 'package.xml', 
  5 => 'PEAR.php', 
  6 => 'tests', 
 ) 
 */ 

```

<br>

> file_put_content(파일명, 내용);

<br>
파일이 있으면 그 안에 내용을 넣고, 파일이 없으면 파일을 생성한다.

<br>


```
<?php
  file_put_content(파일명, 내용);
?>
```









