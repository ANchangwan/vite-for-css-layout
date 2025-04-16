
# CSS ::before 와 content 정리

## ::before란?

`::before`는 **CSS의 가상 요소(Pseudo-element)**입니다.  
선택한 요소 **앞에** 실제 HTML에는 없는 **가상의 요소**를 생성하여 스타일링할 수 있습니다.

### ✅ 특징
- HTML 구조를 변경하지 않고도 콘텐츠를 추가할 수 있음
- 아이콘, 장식, 선 등을 추가할 때 유용함

### ✅ 사용 예시
```css
h1::before {
  content: "🔥";
}
```
→ 모든 `<h1>` 요소 앞에 불 이모지가 가상으로 추가됩니다.

---

## content란?

`content`는 `::before` 또는 `::after`와 함께 사용되며,  
**가상 요소 안에 어떤 내용을 넣을지** 정하는 CSS 속성입니다.

### ✅ 가능한 값
- 텍스트
- 이미지 (예: `url("image.png")`)
- 빈 문자열 `""` (보이지 않지만 스타일은 적용 가능)

### ✅ 사용 예시
```css
h1::before {
  content: "🔥"; /* 불 이모지 추가 */
}

h1::after {
  content: " 끝!"; /* 텍스트 추가 */
}
```

```css
.box::before {
  content: ""; 
  display: block;
  width: 100%;
  height: 2px;
  background-color: red;
}
```
→ `""`를 사용해 보이지 않는 요소를 만들고, 선 등의 스타일을 적용할 수 있음

---

## 활용 예시: HTML 수정 없이 선 추가하기

```css
.product__footer {
  position: relative; /* 기준 요소 설정 */
}

.product__footer::before {
  content: ""; /* 가상 요소 생성 */
  position: absolute;
  top: 0;
  bottom: 0;
  left: 50%; /* 가운데 정렬 */
  width: 0;
  border-right: 2px solid #292d32; /* 세로선 */
  z-index: 1;
}
```

→ `.product__footer` 요소의 **가운데에 세로선을 가상 요소로 삽입**합니다.

---

## 요약

| 개념        | 설명 |
|-------------|------|
| `::before`  | 선택한 요소 앞에 가상 요소를 생성 |
| `content`   | 가상 요소에 넣을 내용을 정의 |

### ✅ 장점
- HTML을 변경하지 않고도 아이콘, 장식, 선 등을 추가 가능
- 스타일링과 꾸미기에 매우 유용

---

## 참고
- `::after`도 같은 방식으로 사용 가능 (단, 요소 뒤에 삽입됨)
