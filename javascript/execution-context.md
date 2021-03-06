# 자바스크립트 실행 컨텍스트

## 실행 컨텍스트란?

실행 컨텍스트는 **실행할 코드에 제공할 환경 정보를 담아 놓은 객체이다.** This, Closure, Hosting등 자바스크립트의 핵심 개념들을 이해하는데 굉장히 중요하다.

## 종류

- **전역 컨텍스트** - 보통 브라우저 or 노드가 실행되는 시점에 활성화 된다. 애플리케이션이 종료 될 때 까지 호출 스텍에 남아 있는다.
- **함수 컨텍스트** - 함수가 실행 될 때 실행 컨텍스트가 생성 되고 함수가 끝나면 호출 스텍에서 제거 된다.

## 실행 컨텍스트가 수집하는 정보

- **Variable Object (변수 객체)** - 컨텍스트를 구성하는 함수의 매개 변수, 변수의 식별자, 선언된 함수를 저장하는 객체를 말한다.

- **Scope Chain (스코프 체인)** - 스코프란 식별자의 유효범위 이다. 식별자의 유효범위를 콜스택의 안에서 부터 바깥 범위로 리스트 형식으로 관리 하게 되는데 이것을 **스코프 체인** 이라고 한다.

- **This Value** - This에 대한 정보를 담고 있다.

## Reference

- https://poiemaweb.com/js-execution-context
- 코어 자바스크립트 (책)
