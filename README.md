# 미션 - 다리 건너기

## 🚀 기능 요구 사항

위아래 둘 중 하나의 칸만 건널 수 있는 다리를 끝까지 건너가는 게임이다.

- 위아래 두 칸으로 이루어진 다리를 건너야 한다.
    - 다리는 왼쪽에서 오른쪽으로 건너야 한다.
    - 위아래 둘 중 하나의 칸만 건널 수 있다.
- 다리의 길이를 숫자로 입력받고 생성한다.
    - 다리를 생성할 때 위 칸과 아래 칸 중 건널 수 있는 칸은 0과 1 중 무작위 값을 이용해서 정한다.
    - 위 칸을 건널 수 있는 경우 U, 아래 칸을 건널 수 있는 경우 D값으로 나타낸다.
    - 무작위 값이 0인 경우 아래 칸, 1인 경우 위 칸이 건널 수 있는 칸이 된다.
- 다리가 생성되면 플레이어가 이동할 칸을 선택한다.
    - 이동할 때 위 칸은 대문자 U, 아래 칸은 대문자 D를 입력한다.
    - 이동한 칸을 건널 수 있다면 O로 표시한다. 건널 수 없다면 X로 표시한다.
- 다리를 끝까지 건너면 게임이 종료된다.
- 다리를 건너다 실패하면 게임을 재시작하거나 종료할 수 있다.
    - 재시작해도 처음에 만든 다리로 재사용한다.
    - 게임 결과의 총 시도한 횟수는 첫 시도를 포함해 게임을 종료할 때까지 시도한 횟수를 나타낸다.
- 사용자가 잘못된 값을 입력할 경우 `IllegalArgumentException`를 발생시키고, "[ERROR]"로 시작하는 에러 메시지를 출력 후 그 부분부터 입력을 다시 받는다.
    - `Exception`이 아닌 `IllegalArgumentException`, `IllegalStateException` 등과 같은 명확한 유형을 처리한다.

<br>

## 🚀 기능 목록

### 🔽 브릿지 게임 - 시작

***

#### · 출력

- [x] 게임 진행 안내 메시지

#### · 입력

- [x] 다리의 길이 입력

#### · 기능

- [x] 길이에 맞는 다리가 생성
- [x] 0과 1, "D","U"로 매칭

#### · 예외사항

- [x] 입력문이 숫자가 아닌 다른 문자인지
- [x] 입력문의 범위가 3 ~ 20 인지
- [x] 입력문이 널값인지
- [x] 다리의 길이가 3 ~ 20 인지
- [x] 0과 1, "D","U"로 매칭확인

  <br>

### 🔽 브릿지 게임 - 진행중

***

#### · 출력

- [x] 게임 진행 안내 메시지
- [x] 다리 상태

#### · 입력

- [x] 이동할 칸 선택

#### · 기능

- [x] 정답과 입력문이 일치하는지
- [x] 윗 다리 생성
- [x] 아랫 다리 생성
- [x] 한칸씩 움직임

#### · 예외사항

- [x] 입력문이 "D","U" 이외에 다른 문자인지

  <br>

### 🔽 브릿지 게임 - 성공/실패

***

#### · 출력

- [x] 게임 진행 안내 메시지
- [x] 다리 상태
- [x] 게임 종료 시, 성공 여부 및 시도 횟 수 출력

#### · 입력

- [x] 재시도 및 종료 커맨드

#### · 기능

- [x] 재시도 커맨드 입력 시, 게임 재개
- [x] 종료 커맨드 입력 시, 게임 종료

#### · 예외사항

- [x] 입력문이 "R","Q" 이외에 다른 문자인지
  <br>
