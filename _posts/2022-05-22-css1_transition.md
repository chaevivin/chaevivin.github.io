---
title: 14. CSS transitions
categories: [CSS]
comments: true
---

# Transitions (전환)
- 전환 효과를 지정
- 바뀌기 전 요소에 transition 속성 작성
- 사용법
    - transition: 속성이름 지속시간 [타이밍함수 대기시간];
{% highlight css %}
div {
    transition: width 1s, background 1s;
}
{% endhighlight %}

<br>

### transition-property
- 전환 효과를 사용할 속성 이름을 설정
- 속성 값
    - all : 모든 속성에 적용
    - 속성 이름 : 전환 효과를 적용할 속성 이름

<br>

### transition-duration 
- 전환 효과의 지속시간을 설정
- 속성 값
    - 시간 : 전환 효과가 지속되는 시간

<br>

### transition-timing-function
- 타이밍 함수 (애니메이션 전환 효과) 지정
- 속성 값
    - ease : 빠르게-느리게
    - linear : 일정하게
    - ease-in : 느리게-빠르게
    - ease-out : 빠르게-느리게
    - ease-in-out : 느리게-빠르게-느리게
    - cubic-bezier(n, n, n, n) : 값 지정 (0 ~ 1)
    - steps(n) : n번 분할된 애니메이션

<br>

### transition-delay
- 전환 효과가 몇 초 뒤에 시작할 지 대기시간 지정
- 속성 값
    - 시간 : 전환 효과의 대기시간을 설정

<br>

{% include codepen.html hash="eYVRqLB" title="css_transitions" %}