# 자바스크립트 This

## this란?

- 대부분의 객체지향 언어에서는 this는 클래스로 생성한 인스턴트를 가리키지만 자바스크립트는 실행 컨텍스트 생성될 떄 결정 (함수가 호출할 때)
- 전역 공간에서의 this는 브라우저는 window 노드는 global

## 동작 방식

- **함수**
  - 독립적인 기능을 수행하는 코드 묶음을 함수라고 칭함
  - 함수에서의 this는 **strict mode**를 하지 않으면 window or global를 가리키고 **strict mode**를 하면 undefined를 가리킴
- **메소드**
  - 객체에 할당된 함수를 메소드라고 칭함
  - 메소드에서의 this는 호출한 객체를 가리킴
- **화살표 함수**
  - 화살표 함수는 고유한 this를 가지지 않고 상위 컨텍스트의 this를 참조함
  - 메소드내의 내부 함수의 this를 바인딩 할 때 유용함
- **콜백 함수**
  - 콜백 함수도 함수임 기본적으로 **strict mode**를 하지 않으면 window or global을 가리킴
  - 하지만 addEventListner에서의 콜백함수의 this는 addEventListner를 호출한 DOM객체를 가리키게 되어있음
- **생성자 함수**
  - 함수내에 this.[property]를 쓰면 다른 객체지향 프로그래밍 언어 처럼 new 연산자를 써서 인스턴스를 만들 수 있음
  - 이때의 this는 인스턴스 자신을 가리킴
- **call / apply / bind**
  - call / apply / bind를 쓰면 this를 명시적으로 바인딩 할 수 있음
  - 세가지다 첫번째 인자는 바인딩할 객체
  - call의 두번째 이후 인자 목록들을
  - apply 두번째 인자는 배열을
    - Math.max.apply(null, 배열)을 사용하면 배열을 받을 수 있음
      - spread 연산자 쓰면 더 편하다 Maht.max(...rest)
  - bind는 call과 비슷하지만 함수를 반환함
  - 유사배열객체를 Array.prototype의 내장 함수를 사용할 수 있음
    - 솔직히 걍 Array.from() 사용하는게 더 나음

## 참고

- 코어 자바스크립트
- [MDN](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Operators/this)
