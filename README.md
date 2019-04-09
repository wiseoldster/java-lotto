## 프리코스 3주차 미션 : 로또
---
### 기능 요구 사항
+ 로또 게임 기능을 구현해야 한다.
+ 로또 구입 금액을 입력하면 구입 금액에 해당하는 로또를 발급해야 한다.
+ 로또 한 장의 가격은 1000원이다.
+ 로또 담청 금액은 고정되어 있는 것으로 가정한다.
+ 수익률을 계산해 출력해야 한다.

### 프로그래밍 요구사항
+ 다음 Lotto 객체를 활용해 구현해야 한다.
  + Lotto 기본 생성자를 추가할 수 없다.
  + number 변수의 접근 제어자인 private를 변경 할 수 없다.
  + Lotto에 필수(인스턴스 변수)를 추가할 수 없다.
+ 다음 WinningLotto 객체를 활용해 구현해야 한다.
  + match() 메소드의 반환 값인 Rank는 저장소에서 제공한다.
  + WinningLotto 기본생성자를 추가할 수 없다.
  + lotto, bonusNo 변수의 접근 제어자인 private을 변경 할 수 없다.
  + WinningLotto에 필드(인스턴스 변수)를 추가할 수 없다.
+ 자바 코드 컨변션을 지키면서 프로그래밍한다.
+ indent(들여쓰기) depth를 2이 넘지 않도록 구현한다.
+ 함수(또는 메소드)의 길기가 10라인을 넘어가지 않도록 구현한다. 
+ 함수(또는 메소드)의 인자 수를 3개 까지만 허용한다.
+ else 예약어를 쓰지 않는다.  

### 구현 기능 목록
+ 구입 금액을 입력 받아아야 한다.
  + 구입금액이 숫자인지 확인해야 한다.
+ 구입 금액에 따른 구매 장수를 구해야 한다.
  + 구매금액이 PRICE원으로 나누어 떨어지지 않는 경우 구입금액을 재조정 해줘야 한다.
  + 구입 장수가 0장인 경우 수익률 예외처리하여 프로그램을 종료하거나, 수익률 계산시 예외 처리를 한다. 
+ 중복되지 않는 1~MAX_BALL_NUM 사이의 숫자 임의의 숫자 NUM_BALL개를 생성해야 한다.
+ 로또의 번호를 정렬한다.
+ 구매한 로또 번호를 출력해야 한다.
+ WinningLotto를 생성해야한다.
  + NUM_BALL개의 숫자를 입력 받아 Lotto 객체로 반환할 수 있어야 한다.
  + 보너스볼을 입력 받아 winningLotto에 저장할 수 있어야 한다.
  + 입력 된 숫자의 갯수가 NUM_BALL인지 확인해야한다.
  + 입력 된 숫자가 1~MAX_BALL_NUM 사이의 숫자가 맞는지 확인 해야한다.
+ (WinningLotto.match)구매한 로또가 몇 등인지 알아야 한다.
  + 구매한 로또와 위닝 로또가 몇 개의 숫자가 겹치는지 알아야 한다.
  + 보너스 번호가 구매한 로또에 있는지 알 수 있어야한다.
+ 당첨통계를 출력해야 한다.
  + 각 Rank에 값에 대해 적절한 출력 String으로 변환한다. rankToSting
  + 각 Rank에 값에 대해 해당하는 로또가 몇장인지 출력해야한다.
  + 총 당첨 금액을 계산해야한다.
  + 수익률을 출력해야한다.

### 상수, 변수  목록
+ private final int PRICE = 1000  
+ private final int MAX_BALL_NUM = 45
+ private final int NUM_BALL = 6
+ private static List<Lotto> myLottos
+ private static WinningLotto winningLotto
+ private HashMap<Rank, Integer>(?) Result  


### 실행결과 예
구입금액을 입력해주세요.  
500  
    
0개를 구매했습니다.  
  
지난 주 당첨 번호를 입력해주세요.  
1,2,3,4,5,6  
보너스 볼을 입력해 주세요.  
7  
  
당첨통계  
\-\-\-\-\-\-
3개 일치(5000원) - 0개
4개 일치(50000원) - 0개
5개 일치 (1500000원) - 0개
5개 일치, 보너스 볼 일치(30000000원) - 0개
6개 일치(2000000000원) - 0개
총 수익률은 0입니다.

