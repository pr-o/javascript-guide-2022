# 변수와 상수

## 변수 (Variable)

변수는 값을 저장할 수 있는 컨테이너입니다. 변수를 선언할 때에는 `var` 또는 `let` 키워드 뒤에 변수의 이름을 지정하면 됩니다.

```jsx
var myColor;
let myJob;
```



변수를 선언한 후에, 다음과 같이 값을 할당할 수 있습니다.

```jsx
myColor = 'teal';
myJob = 'developer';
```



혹은 변수의 선언과 동시에 값을 할당할 수도 있습니다.

```jsx
var myColor = 'teal';
let myJob = 'developer';
```



이미 값이 할당된 변수에 새로운 값을 재할당해 변수의 값을 변경할 수도 있습니다.

```jsx
myColor = 'pink';
myJob = 'singer';
```



## 상수 (Constant)

상수는 변수와 달리 변하지 않는 값을 저장하는 컨테이너입니다. 상수를 선언할 때엔 `const` 키워드와 변수 이름 뒤에 초기값을 지정해야만 합니다. 상수의 값은 재할당을 통해 변경할 수 없습니다.

```jsx
const pi = 3.1415;
```



다음과 같이 상수 선언시에 초기값을 생략한 경우, 상수의 재할당을 시도하는 경우엔 에러가 발생합니다.

```jsx
const pi;    // * Uncaught SyntaxError: Missing initializer in const declaration
pi = 100;    // * Uncaught TypeError: Assignment to constant variable
```
