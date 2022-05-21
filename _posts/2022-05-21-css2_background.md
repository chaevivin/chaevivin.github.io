---
title: 13. CSS background
categories: [CSS]
comments: true
---

# background
- 배경 설정
- 사용법
    - background: 색상 이미지경로 반복 위치 스크롤특성;

<br>

### background-color
- 요소의 배경 색상 지정
- 속성 값
    - 색상 : 요소의 배경 색상
    - transparent : 투명

<br>

### background-image
- 요소의 배경에 하나 이상의 이미지 삽입
- 속성 값
    - none : 이미지 없음
    - url("경로") : 이미지 경로 URL
- 사용법
    - background-image: url("경로");
- 배경 이미지 삽입 시, 요소의 크기가 설정되어 있어야 배경 이미지가 보인다.
- 하나 이상의 배경 이미지를 삽입할 경우 ','로 구분한다. 먼저 작성된 이미지가 더 위에 쌓인다.
- url() 속성 단독 사용 불가

<br>

### background-repeat
- 배경 이미지의 반복을 설정
- 속성 값
    - repeat : 배경 이미지를 수직, 수평으로 반복
    - repeat-x : 배경 이미지를 수평으로 반복
    - repeat-y : 배경 이미지를 수직으로 반복
    - no-repeat : 반복 없음

<br>

### background-position
- 배경 이미지의 위치를 설정
- 속성 값
    - % : 왼쪽 상단 모서리는 0% 0%, 오른쪽 하단 모서리는 100% 100%
    - 방향 : 방향을 입력하여 위치 설정 (top, bottom, left, right, center)
    - 단위 : px, em, cm 등 단위로 지정
- 사용법
    - 방향
        - background-position: 방향1 방향2;
    - 단위
        - background-position: x축 y축;

<br>

### background-attachment
- 요소가 스크롤될 때 배경 이미지의 스크롤 여부
- 속성 값
    - scroll : 배경 이미지가 요소를 따라서 같이 스크롤
    - fixed : 배경 이미자 뷰포트에 고정되어 같이 스크롤 되지 않는다.
    - local : 요소 내 스크롤 시 배경 이미지가 같이 스크롤

<br>

### background-size
- 배경 이미지 크기 지정
- 속성 값
    - auto : 배경 이미지가 원래의 크기로 표시
    - 단위 : px, em, % 등 단위로 지정
    - cover : 배경 이미지의 크기 비율을 유지하며 요소의 더 넓은 너비에 맞춰짐 (이미지가 잘릴 수 있음)
    - contain : 배경 이미지의 크기 비율을 유지하며 요소의 더 짧은 너비에 맞춰짐 (이미지가 잘리지 않음)