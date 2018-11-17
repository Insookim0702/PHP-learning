## 배열 가즈아~

```
<?php
  $array = array('1','2','3','4','5');
  echo $array[1]   // =>2출력
  echo $array[3]   // =>4출력
  echo count($array);   //  =>5 출력
  echo var_dump(count($array));   // =>int(5) 출력
?>
```
<h1> 배열에 사용하는 php 함수.</h1>
<ol>
  <li> count($배열변수);   - 배열 원소의 개수를 출력한다.
  <li> array_push($배열변수, '삽입할 값'); - array를 스택으로 취급, array 끝에 변수를 넣는다.
  <li> array_pop(); - 배열의 마지막 원소 빼내기.
  
</ol>
