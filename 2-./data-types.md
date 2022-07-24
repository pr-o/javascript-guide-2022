# 자료형 (Data Types)

자바스크립트 자료형은 크게 원시값과 객체로 나뉩니다. 이 중에서 가장 기본적이고 이 튜토리얼에서 사용하게 될 자료형들만 알아보겠습니다.

* 원시값 (Primitive values)
  * Boolean
  * Null
  * Undefined
  * Number
  * BigInt
  * String
  * Symbol
* 객체 (Object)

## Boolean

논리 요소를 표현하며, `true` 혹은 `false` 두 가지의 값을 가질 수 있습니다.

```jsx
const horse = true;
const unicorn = false;
```

## Null

`null` 하나의 값만 가질 수 있습니다. 비어있는 값을 표현합니다. 어떤 값이 의도적으로 비어있음을 표현합니다.

```jsx
let emailA = null;
```

> A는 본인의 이메일을 공개하지 않겠답니다. 그러므로 우리에겐 A의 이메일이 없습니다. 이 사실을 코드에 반영하자면 A의 이메일을 저장하는 변수에 `null`을 할당하는 것이 최선입니다.

## Undefined

`undefined` 하나의 값만 가질 수 있습니다. 존재하지 않는 값을 표현합니다. 선언한 후 값을 할당하지 않은 변수에 자동으로 할당됩니다.

```jsx
let emailB = undefined;
let emailC;    // emailC의 값은 undefined로 자동 할당
```

> B와 C는 이메일이 없다고 합니다. 태어나서 한번도 사용한적이 없고 급한 연락이 필요할때엔 전서구와 봉화를 이용한다고 합니다. 이 사실을 코드에 반영하자면 B의 이메일을 저장하는 변수에 `undefined`를 할당하는 것이 최선입니다.

`null`과 `undefined`의 차이점이 모호하게 느껴질 수 있습니다. `0`, `null`, `undefined` 셋을 설명하는 아래의 이미지를 보고 위의 예시를 다시 한번 읽어보시는 것을 추천합니다.

![Stefan Baumgartner's Twitter](<../.gitbook/assets/DusCOfyXcAA9\_F7 (1).jpeg>)

## Number

\-(2^53 − 1)부터 2^53 − 1까지의 수를 표현합니다. 2^53는 약 9천조입니다.

```jsx
const pi = 3.1415;
let price = 5000;
```

## String

문자열이라고도 부르는 텍스트 데이터를 표현합니다. 작은 따옴표나 큰 따옴표로 묶어야 합니다. 그렇지 않으면 다른 변수의 값을 할당하게 됩니다.

```jsx
const hello = 'Hello, ';
const js = "JavaScript";
hello + js;    // Hello, javascript
```
