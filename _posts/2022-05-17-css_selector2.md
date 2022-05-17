---
title: 4. CSS 선택자 (Selector) - 가상요소선택자
categories: [CSS]
comments: true
---

# 가상요소 선택자
✨ 가상요소 선택자를 사용할 때는 무조건 "content"라는 속성을 써줘야 한다. ✨

<br>

- before : E 요소 내부의 앞에 내용(content) 삽입 (E::before)
{% highlight html %}
<div>1</div>
<div>2</div>
<div>3</div>
{% endhighlight %}
{% highlight css %}
div::before {  /* 모든 <div>태그 앞에 "number"라는 내용이 붙음 -> number1 */
    content: "number";
}
{% endhighlight %}

<br>

- after : E 요소 내부 뒤에 내용 삽입 (E::after)
{% highlight html %}
<div>1</div>
<div>2</div>
<div>3</div>
{% endhighlight %}
{% highlight css %}
div::before {  /* 모든 <div>태그 뒤에 "number"라는 내용이 붙음 -> 1number */
    content: "number";
}
{% endhighlight %}

<br>
<br>
<br>