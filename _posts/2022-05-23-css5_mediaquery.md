---
title: 19. CSS 반응형 미디어쿼리 ⭐
categories: [CSS]
comments: true
---

## 반응형 웹
반응형 웹은 쉽게 말해 브라우저의 크기가 변할 때마다 css 디자인이 바뀌는 것을 말한다. 데스크탑, 태블릿, 모바일의 화면 크기가 다 다르기 때문에 화면 크기가 바뀔 때마다 디자인이 바뀌면서 해당 화면에서 더 잘 보일 수 있도록 고안된 것이다.

<br>

- 반응형 웹 예시 : https://chaevivin.github.io/Portfolio/ 
    - 브라우저의 크기를 늘였다 줄였다 하면서 화면이 어떻게 바뀌는 지 확인해 보세요.

<br>

- 사용법
    - @media screen and () {실행문}
{% highlight css %}
@media screen and (min-width: 768px) {
    div {
        width: 60%;
        background-color: blue;
    }
}
{% endhighlight %}

<br>

- min과 max의 의미
    - min : 브라우저 크기가 000px 이상일 때 적용
    - max : 브라우저 크기가 000px 이하일 때 적용 

### 주의 사항

- min과 max 사용 시 작성 순서 
    - min을 사용할 때는 반드시 크기가 작은 순서대로 작성
    - max를 사용할 때는 반드시 크기가 큰 순서대로 작성
{% highlight css %}
@media screen and (min-width: 320px) {실행문}
@media screen and (min-width: 768px) {실행문}
@media screen and (min-width: 1024px) {실행문}
{% endhighlight %}
{% highlight css %}
@media screen and (max-width: 1024px) {실행문}
@media screen and (max-width: 768px) {실행문}
@media screen and (max-width: 320px) {실행문}
{% endhighlight %}