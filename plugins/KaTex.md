# KaTex

[KaTex](https://plugins.gitbook.com/plugin/katex)用于支持数学公式，官网上说`Katex`速度要快于`MathJax`。

[MathJax使用LaTeX语法编写数学公式教程](http://iori.sinaapp.com/17.html)

安装

```bash
plugins: ["katex"]
gitbook install
```

与 `MathJax` 存在冲突，需要将之屏蔽：

```bash
plugins: ["-mathjax"]
```

使用示例:

```bash
When {% math %}a \ne 0{% endmath %}, there are two solutions to {% math %}(ax^2 + bx + c = 0){% endmath %} and they are {% math %}x = {-b \pm \sqrt{b^2-4ac} \over 2a}.{% endmath %}

$$ \int_{-\infty}^\infty g(x) dx $$

$$ 1 \over 3 $$

$$ f(x,y,z) = 3y^2z \left( 3+\frac{7x+5}{1+y^2} \right) $$

$$ \sum_{i=0}^n \frac{1}{i^2} $$　　

$$\prod_{i=0}^n \frac{1}{i^2} $$
```

效果：


When {% math %}a \ne 0{% endmath %}, there are two solutions to {% math %}(ax^2 + bx + c = 0){% endmath %} and they are {% math %}x = {-b \pm \sqrt{b^2-4ac} \over 2a}.{% endmath %}

$$ \int_{-\infty}^\infty g(x) dx $$

$$ 1 \over 3 $$

$$ f(x,y,z) = 3y^2z \left( 3+\frac{7x+5}{1+y^2} \right) $$

$$ \sum_{i=0}^n \frac{1}{i^2} $$　　

$$\prod_{i=0}^n \frac{1}{i^2} $$
