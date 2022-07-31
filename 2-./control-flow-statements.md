# 제어문 (Control Flow Statements)

경우에 따라 코드의 순차적인 흐름을 제어해야할 때 사용하는 명령문을 제어문이라고 합니다.



## 조건문 (Conditional Statements)

특정 조건, 경우에 따라 다른 동작을 수행하고 싶을 때 조건문을 사용합니다.

### if 문

조건의 결과가 `true`인 경우 주어진, 중괄호 안의 명령문을 실행하고, `false`인 경우 실행하지 않습니다.

```jsx
let w = 92;
if (w < 100) {
  console.log('smaller than 100')
};
```



### if… else 문

```jsx
let testScore = 85;
if (testScore > 79) {
  console.log('PASS');
} else {
  console.log('FAIL');
};
```



### if… else if… else 문

```jsx
let age = 20;
if (age <= 2) {
  console.log('toddler');
} else if (age <= 12) {
  console.log('child');
} else if (age <= 18) {
  console.log('adolescent');
}
```



### switch… case 문

주어진 조건의 값을 `case` 레이블의 값과 비교해 일치하는 `case`의 명령문을 실행합니다.

```jsx
const color = 'teal';

switch (color) {
  case 'red':
    console.log('#FF0000');
    break;
  case 'green':
    console.log('#00FF00');
    break;
  case 'blue':
    console.log('#0000FF');
    break;
  case 'teal':
    console.log('#008080');
    break;
}
```

`break`는 `case`의 명령문을 실행한 후에 `switch`문을 탈출해 다음 명령문을 실행할 수 있도록 합니다.



## 반복문

특정 명령문을 반복적으로 실행하기 위해 사용합니다.

### while

조건을 만족하는 동안 코드를 반복실행합니다.

```jsx
let i = 0;

while (i < 5) {
  console.log(i);
  i++;
}
```



`i`의 초기값은 0이므로, 조건인 `i < 5` 가 참인 동안 4\~5번 라인의 코드가 반복실행됩니다. 5번 라인의 증가연산자(`++`)에 의해 `i`가 증가하게 되면서 5보다 작지 않을때 `while` 반복문을 탈출하게 됩니다.



### for

`while` 반복문의 예제에서 보았듯이 반복문에는 대부분 초기화식과 조건식 그리고 증감식이 존재합니다.

{% hint style="info" %}
초기화식: `let i = 0;` 조건식: `i < 5` 증감식: `i++`
{% endhint %}

이런 경우엔 `for` 반복문을 이용해 코드를 좀 더 간편하고 짧게 구성할 수 있습니다. 다음 예제는 위의 예제와 완전히 똑같이 작동합니다.

```jsx
for (let i = 0; i < 5; i++) {
  console.log(i)
}
```



`for` 키워드를 뒤따르는 소괄호 안에 초기화식, 조건식, 증감식 순서대로 세미콜론(`;`)으로 구분지어 정의한다고 이해하면 좋습니다.



### for … in

객체의 모든 열거할 수 있는 속성들을 순차적으로 접근하며 코드를 반복실행할 수 있습니다.

```jsx
const movie = {
	title: 'The Curious Case of Benjamin Button',
	director: 'David Fincher',
	writer: 'Eric Roth',
	releaseYear: 2008,
};

for (let key in movie) {
	console.log(key + ': ' + movie[key]);
};
```



### for … of

주로 배열의 항목들을 순회하며 코드를 반복실행할 수 있습니다.

```jsx
const odd = [1, 3, 5, 7, 9];
for (let number of odd) {
	console.log(number);
};
```

####

이 외에도 `while` 문 그리고 `do... while` 문 등이 있습니다.

