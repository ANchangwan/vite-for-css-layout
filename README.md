# CSS

# ✅ Grid

- **_grid란_**수평선과 수직선이 교차해서 이루어진 집합체
- 하나의 집합체는 세로 열을 그리고 다른 하나는 가로 행을 정의

# ✅ grid-auto

<aside>
✍🏻 grid-auto-rows && grid-auto-columns

</aside>

- 동적으로 grid를 설정하고 싶을 때 사용
- 2 x 2 grid에서 만약에 추가로 열이 추가 될 때 그 열에 크기를 동적으로 설정 가능

<aside>
✍🏻 grid-auto-flow

</aside>

- 동적으로 추가되는 형태를 설정할 수있음
  - grid-auto-flow: row OR column

# ✅ align, justify

- align은 세로축을 의미한다
- justify는 가로축을 의미한다.
-

<aside>
✍🏻 items

</aside>

- items는 부모를 기준으로 하나의 수직,수평 선을 정령한다.

<aside>
✍🏻 self

</aside>

- 자식을 기준으로 움직인다.
- grid-column or row : span 2를 하면 두개의 영역을 가진다.

<aside>
✍🏻 content

</aside>

- 부모를 기준으로 두줄 이상의 정렬을 한다.

items와 content의 차이는?

items 👉 item을 어떻게 배치 할 것인가에 대한 속성

content 👉 item의 줄 간격을 어떻게 배치 할 것인가에 대한 속성

# Auto Sizing and Minmax

## min-content / max-content
✍️ min-content
단어 중에서 가장 큰 값을 기준으로 셀 크기를 정함
✍️ max-content
전체 단어 길이를 기준으로 셀 크기를 정함
✍️minmax
    - 반응형으로 만듬
    - 최소로 줄어들 크기, 최대로 커질 크기를 정함
    - grid-template-columns: 1fr minmax(250px, 1fr) 1fr 또는 repeat(3, minmax(250px, 1fr)) 

# ✅ auto-fill & auto-fit

두개의 차이는 남는 여백으로 사용이 달라진다.

✍️auto-fill

최대한 많은 아이템을 배치하고, 남은 공간은 비어있게 둡니다.

✍️ auto-fit

필요한 만큼의 아이템을 배치하고, 남은 공간은 아이템을 늘려 채웁니다.