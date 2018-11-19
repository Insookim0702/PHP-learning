## PHP 사용자 정의 함수 - PHP User Defined Functions
내장된 php함수 이외에 사용자가 정의하는 함수 <br>
함수의 **호출**에 의해 실행된다. <br>

### Syntax
<br>

```
<?php
function functionName($arg_1, $arg_2,.... ){
  echo "fun함수를 사용해서 출력됨.";
}

functionName();  //함수 호출
?>


결과
fun함수를 사용해서 출력됨.
```

## PHP 함수 인수(Arguments)
인수를 통해서 함수에 정보가 전달 될 수 있다. <br>

','를 사용해서 Arguments를 여러 개 넣을 수 있다. <br>

```
<?php
function funcTest($name){
  echo "welcome $name.\n"; 
}

funcTest("Alice");

?>


결과
welcome Alice
```

## PHP Function - returning values
```
<?php
function sum($r, $e){
  $z = $r + $e;
  return $z;
}

echo "4 +10 = ".sum(4,10)."<br>"; 
?>
```

<br>

#### PHP의 모든 함수와 클래스는 전역입니다. 함수가 내부에서 정의되어도 외부에서 호출할 수 있다.

#### PHP는 함수오버로딩을 지원하지 않는다. 함수 정의를 해제하거나 이미 선언된 함수를 다시 선언할 수 없다.
