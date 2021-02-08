# 자바스크립트 클로저

## 클로저란?

클로저는 **특정 함수가 외부 변수를 기억하고 있는 특성**이다. 클로저는 자바스크립트에 있는 개념이 아니라 함수형 프로그래밍을 지원하는 언어에서 보편적으로 볼 수 있는 개념이다.

```javascript
function outer() {
  const name = "james";

  return function () {
    console.log(name);
  };
}

const bar = outer();
bar();
// result - console james
```

위의 코드를 보면 bar를 호출 할 때 분명 outer의 실행 컨텍스트는 종료가 된 상태이다 하지만 bar를 호출 할 때 정상적으로 james가 호출이 된다.
클로저는 **외부 함수가 반환이 되어도 가비지 컬렉션에 의해 제거 되지 않고 유지가 된다**.

## 활용 방법들

- 정보 은닉
- 지연 평가 (currying)
