# 표준 빌트인 객체 중 생성자 함수 객체 메서드1

---

## Number
1. ```Number.MAX_VALUE``` 자바스크립트에서 표현할 수 있는 가장 큰 양수 값
2. ```Number.MIN_VALUE``` 자바스크립트에서 표현할 수 있는 가장 큰 음수 값
3. ```Number.MAX_SAFE_INTEGER``` 자바스크립트에서 표현할 수 있는 가장 큰 안전한 정수 값 < 범위를 벗어난다면 ```BigInt``` 사용
4. ```Number.MIN_SAFE_INTEGER``` 자바스크립트에서 표현할 수 있는 가장 작은 정수 값
5. ```Number.isNaN()``` 인수가 NaN이면 true, 아니면 false 반환
6. ```Number.isInteger()``` 인수가 정수면 true 반환, 인수를 암묵적 형변환 하지 않음
7. ```Number.isSafeInteger()``` 인수가 안전한 정수면 true, 아니면 false 반환
8. ```Number.toFixed()``` 인수로 소수점 이하 자릿수를 나타내는 0~20 전달 가능. 반올림하는 메서드
9. ```Number.toString()``` 진법을 나타내는 2~36 사이의 숫자를 인수로 전달 가능. 문자열로 변환하여 반환하는 메서드

## Math
1. ```Math.PI``` 원주율 파이 값 (3.141592653589793) 을 반환
2. ```Math.abs()``` 인수로 전달된 정수값의 절대값 반환
3. ```Math.round()``` 소수점 이하를 반올림
4. ```Math.ceil()```  소수점 이하를 올림
5. ```Math.floor()``` 소수점 이하를 내림
6. ```Math.sqrt()``` 제곱근 반환
7. ```Math.random()``` 0~1사이의 난수 값 랜덤으로 반환
8. ```Math.pow()``` 첫 번째 인수로 밑, 두 번째 인수를 지수로 거듭제곱한 결과를 반환
9. ```Math.max()``` 전달받은 인수 중 가장 큰 값 반환
10. ```Math.min()``` 전달받은 인수 중 가장 작은 값 반환

## Date
- ``` new Date() ``` <= 와 같이 new 연산자로 인스턴스를 생성한다.
  ```new Date(2020, 2, 26, 10, 00, 00, 0); // Thu Mar 26 2020 10:00:00 GMT+0900``` 
  첫 번째부터 yeqr, month, day, hour, minute, second, millisecond 를 인자로 받는다.
- ```Date.now()``` 1970년 1월 1일 00:00:00(UTC)을 기점으로 현재까지 경과한 밀리초를 숫자로 반환
  ```new Date(Date.now())``` << 현재시간 반환
- ```new Date('2020/07/24').getFullYear``` Date 객체의 연도를 나타내는 정수 반환
- ```new Date().setFullYear``` Date 객체의 연도를 나타내는 정수 설정
- month, day, seconds, milliseconds도 위와 동일한 메서드 존재, month는 +1 해줘야 현재 달이 나옴.

