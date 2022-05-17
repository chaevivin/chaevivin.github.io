---
title: 3. CSS 선택자 (Selector)
categories: [CSS]
comments: true
---

# 선택자 (Selector) 종류

1. 전체 선택자 : 전체 요소 선택
{% highlight css %}
* {
	color: red;
}
{% endhighlight %}

<br>

2. 태그 선택자 : 태그 이름으로 선택
    - HTML에 있는 해당 태그 모두 선택
    - 앞,뒤에 기호 없으면 태그 선택자
{% highlight css %}
div {
    color: yellow;
}
{% endhighlight %}

<br>

3. 클래스 선택자 (.) : HTML 태그의 클래스 값으로 선택
    - 활용도 굿 👍
{% highlight CSS %}
.test {
    color: yellow;
}
{% endhighlight %}
{% highlight html %}
<div class="test">banana</div>
{% endhighlight %}

<br>

4. 아이디 선택자 (#) : HTML 태그의 ID 값으로 선택 (ID는 고유해야 함)
    - 중요할 때 사용
{% highlight css %}
#test {
    color: yellow;
}
{% endhighlight %}

<br>
<br>
<br>

# 복합 선택자 

1. 일치 선택자 : 여러 선택자들을 동시에 만족하는 요소 선택 (EF)
{% highlight css %}
div.test {  /* <div>태그와 test 클래스를 갖고 있는 요소 선택 */
    color: yellow;
}
{% endhighlight %}
{% highlight html %}
<span class="test">banana</span>
<div class="test">banana</div>  <!-- 선택 -->
{% endhighlight %}

<br>

2. 자식 선택자 : 어떤 선택자의 자식 요소를 선택 (E > F)
    - E (조건) > F (실제로 찾아야 되는 것)
{% highlight css %}
div > .test {  /* <div>태그의 자식 요소 중에 test 클래스를 갖고 있는 요소 선택 */
    color: yellow;
}
{% endhighlight %}
{% highlight html %}
<div>
    <span class="test">banana</span>  <!-- 선택 -->
</div>
<span class="test">banana</span>
{% endhighlight %}

<br>

<br>
<br>
<br>

# 가상 클래스 선택자

1. hover : 어떤 요소에 마우스를 올리고 있는 동안에만 그 요소 선택
{% highlight css %}
div {
    color: yellow;
}
div:hover {  /* <div> 태그에 마우스를 올리면 색이 yellow -> red */
    color: red;
}
{% endhighlight %}

<br>

2. active : 요소를 마우스를 클릭하는 동안에만 그 요소 선택
{% highlight css %}
div {
    width: 100px;
    height: 100px;
    background: yellow;
}
div:hover {  /* <div> 태그를 클릭했을 때 yellow -> red */
    background: red;
}
{% endhighlight %}

<br>

3. First Child : 형제 요소들 중 첫번째 요소 선택
{% highlight css %}
li: first-child {
    color: yellow;
}
{% endhighlight %}
{% highlight html %}
<ul>
    <li>banana</li>  <!-- 선택 -->
    <li>peach</li>
    <li>apple</li>
</ul>
{% endhighlight %}

<br>

4. Last Child : 형제 요소들 중 마지막 요소 선택
{% highlight css %}
li: first-child {
    color: yellow;
}
{% endhighlight %}
{% highlight html %}
<ul>
    <li>banana</li>  
    <li>peach</li>
    <li>apple</li>  <!-- 선택 -->
</ul>
{% endhighlight %}

<br>

5. nth Child : 형제 요소들 중 n번째 요소 선택
    - 0번째는 존재하지 않으므로 선택되지 않음
{% highlight css %}
li: nth-child(2n) {  /* 짝수번째 요소들만 선택 */
    color: yellow;
}
{% endhighlight %}
{% highlight html %}
<ul>
    <li>banana</li>  
    <li>peach</li>  <!-- 선택 -->
    <li>apple</li>
    <li>orange</li>  <!-- 선택 -->
</ul>
{% endhighlight %}

<br>

{% highlight css %}
li: nth-child(n+3) {  /* 3번째 요소부터 이후 요소들 선택 */
    color: yellow;
}
{% endhighlight %}
{% highlight html %}
<ul>
    <li>banana</li>  
    <li>peach</li>  
    <li>apple</li>  <!-- 선택 -->
    <li>orange</li>  <!-- 선택 -->
</ul>
{% endhighlight %}

<br>

6. 부정 선택자 : S가 아닌 E 선택 (E:not(S))
{% highlight css %}
li: not(.apple) {  /* apple 클래스 빼고 li 태그 모두 선택 */
    color: yellow;
}
{% endhighlight %}
{% highlight html %}
<ul>
    <li>banana</li>  <!-- 선택 -->
    <li>peach</li>  <!-- 선택 -->
    <li class="apple">apple</li>  
    <li>orange</li>  <!-- 선택 -->
</ul>
{% endhighlight %}