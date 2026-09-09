### 1. JavaScript 배열(Array)

JavaScript에서 배열은 여러 개의 데이터를 하나의 변수에 저장할 수 있는 데이터 타입이다.

```javascript
let fruits = ["사과", "바나나", "딸기"];
````

배열의 각 데이터에는 **인덱스(index)**가 있으며, 인덱스는 0부터 시작한다.


console.log(fruits[0]); // 사과
console.log(fruits[1]); // 바나나
console.log(fruits[2]); // 딸기


배열에 데이터를 추가하거나 삭제할 수도 있다.

```javascript
fruits.push("포도"); // 마지막에 포도 추가
fruits.pop();        // 마지막 데이터 삭제
```

또한 `length`를 이용하면 배열에 들어 있는 데이터의 개수를 확인할 수 있다.

```javascript
console.log(fruits.length);
```

배열은 여러 데이터를 저장하고 반복해서 처리할 때 유용하게 사용할 수 있다.

### 2. class가 설정된 HTML 태그에 접근하기

HTML 태그에 `class`를 설정하고 JavaScript를 이용하면 해당 태그에 접근하여 내용을 변경하거나 조작할 수 있다.

HTML에서 다음과 같이 class를 설정한다.

```html
<p class="hello">안녕하세요</p>
```

JavaScript의 `querySelector()`를 사용하면 특정 class를 가진 태그에 접근할 수 있다.

```javascript
let tag = document.querySelector(".hello");
```

여기서 `.hello`의 `.`은 **class를 의미한다.**

따라서

```javascript
document.querySelector(".hello");
```

는 **class가 `hello`인 태그를 찾아서 가져오는 것**이다.

가져온 태그는 JavaScript를 통해 조작할 수 있다.

```javascript
tag.textContent = "반갑습니다!";
```

실행하면 HTML의 내용이

```html
<p class="hello">반갑습니다!</p>
```

로 변경된다.

여러 개의 같은 class를 가진 태그에 접근할 때는 `querySelectorAll()`을 사용할 수 있다.

```javascript
let students = document.querySelectorAll(".student");
```

### 느낀 점

이번 공부를 통해 JavaScript가 단순히 데이터를 처리하는 것뿐만 아니라 HTML의 태그를 직접 찾아서 내용을 변경하거나 조작할 수 있다는 것을 알게 되었다.

특히 `querySelector(".class이름")`을 사용하면 **class를 기준으로 원하는 HTML 태그에 접근할 수 있다는 점**을 이해했다.


요약하면,

배열
→ 여러 데이터를 하나로 묶음
→ [0], [1], [2]처럼 인덱스로 접근

class 태그 접근
→ HTML에 class 설정
→ querySelector(".클래스이름")
→ 해당 태그를 가져옴
→ textContent 등으로 조작
