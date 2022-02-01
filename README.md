# Javascript
> <script> 태그를 이용하면 자바스크립트 프로그램을 HTML 문서 대부분의 위치에 삽입할 수 있습니다. <br><br>
> 
#### 외부 스크립트 
> 자바스크립트 코드의 양이 많은 경우엔, 파일로 소분하여 저장할 수 있습니다. <br>
> 이렇게 분해해 놓은 각 파일은 src 속성을 사용해 HTML에 삽입합니다 <br> 
>   ## :warning:  <br>
>  * src 속성이 있으면 태그 내부의 코드는 무시됩니다. <br>
> * <script> 태그는 src 속성과 내부 코드를 동시에 가지지 못합니다. <br>
>  
>  ```c
> <script src="file.js">
>      alert(1); // src 속성이 사용되었으므로 이 코드는 무시됩니다.
> </script>
> ``` 
> <br>   
> 
> #### 세미콜론 
> 줄 바꿈이 있다면 세미콜론(semicolon)을 생략할 수 있습니다. <br>
> 아래 코드는 에러 없이 동작합니다.
>  ```c
> alert('Hello')
> alert('World')
> ```
>  <br>
>
> #### 변수
> * var는 let과 거의 동일하게 동작합니다. var도 let처럼 변수를 선언하는 데 쓰이죠. 다만 var는 ‘오래된’ 방식입니다. <br>
> * 여러 단어를 조합하여 변수명을 만들 땐 카멜 표기법(camelCase)가 흔히 사용됩니다. 카멜 표기법은 단어를 차례대로 나열하면서 첫 단어를 제외한 각 단어의 첫 글자를 대문자로 작성합니다. myVeryLongName같이 말이죠. 
> <br>
>  
> #### 상수
> * 변화하지 않는 변수를 선언할 땐, let 대신 const를 사용합니다. <br>
> * const로 선언한 변수를 '상수(constant)'라고 부릅니다. 상수는 재할당할 수 없으므로 상수를 변경하려고 하면 에러가 발생합니다.
> ```c
> const myBirthday = '18.04.1982';
> myBirthday = '01.01.2001'; // error, can't reassign the constant!
> ```  
> <br>
>
> #### undefined 값
> * undefined 값도 null 값처럼 자신만의 자료형을 형성합니다.
> * undefined는 '값이 할당되지 않은 상태’를 나타낼 때 사용합니다.
> * 변수는 선언했지만, 값을 할당하지 않았다면 해당 변수에 undefined가 자동으로 할당됩니다.
> ```c
> let age;
> alert(age); // 'undefined'가 출력됩니다.
> ``` 
> <br>
> 
> #### typeof 연산자
> * typeof 연산자는 인수의 자료형을 반환합니다. 자료형에 따라 처리 방식을 다르게 하고 싶거나 변수의 자료형을 빠르게 알아내고자 할 때 유용합니다.
> * typeof 연산자는 두 가지 형태의 문법을 지원합니다.
> 1. 연산자: typeof x
> 2. 함수: typeof(x) <br>
> 괄호가 있든 없든 결과가 동일합니다. <br>
> typeof x를 호출하면 인수의 자료형을 나타내는 문자열을 반환합니다.
> ```c
> ypeof undefined // "undefined"
>
> typeof 0 // "number"
>
> typeof 10n // "bigint"
>
> typeof true // "boolean"
> 
> typeof "foo" // "string"
>
> typeof Symbol("id") // "symbol"
>
> typeof Math // "object"  (1)
>
> typeof null // "object"  (2)
>
> typeof alert // "function"  (3)
> ``` 