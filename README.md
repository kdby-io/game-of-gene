# game-of-gene

Conway's Game of Life에 유전 알고리즘을 적용.

## 정의

### Grid

2차원 Cell 배열.

### Cell

`alive` 또는 `dead`상태인 1차원 Gene 배열. 살아있는 Cell만 Gene 배열을 가진다.

### Gene

Grid의 다음 상태 결정에 영향을 미치는 요소.

> 어떻게 만들 것인가? 위치에 따라 특성이 정해진 bool or int 배열? 아니면 함수 배열? 다른 셀에 영향을 미칠 수 있는가? 없는가?

## 과정

### Initialize

랜덤하게 Gene을 가진 Cell을 다수 생성하여 Grid에 배치.

### Iterative Process

Game of gene의 사이클은 Conway's game of life와 유전 알고리즘 사이클을 조합한다.

1. 각 Cell의 다음 상태를 결정한다. 각 Cell은 현재 상태에 Conway's game of life의 규칙과 소유한 Gene을 적용해 다음 상태를 결정한다.
2. 다음 상태에서 살아있는 각 Cell의 Gene을 결정한다. 해당 Cell에 영향을 준 현재 상태의 Cell들의 Gene을 조합하여 해당 Cell의 Gene을 결정한다.

### 참고

Game of life 사이클

1. Evaluate: 현재 상태를 룰에 적용해 다음 상태를 결정. 반복.

유전 알고리즘 사이클

1. Fitness function: 주어진 문제에 대해 염색체의 적합도를 계산.
2. Select**: 적합도를 기준으로 염색체를 선택.
3. Generic operator: 선택한 염색체로 다음 세대의 유전자를 생성.

## Todo

- [ ] game of life 구현
- [ ] Gene 데이터타입 결정
- [ ] Gene이 다른 셀에 영향을 미칠 수 있는지 결정
- [ ] Genetic Operator 구현
