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
> * 역 따옴표(백틱, backtick) : `Hello` <br>
>       역 따옴표로 변수나 표현식을 감싼 후 ${…}안에 넣어주면, 아래와 같이 원하는 변수나 표현식을 문자열 중간에 손쉽게 넣을 수 있습니다. <br>
> 
>  ```c
> let name = "John";
> 
> // 변수를 문자열 중간에 삽입
> alert( `Hello, ${name}!` ); // Hello, John!
>
> // 표현식을 문자열 중간에 삽입
> alert( `the result is ${1 + 2}` ); // the result is 3
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
> <br>
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
> <br>
>
> #### null 값
> * null 값은 지금까지 소개한 자료형 중 어느 자료형에도 속하지 않는 값입니다.
> * null 값은 오로지 null 값만 포함하는 별도의 자료형을 만듭니다.
> * null의 typeof 연산은 "object"인데, 이는 언어상 오류입니다. null은 객체가 아닙니다.
>
> <br><br>
>
> - 객체(object)형은 특수한 자료형입니다.
> 객체형을 제외한 다른 자료형은 문자열이든 숫자든 한 가지만 표현할 수 있기 때문에 원시(primitive) 자료형이라 부릅니다. 반면 객체는 데이터 컬렉션이나 복잡한 개체(entity)를 표현할 수 있습니다. <br>
> - 심볼(symbol)형은 객체의 고유한 식별자(unique identifier)를 만들 때 사용됩니다. 
> 
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
>
> <br> <br>
>
> #### alert
> * alert 함수는 앞선 예제에서 살펴본 바 있습니다. 이 함수가 실행되면 사용자가 ‘확인(OK)’ 버튼을 누를 때까지 메시지를 보여주는 창이 계속 떠있게 됩니다.
>
> <br> <br>
>
> #### prompt
> * 브라우저에서 제공하는 prompt 함수는 두 개의 인수를 받습니다.
> * 함수가 실행되면 텍스트 메시지와 입력 필드(input field), 확인(OK) 및 취소(Cancel) 버튼이 있는 모달 창을 띄워줍니다.
> * title : 사용자에게 보여줄 문자열 <br>
> * default : 입력 필드의 초깃값(선택값) <br>
> * 인수를 감싸는 대괄호 [...]의 의미 : default를 감싸는 대괄호는 이 매개변수가 필수가 아닌 선택값이라는 것을 의미합니다.
>
> ```c
> result = prompt(title, [default]);
> ``` 
> <br>
>
> * prompt 함수는 사용자가 입력 필드에 기재한 문자열을 반환합니다. 사용자가 입력을 취소한 경우는 null이 반환됩니다.
>
> ```c
> let age = prompt('나이를 입력해주세요.', 100);
>
> alert(`당신의 나이는 ${age}살 입니다.`); // 당신의 나이는 100살입니다.
> ``` 
>
> :warning: Internet Explorer(IE)에서는 항상 '기본값’을 넣어주세요. <br>  
> IE 사용자를 비롯한 모든 사용자에게 깔끔한 프롬프트를 보여주려면 아래와 같이 두 번째 매개변수를 항상 전달해 줄 것을 권장합니다.
> 

