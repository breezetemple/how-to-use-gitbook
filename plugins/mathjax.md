# mathjax

[GitBook plugin-mathjax](https://github.com/GitbookIO/plugin-mathjax)用于编辑数学公式


```bash
npm install gitbook-plugin-mathjax
"plugins": ["mathjax"]
```

或者：

```bash
"plugins": ["mathjax"]
gitbook install
```


使用方式：使用 `$$` 将公式包括起来：

```bash
{% math %}f(x)=a+b{% endmath %}
{% math %}(ax^2 + bx + c = 0){% endmath %}
{% math %}x = {-b \pm \sqrt{b^2-4ac} \over 2a}.{% endmath %}
```

如下：

When {% math %}a \ne 0{% endmath %}, there are two solutions to {% math %}(ax^2 + bx + c = 0){% endmath %} and they are {% math %}x = {-b \pm \sqrt{b^2-4ac} \over 2a}.{% endmath %}

{% math %}f(x)=a+b{% endmath %}

{% math %}(ax^2 + bx + c = 0){% endmath %}

{% math %}x = {-b \pm \sqrt{b^2-4ac} \over 2a}.{% endmath %}

