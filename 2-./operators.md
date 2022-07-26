# 연산자 (Operators)

말그대로 두 값으로무터 결과를 만들어내는 기호입니다.



## 산술 연산자

### 더하기 연산자

두 수를 더하거나, 문자열을 하나로 붙입니다.

```jsx
5 + 10;
"Hello, " + "world!";
```

### 빼기, 곱하기, 나누기, 나머지 연산자

기초수학에서와 동일하게 동작합니다

```jsx
10 - 7;    // 3
12 * 3;    // 9
40 / 5;    // 8
10 % 4;    // 2
```

### 증가 및 감소 연산자

증가 연산자 `++`는 피연산자 변수에 1을 더해주고 감소 연산자 `--`는 1을 빼줍니다. 두 증감 연산자는 변수의 앞에 위치할때와 뒤에 위치할때의 동작 방식이 살짝 다릅니다. 변수 뒤에 위치할 경우엔 해당 라인의 코드가 실행된 후에 증감이 일어나고, 앞에 위치할 경우엔 실행 전에 증감이 일어납니다. 이 동작은 아래의 예시 코드에서 확인할 수 있습니다.

```jsx
let a = 1
console.log(a++)    // 1
console.log(++a)    // 3

let b = 5
console.log(b--)    // 5
console.log(--b)    // 3
```

## 할당 연산자

값을 우변 피연산자의 값에 따라 좌변 피연산자에 할당합니다.

### 할당 연산자

```jsx
let k = 2
```

### 덧셈, 뺄셈 할당 연산자

```jsx
k += 3    // 5
k -= 4    // 1
```

### 곱셈, 거듭제곱 할당 연산자

```jsx
k *= 5     // 5
k **= 2    // 25
```

### 나눗셈, 나머지 할당 연산자

```jsx
k /= 5    // 5
k %= 4    // 1
```



## 비교 연산자

두 값이 서로 같은지 테스트하여 결과를 `true` 혹은 `false`를 반환합니다.

```jsx
let p = 100;
p === 99;
k **= 2;    // 25
```

### 동등 연산자

왼쪽과 오른쪽 피연산자의 값이 같으면 `true`를 반환합니다.

```jsx
let p = 100;
p == 100;      // true
p == '100';    // true
```

### 일치 연산자

왼쪽과 오른쪽 피연산자의 값이 같고, 같은 타입이면 `true`를 반환합니다.

```jsx
let p = 100;
p === 100;      // true
p === '100';    // false
```



{% hint style="info" %}
**동등 연산자 vs. 일치 연산자**\
동등 연산자(==, equal)와 일치 연산자(===, strict equal)는 모두 두 개의 피연산자가 서로 같은지를 비교해 줍니다. 두 연산자 모두 피연산자의 타입을 가리지는 않지만, 그 같음을 정의하는 기준이 조금 다릅니다. 동등 연산자(==)는 두 피연산자의 값이 서로 같으면 참(true)을 반환합니다. 이때 두 피연산자의 타입이 서로 다르면, 비교를 위해 강제로 타입을 같게 변환합니다. 하지만 일치 연산자(===)는 타입의 변환 없이 두 피연산자의 값이 같고, 타입도 같아야만 참(true)을 반환합니다.


{% endhint %}

### 부등 연산자

왼쪽과 오른쪽 피연산자의 값이 같지 않으면 `true`를 반환합니다.

```jsx
let p = 100;
p != 99;    // true
```

### 불일치 연산자

왼쪽과 오른쪽 피연산자의 값이 같지 않거나, 다른 타입이면 `true`를 반환합니다.

```jsx
let p = 100;
p !== 100;      // false
p !== '100';    // true
```

### 비교 연산자

왼쪽과 오른쪽 피연산자의 관계가 부등기호와 일치할 경우 `true`, 아닐 경우 `false`를 반환합니다.

```jsx
let p = 100;
p < 101;    // true
p > 100;    // false

p <= 101;    // true
p >= 101;    // false
```



## 논리 연산자

주어진 논리식을 판단하여, `true` 혹은 `false`을 반환합니다.

### 논리부정 (Logical NOT)

```jsx
!true;     // false
!false;    // true
```

### 논리 (Logical AND)

```jsx
true && true;      // true
true && false;     // false
false && true;     // false
false && false;    // false
```

### 논리 (Logical OR)

```jsx
true || true;      // true
true || false;     // true
false || true;     // true
false || false;    // false
```

### 삼항 연산자 (Ternary Operator)

주어진 조건에 따라 두 값 중 하나를 반환하고 구문은 다음과 같습니다:

```jsx
condition ? valueA : valueB;
```

조건인 `condition`이 참이라면 연산자는 `valueA`를 반환하고, 그렇지 않다면 `valueB`를 반환합니다. 예를 들어 다음과 같이 사용할 수 있습니다. `score`가 80 이상이라면 `result` 변수에 “PASS”를, 그렇지 않으면 “FAIL”을 할당합니다.

```jsx
const result = score > 79 ? 'PASS' : 'FAIL';
```



## 제어문 (Control Flow Statements)

경우에 따라 코드의 순차적인 흐름을 제어해야할 때 사용하는 명령문을 제어문이라고 합니다.

### 조건문 (Conditional Statements)

특정 조건, 경우에 따라 다른 동작을 수행하고 싶을 때 조건문을 사용합니다.

#### if 문

조건의 결과가 `true`인 경우 주어진, 중괄호 안의 명령문을 실행하고, `false`인 경우 실행하지 않습니다.

```jsx
let w = 92;
if (w < 100) {
	console.log('smaller than 100')
};
```

#### if… else 문

```jsx
let testScore = 85;
if (testScore > 79) {
	console.log('PASS');
} else {
	console.log('FAIL');
};
```

#### if… else if… else 문

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

#### switch… case 문

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

`break`는 `case`의 명령문을 실행한 후에 `switch`문을 탈출해 다음 명령문을 실행할 수 있게합니다

### 반복문

특정 명령문을 반복적으로 실행하기 위해 사용합니다.

#### while

조건을 만족하는 동안 코드를 반복실행합니다.

```jsx
let i = 0;

while (i < 5) {
	console.log(i);
  i++;
}
```

`i`의 초기값은 0이므로, 조건인 `i < 5` 가 참인 동안 4\~5번 라인의 코드가 반복실행됩니다. 5번 라인의 증가연산자(`++`)에 의해 `i`가 증가하게 되면서 5보다 작지 않을때 `while` 반복문을 탈출하게 됩니다.

#### for

`while` 반복문의 예제에서 보았듯이 반복문에는 대부분 초기화식과 조건식 그리고 증감식이 존재합니다.

> 초기화식: `let i = 0;` 조건식: `i < 5` 증감식: `i++`

이런 경우엔 `for` 반복문을 이용해 코드를 좀 더 간편하고 짧게 구성할 수 있습니다. 다음 예제는 위의 예제와 완전히 똑같이 작동합니다.

```jsx
for (let i = 0; i < 5; i++) {
	console.log(i)
}
```

`for` 키워드를 뒤따르는 소괄호 안에 초기화식, 조건식, 증감식 순서대로 세미콜론(`;`)으로 구분지어 정의한다고 이해하면 좋습니다.

#### for … in

#### for … of

####

이 외에도 `while` r그리고 `do... while` 문 등이 있습니다.
