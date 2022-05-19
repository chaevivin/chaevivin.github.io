---
title: 8. CSS display
categories: [CSS]
comments: true
---

# display
- 요소의 박스 타입 설정
- 속성 값
    - block : 블록 요소 
    - inline : 인라인 요소
    - inline-block : 인라인-블록 요소
    - 기타 : table, table-cell, flex 등
    - none : 요소의 박스 타입이 없음 (요소가 사라짐)
    
- inline 요소는 화면에 보이지 않는다 (text 위주) -> display: block으로 바꾸면 보여진다. (반대도 가능)
- inline-block 요소는 원래 inline인데 block 특징을 가진다. (margin, padding, 너비) -> 수평으로 쌓임
- none은 요소가 아예 사라진다. - opacity는 존재하지만 보이지 않는다.

{% include codepen.html hash="ZErKJNa" title="css_display" %}