# Hoisting

자바스크립트는 변수 선언과 함수 선언을 위로 끌어올린다.

### 예시

```js
console.log(a());

function a() {
  return "a";
}
```

위의 코드는 a를 선언하고 정의하기 전에 a를 실행시켰는데 오류가 나지 않는다.<br>
왜냐하면, 자바스크립트는 변수 선언과 함수 선언을 위로 끌어올리고 나서 실행시키기 때문이다.
<br><br>
따라서, 위의 코드는 아래와 같이 변하고 실행이 된다.

```js
function a() {
  return "a";
}

console.log(a());
```

<br>
하지만, 아래의 경우에는 에러가 발생한다.

```js
console.log(b());

var b = function () {
  return "b";
};
```

<br>
왜냐하면, 아래처럼 선언만 위로 끌어올리기 때문에 b가 함수인 것을 모르기 때문이다.

```js
var b;
console.log(b());

b = function () {
  return "b";
};
```
