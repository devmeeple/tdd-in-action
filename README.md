# TDD in Action

타입스크립트와 함께 하는 TDD

## 테스트 주도 개발(Test-Driven Development)

테스트로부터 시작하는 개발 방식

1. (실패하는) 테스트 코드 작성
2. 테스트를 통과시킬 만큼 구현
3. 코드 정리(리팩토링)

## TDD를 시작할 때 어려운 점

테스트 코드 어디서부터 시작해야 하나?

### 테스트 코드 작성 순서

* 쉬움/예외 -> 어려움/정상
* 여려운 것부터 시도했을 때 시간이 오래 걸려 피드백이 느려진다. 또한 예외적인 상황을 뒤에서 테스트 하면 이미 구현한 코드 구조에 영향을 끼친다.
    * 회원 가입: 이메일이 이미 존재하면 vs 이메일이 존재하지 않으면
    * 만료일 계산: 1월 31일에서 한달 뒤 vs 1월 25일에서 한달 뒤
    * 회원 주소 변경: 회원이 없는 경우 vs 회원이 있는 경우

## 완급 조절

* 정해진 값을 반환하고 다양한 테스트를 추가하면서 구현을 일반화 한다.
* 구현이 생각나면 빠르게 구현한다.
    * 단 테스트를 통과시킬 정도로만 구현한다. 앞서가지 않는다.
* 구현이 막히면 다시 뒤로 돌아와서 천천히 진행한다.

## 기능

기능은 입력과 결과로 구성된다.

* 로그인
    * 입력: 아이디, 암호
    * 결과: (반환) 일치하면 true, 실패하면 false
* 회원 가입
    * 입력: 아이디, 암호, 이름
    * 결과: (반환) 회원 일련 번호, 회원 정보 DB에 저장

기능 명세는 설계로 연결된다. 이름, 파라미터, 리턴 타입 등 결정

## 추천 자료

* [테스트 주도 개발 - 켄트백](https://product.kyobobook.co.kr/detail/S000001032985)
* [클린코드 - 로버트 마틴](https://product.kyobobook.co.kr/detail/S000001032980)