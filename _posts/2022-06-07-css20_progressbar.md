---
title: CSS만 사용해서 아이콘과 함께 움직이는 진행바 만들기
categories: [CSS]
comments: true
---

<br>

![css_progressbar](https://user-images.githubusercontent.com/83055813/172118039-beffed09-f2f7-4920-a668-7a2ef48ca05e.gif)

<br>

## 자바스크립트 없이 CSS로 아이콘과 함께 움직이는 프로그레스바 만들기

<br>

개요 : 미니프로젝트를 진행하던 중 아이콘과 함께 움직이는 프로그레스바를 만들고 싶었으나 제이쿼리나 자바스크립트를 사용해야 했다. 
제이쿼리는 요즘 덜 사용하는 추세여서 최대한 안 쓰고 싶었다. 자바스크립트는 프로그레스바를 간단하게 구현할 수 있으나 아이콘과 함께 움직이는 프로그레스 바는 구현하기 힘들었다. <span style="color: yellow;">그래서 CSS만 사용해서 구현해보기로 했다.</span>

<br>
<br>

### 1. HTML
{% highlight html %}
<div class="progress_container">
    <div class="progress_now"></div>
    <img src="아이콘 경로" alt="" class="progress_icon">
</div>
{% endhighlight %}

<br>

- progress_container : 프로그레스바의 전체
- progress_now : 프로그레스바의 현재 부분

<br>
<br>

### 2. CSS
{% highlight css %}
.progress_container {
    height: 5px;  /* 프로그레스바 전체 높이 */  
    width: 80vw;  /* 프로그레스바 전체 넓이 */ 
    border: 1px solid var(--color-button);  /* 프로그레스바 경계선 */
}

.progress_now {
    height: 5px;  /* 전체 높이와 똑같이 */
    width: calc(100/6*1%);  
    background-color: var(--color-button);  /* 프로그레스바가 채워질때 색 */
}

.progress_icon {
    transform: translate(-60%, -60%);  /* 예시 */
    left: calc(100/6*1%);  /* 중요 */
}
{% endhighlight %}

<br>

- progress_now
    - 페이지가 넘어갈 때마다 프로그레스바에 채워지는 부분이 점점 늘어나야 한다. 
    - height은 progress_container와 똑같이 해주고,
    - width은 페이지가 넘어갈 때마다 바뀌어야 하므로 계산해주는 calc()를 이용 -> 100/(문제수)*현재페이지%
    - 만약 총 8문제이고 현재 2번째 페이지이면 width: calc(100/8*2%); 

<br>

- progress_icon
    - 페이지가 넘어갈 때마다 진행되는 프로그레스바와 함께 아이콘이 함께 움직여야 한다.
    - 위치를 transform 속성을 사용해서 프로그레스바의 위치로 옮겨주고,
    - left 속성으로 프로그레스바가 이동한 만큼 오른쪽으로 이동시켜 주었다.

<br>
<br>

