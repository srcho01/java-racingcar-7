# 자동차 경주

### 🎯 기능 요구 사항
- 주어진 횟수 동안 n대의 자동차는 전진 또는 정지
- 각 자동차에 이름을 부여할 수 있다. 전진하는 자동차를 출력할 때 자동차 이름을 같이 출력한다.
- 자동차 이름은 쉼표(,)를 기준으로 구분하며 이름은 5자 이하
- 사용자는 몇 번의 이동을 할 것인지를 입력할 수 있어야 한다.
- 전진하는 조건은 0에서 9 사이에서 무작위 값을 구한 후 무작위 값이 4 이상일 경우이다.
- 자동차 경주 게임을 완료한 후 누가 우승했는지를 알려준다. 우승자는 한 명 이상일 수 있다.
- 우승자가 여러 명일 경우 쉼표(,)를 이용하여 구분한다.
- 사용자가 잘못된 값을 입력할 경우 IllegalArgumentException을 발생시킨 후 애플리케이션은 종료되어야 한다.

### 🎯 프로그래밍 요구 사항
- indent depth를 최대 2까지
- 3항 연산자 금지
- 함수(또는 메서드)가 한 가지 일만 하도록 최대한 작게
- JUnit 5와 AssertJ를 이용한 테스트 코드 작성

<br><br>

### 🔧 구현할 기능
- [ ] Model Layer
  - [ ] Car : 자동차 객체. 이름 및 현재 위치 저장.
  - [ ] Race : Car 리스트, 진행해야 할 총 round 저장 
- [ ] View Layer
  - [ ] Input : 자동차 이름 및 진행횟수 입력. 조건에 맞지 않는 입력은 예외 처리.
  - [ ] Output : 각 round 별 경기 결과 출력. 최종 우승자 출력.
- [ ] Service Layer
  - [ ] GameService : 한 라운드를 진행하는 로직. 우승자 결정 로직.
- [ ] Controller Layer
  - [ ] CarRace : 전체 라운드를 진행. Model 객체 생성. Service와 View 연결.
- [ ] Util
  - [X] Exception : 처리할 예외 목록
  - [X] CONSTANT : 필요한 상수값 변수화