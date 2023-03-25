# strict mode
- 자바스크립트 언어의 문법을 좀 더 엄격히 적용하여 오류를 발생시킬 가능성이 높거나 자바스크립트 엔진의 최적화 작업에 문제를 일으킬 수있는 코드에 에러를 발생시킴.
- ESLint 같은 도구로 대체 가능.

## 적용법
- 전역 또는 함수 몸체 첫 번째 라인에 ```"use strict";``` 추가하면 strict 모드가 적용됨.
- ex)   
    => 적용 전, 일반 함수의 this는 window 객체를 가리키지만, 적용 하면 this는 global 객체를 가리키게 됨.

## 주의할 점
- strict mode와 non-strict mode를 혼용할 경우 오류를 발생시킬 수 있음. 따라서 즉시 실행 함수로 스크립트 전체를 감싸서 스코프를 구분하고 선두에 strict mode 선언.
- 함수 단위로 strict mode를 적용 시킬 경우, 그 함수가 상위 컨텍스트를 참조하게 될 경우, 그 상위 컨텍스트가 non-strict 모드라면 오류를 발생시킬 수 있음.

## strict 모드가 잡아내는 에러
- 암묵적 전역선언
- 변수, 함수, 매개변수의 삭제 (window객체에 들어가있는 프로퍼티들)
- 매개변수 네임 중복
- ~with문 사용 (eval, with 금기어)~

# 빌트인 객체
- Object, String, Number, Set, Map, Boolean, Function, Promise 등등,, ECMAScript 사양에 정의된 객체들
  Math, Reflect, JSON을 제외한 표준 빌트인 객체는 모두 인스턴스를 생성할 수 있는 생성자 함수 객체

## 레퍼 객체
- 원시값은 기본적으로 프로퍼티나 메서드를 가질 수 없음, 근데 객체처럼 동작하게 하는 이유.
- 원시타입 값에 대해 객체처럼 접근하면 생성되는 임시 객체 
- ex) ```const str="hi"; console.log(str.length) // 2```
- null과 undefined는 레퍼 객체를 생성하지 않음

## URI
- ```https:``` protocol
- ```www.naver.com``` domain(host)
- ```:80``` port
- ```/docs/search?``` path
- ```?category=javascript&lang=ko``` query(query string)
- ```#intro``` fragment

## encoding, decoding
- encodeURI 는 uri 이스케이프 처리
- decodeURI 는 uri 이스케이프 처리 전 uri로 돌려놓음
- encodeURIComponent 와 decodeURIComponent 는 쿼리스트링부분만 처리

# this
- this는 자신이 속한 객체 또는 자신이 생성할 인스턴스를 가리키는 자기 참조 변수.
- this가 가리키는 값은 함수 호출 방식에 따라 동적으로 결정됨.

## this바인딩
- this가 가리킬 객체를 바인딩 (이어준다고 생각)
- this 바인딩 또한 동적으로 결정될 수 있다. strict 모드가 this 바인딩에 영향을 줄 수 있음.

## 함수호출방식과 this바인딩
- 자바스크립트는 정적스코프, 함수 정의가 평가되어 함수 객체가 생성되는 시점에 상위 스코프를 결정함. ```하지만 this 바인딩은 함수 호출 시점에 결정됨.```

### 일반함수
- this에 전역객체가 바인딩됨.
- strict 모드에선 undefined가 바인딩됨.

### 메서드
- 메서드는 객체에 포함되는 것이 아니라 독립적으로 존재하는 별도의 객체
- 따라서 메서드 안의 this는 메서드를 소유한 객체가 아닌 메서드를 호출한 객체에 바인딩됨.

### 생성자 함수
- 생성자 함수 내부의 this는 생성될 인스턴스가 바인딩됨.

## call, apply, bind
- call, apply, bind를 사용하면 this를 동적바인딩 가능.
- ex)
=> 비동기 처리되는 setTimeout 콜백 함수안의 this는 본래 window 전역객체를 가리키게됨. 그러나 위 메소드로 동적바인딩하면 바인딩 된 객체를 가리킴.







