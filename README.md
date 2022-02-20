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
> <br>
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
> * 프롬프트 함수의 두 번째 매개변수는 선택사항이지만, 이 매개변수가 없는 경우 IE는 "undefined"를 입력 필드에 명시합니다. <br>
> * IE 사용자를 비롯한 모든 사용자에게 깔끔한 프롬프트를 보여주려면 아래와 같이 두 번째 매개변수를 항상 전달해 줄 것을 권장합니다.
> ```c
> let test = prompt("Test", ''); // <-- IE 사용자를 위한 매개변수 처리
> ``` 
>
> <br>
> <br>
> 
> #### 컨펌 대화상자
> ```c
> result = confirm(question);
> ``` 
> confirm 함수는 매개변수로 받은 question(질문)과 확인 및 취소 버튼이 있는 모달 창을 보여줍니다. <br>
> 사용자가 확인버튼를 누르면 true, 그 외의 경우는 false를 반환합니다.
> 
> ```c
> let isBoss = confirm("당신이 주인인가요?");
>
> alert( isBoss ); // 확인 버튼을 눌렀다면 true가 출력됩니다.
> ``` 
> 
> <br>
> <br>
> 
> #### 문자형으로 변환
> * 문자형으로의 형 변환은 문자형의 값이 필요할 때 일어납니다. <br>
> * alert메서드는 매개변수로 문자형을 받기 때문에, alert(value)에서 value는 문자형이어야 합니다. 만약, 다른 형의 값을 전달받으면 이 값은 문자형으로 자동 변환됩니다. <br>
> * String(value) 함수를 호출해 전달받은 값을 문자열로 변환 할 수도 있습니다. <br>
> 
> ```c
> let value = true;
> alert(typeof value); // boolean
>
> value = String(value); // 변수 value엔 문자열 "true"가 저장됩니다.
> alert(typeof value); // string
> ``` 
> false는 문자열 "false"로, null은 문자열 "null"로 변환되는 것과 같이, 문자형으로의 변환은 대부분 예측 가능한 방식으로 일어납니다. <br>
> 
> <br> <br>
>
> #### 숫자형으로 변환
> 숫자형으로의 변환은 수학과 관련된 함수와 표현식에서 자동으로 일어납니다.
> ```c
> alert( "6" / "2" ); // 3, 문자열이 숫자형으로 자동변환된 후 연산이 수행됩니다.
> ```
> <br>
>
> Number(value) 함수를 사용하면 주어진 값(value)을 숫자형으로 명시해서 변환할 수 있습니다.
> 
> ```c
> let str = "123";
> alert(typeof str); // string
>
> let num = Number(str); // 문자열 "123"이 숫자 123으로 변환됩니다.
>
> alert(typeof num); // number
> ```
> 숫자형 값를 사용해 무언가를 하려고 하는데 그 값을 문자 기반 폼(form)을 통해 입력받는 경우엔, 이런 명시적 형 변환이 필수입니다.
> 
> <br>
>
> ```c
> let age = Number("임의의 문자열 123");
> 
> alert(age); // NaN, 형 변환이 실패합니다.
> ```
> 숫자 이외의 글자가 들어가 있는 문자열을 숫자형으로 변환하려고 하면, 그 결과는 NaN이 됩니다.
> 
> <br>
>
> ##### 예시
> ```c
> alert( Number("   123   ") ); // 123
> alert( Number("123z") );      // NaN ("z"를 숫자로 변환하는 데 실패함)
> alert( Number(true) );        // 1
> alert( Number(false) );       // 0
> ```
> null과 undefined은 숫자형으로 변환 시 결과가 다르다는 점에 유의.
> null은 0이 되고 undefined는 NaN이 됩니다.
>
> <br> <br>
>
> #### 불린형으로 변환
> Boolean(value)를 호출하면 명시적으로 불리언으로의 형 변환을 수행할 수 있습니다. <br>
> 불린형으로 변환 시 적용되는 규칙은 다음과 같습니다. 
> * 숫자 0, 빈 문자열, null, undefined, NaN과 같이 직관적으로도 “비어있다고” 느껴지는 값들은 false가 됩니다.
> * 그 외의 값은 true로 변환됩니다.
> ```c
> alert( Boolean(1) ); // 숫자 1(true)
> alert( Boolean(0) ); // 숫자 0(false)
>
> alert( Boolean("hello") ); // 문자열(true)
> alert( Boolean("") ); // 빈 문자열(false)
> ```
> ###### :warning: 주의: 문자열 "0"은 true입니다.
> PHP 등의 일부 언어에선 문자열 "0"을 false로 취급합니다. 그러나 자바스크립트에선 비어 있지 않은 문자열은 언제나 true입니다.
> ```c
> alert( Boolean("0") ); // true
> alert( Boolean(" ") ); // 공백이 있는 문자열도 비어있지 않은 문자열이기 때문에 true로 변환됩니다.
> ```
> 
> <br> <br> 
>
> #### ‘단항’, ‘이항’, ‘피연산자’
> * 피연산자(operand) 는 연산자가 연산을 수행하는 대상입니다. 5 * 2에는 왼쪽 피연산자 5와 오른쪽 피연산자 2, 총 두 개의 피연산자가 있습니다. '피연산자’는 '인수(argument)'라는 용어로 불리기도 합니다. <br> 
> * 피연산자를 하나만 받는 연산자는 단항(unary) 연산자 라고 부릅니다. 피연산자의 부호를 뒤집는 단항 마이너스 연산자 -는 단항 연산자의 대표적인 예입니다.
> ```c
> let x = 1;
>
> x = -x;
> alert( x ); // -1, 단항 마이너스 연산자는 부호를 뒤집습니다.
> ```
> 
> <br>
>  
> #### 거듭제곱 연산자 **
> 거듭제곱 연산자(exponentiation operator)를 사용한 a ** b를 평가하면 a를 b번 곱한 값이 반환됩니다.
> ```c
> alert( 2 ** 2 ); // 4  (2 * 2)
> alert( 2 ** 3 ); // 8  (2 * 2 * 2)
> alert( 2 ** 4 ); // 16 (2 * 2 * 2 * 2)
> ```
>
> <br> <br>
>
> #### 단항 연산자 +와 숫자형으로의 변환 
> 덧셈 연산자 +는 이항 연산자뿐만 아니라 단항 연산자로도 사용할 수 있습니다. <br>
> 숫자에 단항 덧셈 연산자를 붙이면 이 연산자는 아무런 동작도 하지 않습니다. 그러나 피연산자가 숫자가 아닌 경우엔 숫자형으로의 변환이 일어납니다.
> ```c
> // 숫자에는 아무런 영향을 미치지 않습니다.
> let x = 1;
> alert( +x ); // 1
>
> let y = -2;
> alert( +y ); // -2
>
> // 숫자형이 아닌 피연산자는 숫자형으로 변화합니다.
> alert( +true ); // 1
> alert( +"" );   // 0
> ```
> 단항 덧셈 연산자는 짧은 문법으로도 Number(...)와 동일한 일을 할 수 있게 해줍니다. <br>
> 개발을 하다 보면 문자열을 숫자로 변환해야 하는 경우가 자주 생깁니다. HTML 폼(form) 필드에서 값을 가져왔는데 그 값이 문자형일 때 같이 말이죠. <br>
> 실제로 폼에서 가지고 온 값은 대개 문자열 형태입니다.
> 
> <br> <br>
>
> #### 증가·감소 연산자
> 증가(increment) 연산자 ++는 변수를 1 증가시킵니다.
> ```c
> let counter = 2;
> counter++;      // counter = counter + 1과 동일하게 동작합니다. 하지만 식은 더 짧습니다.
> alert( counter ); // 3
> ```
>
> <br>
>
> 감소(decrement) 연산자 --는 변수를 1 감소시킵니다.
> ```c
> let counter = 2;
> counter--;      // counter = counter - 1과 동일하게 동작합니다. 하지만 식은 더 짧습니다.
> alert( counter ); // 1
> ```
>
> <br> <br>
>
> #### 문자열 비교
> * 자바스크립트는 '사전’순으로 문자열을 비교합니다. '사전편집(lexicographical)'순 이라고 불리기도 하는 이 기준을 적용하면 사전 뒤쪽의 문자열은 사전 앞쪽의 문자열보다 크다고 판단됩니다. <br>
> * 실제 단어를 사전에 실을 때 단어를 구성하는 문자 하나하나를 비교하여 등재 순서를 정하는 것과 같이 자바스크립트도 문자열을 구성하는 문자 하나하나를 비교해가며 문자열을 비교합니다.
> ```c
> alert( 'Z' > 'A' ); // true
> alert( 'Glow' > 'Glee' ); // true
> alert( 'Bee' > 'Be' ); // true
> ```
> <br>
>
> ##### 문자열 비교 시 적용되는 알고리즘은 다음과 같습니다.
> 1. 두 문자열의 첫 글자를 비교합니다.  <br>
> 2. 첫 번째 문자열의 첫 글자가 다른 문자열의 첫 글자보다 크면(작으면), 첫 번째 문자열이 두 번째 문자열보다 크다고(작다고) 결론 내고 비교를 종료합니다. <br>
> 3. 두 문자열의 첫 글자가 같으면 두 번째 글자를 같은 방식으로 비교합니다. <br>
> 4. 글자 간 비교가 끝날 때까지 이 과정을 반복합니다. <br>
> 5. 비교가 종료되었고 문자열의 길이도 같다면 두 문자열은 동일하다고 결론 냅니다. 비교가 종료되었지만 두 문자열의 길이가 다르면 길이가 긴 문자열이 더 크다고 결론 냅니다.
>
> <br> <br>
>
> 동시에 일어나지 않을 법한 두 상황이 동시에 일어나는 경우도 있습니다. <br>
> * 동등 비교(==) 시 true를 반환함 <br>
> * 논리 평가 시 값 하나는 true, 다른 값 하나는 false를 반환함 <br>
> ```c
> let a = 0;
> alert( Boolean(a) ); // false
>
> let b = "0";
> alert( Boolean(b) ); // true
>
> alert(a == b); // true!
> ```
> 두 값(a와 b)을 비교하면 참이 반환되는데, 값을 논리 평가한 후 비교하면 하나는 참, 하나는 거짓이 반환된다는 점에 고개를 갸우뚱할 수도 있습니다. 그런데 자바스크립트 관점에선 이런 결과가 아주 자연스럽습니다. 동등 비교 연산자 ==는 (예시에서 문자열 "0"을 숫자 0으로 변환시킨 것처럼) 피연산자를 숫자형으로 바꾸지만, 'Boolean’을 사용한 명시적 변환에는 다른 규칙이 사용되기 때문입니다.
> #### 일치 연산자
> 동등 연산자(equality operator) ==은 0과 false를 구별하지 못합니다.
> ```c
> alert( 0 == false ); // true
> ```
> 피연산자가 빈 문자열일 때도 같은 문제가 발생
> ```c
> alert( '' == false ); // true
> ```
> 이런 문제는 동등 연산자 ==가 형이 다른 피연산자를 비교할 때 피연산자를 숫자형으로 바꾸기 때문에 발생합니다. 빈 문자열과 false는 숫자형으로 변환하면 0이 되죠.
> ##### 그렇다면 0과 false는 어떻게 구별은?
> 일치 연산자(strict equality operator) ===를 사용하면 형 변환 없이 값을 비교할 수 있습니다. <br>
> 일치 연산자는 엄격한(strict) 동등 연산자입니다. 자료형의 동등 여부까지 검사하기 때문에 피연산자 a와 b의 형이 다를 경우 a === b는 즉시 false를 반환합니다.
> ```c
> alert( 0 === false ); // false, 피연산자의 형이 다르기 때문입니다.
> ```
