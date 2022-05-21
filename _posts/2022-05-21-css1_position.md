---
title: 12. CSS position
categories: [CSS]
comments: true
---

# position
- 요소의 위치 지정 방법의 유형 설정
- 속성 값
    - static : 유형 없음 / 배치 불가
    - relative : 요소 자신을 기준으로 배치
    - absolute : 위치 상 부모 요소를 기준으로 배치
    - fixed : 브라우저를 기준으로 배치
    - sticky : 스크롤 영역으로 배치

<br>

### relative
- 자기 자신을 기준으로 배치
- 자기 자신을 기준으로 배치하기 때문에 자신의 위치가 필요하다. 그래서 요소가 이동한 것처럼 보이지만 원래는 자기 자신의 위치에서 안 보이는 상태이다.
- 주변의 형제 요소에 영향을 받기 때문에 relative를 사용할 때 조심해서 사용해야 한다.

{% include codepen.html hash="YzeQoQG" title="css_relative" %}
- 자기 자신을 기준으로 위에서 20px, 왼쪽에서 50px 이동

<br>

### absoulte ✨ 추천 ✨
- 부모 요소 기준으로 배치 (위치 상의 부모 요소)
- position: relative 가 들어있는 요소를 위치 상의 부모 요소로 삼는다.
- position: relative 가 없으면 뷰포트를 위치 상의 부모 요소로 삼는다.
    - 요소 → 부모 요소 → 조상 요소 → <body> → <html> → window 객체 = 뷰포트 = 화면 전체

<br>

### fixed
- 브라우저(뷰포트) 기준으로 배치
- absolute는 부모 요소를 기준으로 삼기 때문에 뷰포트를 기준으로 삼으려면 fixed 사용

<br>

### sticky
- 스크롤 영역 기준으로 배치
- IE 지원 불가
- top, bottom, left, right 중 값이 하나 이상 존재해야 한다.
{% highlight css %}
.box {
	position: sticky;
	top: 0;  /* 상단에 고정 */
}
{% endhighlight %}