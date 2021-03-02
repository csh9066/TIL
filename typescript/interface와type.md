# 타입스크립트의 interface와 type의 차이점은 뭐고 언제 어디에 사용해야 할까?

- 둘의 공통점은 class, interface의 대해 implements 키워드를 통해 관계를 정의할 수 있다는 점이다 (예전에는 type은 implments가 안됐다고 함)
- 둘의 가장 큰 차이점은 interface는 동일한 이름의 여러번 선언해도 컴파일 시점에서 합칠 수 있음(선언 병합), interface가 좀 더 다양한 기능을 제공함으로 타입스크립트 개발팀은 interface를 추천함
- 유니온 타입, 교차 타입을 사용시 type을 사용하도록 하자 !(유니온 타입, 교차 타입은 implement가 안됨)
