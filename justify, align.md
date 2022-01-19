# Column & Row
- justify는 main axis
- align는 cross axis

### 1. flex-direction : row
- main axis(justify) 가로, cross axis(align) 세로

### 2. flex-direction : column
- main axis(justify) 세로, cross axis(align) 가로

# align-self and order (자식 컴포넌트에서 설정)
- justify-content, align-items는 부모 컴포넌트에서 설정

### 1. align-self
- align-items와 비슷, cross axis
- 한 박스에만 적용
- align-items나 align-self나 둘 다 반드시 부모에서 height 설정 필요

### 2. order
- 자식 컴포넌트에서 box의 순서 변경할 때 쓰는 것(html을 직접 옮겨 순서 변경하기 어려울 때)
- 기본적으로 box의 order은 0
- 그래서 1, 2, 3의 박스가 있을 때 2번 박스에 order 1을 부여하면 1(order: 0), 3(order: 0), 2(order: 1)의 순서로 박스가 놓여짐
