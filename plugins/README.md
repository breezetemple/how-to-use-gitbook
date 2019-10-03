# 插件

gitbook 还支持许多插件，用户可以从 [NPM](https://www.npmjs.com) 上搜索 gitbook 的插件，
[gitbook 文档](https://github.com/GitbookIO/plugin) 推荐插件的命名方式为：

- gitbook-plugin-X: 插件
- gitbook-theme-X: 主题

所以，可以通过以上两种方式来搜索 gitbook 的插件或者主题。

* [Codeblock-filename](#codeblock-filename)
* [Emphasize - 为文字加上底色](#emphasize)
* [Include Codeblock - 用代码块显示包含文件的内容](#include-codeblock)
* [KaTex - 用于支持数学公式](#katex)
* [mathjax - 用于编辑数学公式](#mathjax)
* [mermaid - 编辑显示流程图](#mermaid)
* [multipart - 将书籍分成几个部分](#multipart)
* [PlanUML - 编辑显示UML](#uml)
* [Splitter - 侧边栏的宽度可以自由调节](#splitter)
* [Anchor-navigation-ex - 添加Toc到侧边悬浮导航以及回到顶部按钮](#anchor-navigation-ex)
* [Ace Plugin - 支持ace](#ace-plugin)


## Codeblock-filename

[codeblock-filename](https://plugins.gitbook.com/plugin/codeblock-filename)为代码块添加文件名称

```json
plugins: [ "codeblock-filename" ] 
```
使用示例:  

```bash
''':helloworld
helloworld
'''

'''js:test.js
console.log("test");
'''
```

```:helloworld
helloworld
```

```js:test.js
console.log("test");
```

## Emphasize

[Emphasize](https://plugins.gitbook.com/plugin/emphasize)为文字加上底色

```bash
"plugins": ["emphasize"]
gitbook install
```

使用方式：

```bash
This text is {% em %}highlighted !{% endem %}

This text is {% em %}highlighted with **markdown**!{% endem %}

This text is {% em type="green" %}highlighted in green!{% endem %}

This text is {% em type="red" %}highlighted in red!{% endem %}

This text is {% em color="#ff0000" %}highlighted with a custom color!{% endem %}
```

效果：

This text is {% em %}highlighted !{% endem %}

This text is {% em %}highlighted with **markdown**!{% endem %}

This text is {% em type="green" %}highlighted in green!{% endem %}

This text is {% em type="red" %}highlighted in red!{% endem %}

This text is {% em color="#ff0000" %}highlighted with a custom color!{% endem %}


## Include Codeblock

[Include Codeblock](https://plugins.gitbook.com/plugin/include-codeblock)使用代码块的格式显示所包含文件的内容. 该文件必须存在.

```json
"plugins": [
    "include-codeblock"
]
```

使用示例:

```bash
'''bash
{import}(path/to/file)
'''
```

也可以显示文件中的代码段：

```bash
{include:30-40}(path/to/file)
```

使用`[]` 代替 `{}`，` 代替 '效果：

```bash
[import](../book.json)
```

[include:30-40](../book.json)


## KaTex

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


## mathjax

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


## mermaid

[gitbook-plugin-mermaid-gb3](https://github.com/chriswessels/gitbook-plugin-mermaid-gb3)用于编辑显示流程图：


```bash
npm install gitbook-plugin-mermaid-gb3
"plugins": ["mermaid-gb3"]
```

或者：

```bash
"plugins": ["mermaid-gb3"]
gitbook install
```

使用方式：

```
(```mermaid)
graph TD;
  A-->B;
  A-->C;
  B-->D;
  C-->D;
(```)
```

生成如下：

```mermaid
graph TD;
  A-->B;
  A-->C;
  B-->D;
  C-->D;
```


## multipart

[multipart](https://www.npmjs.com/package/gitbook-plugin-multipart) 插件可以将书籍分成几个部分，例如：

- GitBook Basic
- GitBook Advanced

对有非常多章节的书籍非常有用，分成两部分后，各个部分的章节都从 1 开始编号。

安装及配置:

和安装其它插件一样，执行以下命令：

```bash
$ sudo npm install gitbook-plugin-multipart -g
```

然后编辑 `book.json` 添加 multipart 到 plugins 中：

```bash
"plugins": [
    "multipart"
],
```

或者可以在编辑完 `book.json` 后，执行如下命令安装：

```bash
$ gitbook install
info: 1 plugins to install 
info: No version specified, resolve plugin multipart 
info: install plugin multipart from npm (gitbook-plugin-multipart) with version 0.3.0 
gitbook-plugin-multipart@0.3.0 node_modules/gitbook-plugin-multipart
└── cheerio@0.17.0 (entities@1.1.1, dom-serializer@0.0.1, lodash@2.4.2, CSSselect@0.4.1, htmlparser2@3.7.3)
info: >> plugin multipart installed with success 
```

警告：

```bash
warn: Hook "summary:before"" used by plugin "gitbook-plugin-multipart" has been removed or is deprecated 
warn: Hook "page:after"" used by plugin "gitbook-plugin-multipart" has been removed or is deprecated 
```

Gitbook 2.0.1 has removed `page:after` & `summary:before` hook which this plugin needs.


## UML

[PlantUML in GitBook](https://github.com/GitbookIO/plugin-puml)

安装

```bash
npm install gitbook-plugin-puml
"plugins": ["puml"]
```

或者

```bash
"plugins": ["puml"]
gitbook install
```

```uml
{% plantuml %}

Class Stage
Class Timeout {
    +constructor:function(cfg)
        +timeout:function(ctx)
        +overdue:function(ctx)
        +stage: Stage
}
Stage <|-- Timeout

{% endplantuml %}
```

{% plantuml %}
Bob->Alice : hello
{% endplantuml %}


{% plantuml %}
object john {
    name = 'John'
    birth = 1985
}
{% endplantuml %}


{% plantuml %}
Class Stage
Class Timeout {
    +constructor:function(cfg)
        +timeout:function(ctx)
        +overdue:function(ctx)
        +stage: Stage
}
Stage <|-- Timeout
{% endplantuml %}


## Splitter

[Splitter](https://plugins.gitbook.com/plugin/splitter)使侧边栏的宽度可以自由调节

```json
"plugins": [
    "splitter"
]
```

```bash
gitbook install
```

[效果](https://raw.githubusercontent.com/yoshidax/gitbook-plugin-splitter/master/gitbook-splitter-demo.gif)

## Anchor-navigation-ex

添加Toc到侧边悬浮导航以及回到顶部按钮。需要注意以下两点：
* 本插件只会提取 h[1-3] 标签作为悬浮导航
* 只有按照以下顺序嵌套才会被提取
```
# h1
## h2
### h3
必须要以 h1 开始，直接写 h2 不会被提取
## h2
```

[插件地址](https://plugins.gitbook.com/plugin/anchor-navigation-ex)
```json
{
    "plugins": [
        "anchor-navigation-ex"
    ],
    "pluginsConfig": {
        "anchor-navigation-ex": {
            "isRewritePageTitle": true,
            "isShowTocTitleIcon": true,
            "tocLevel1Icon": "fa fa-hand-o-right",
            "tocLevel2Icon": "fa fa-hand-o-right",
            "tocLevel3Icon": "fa fa-hand-o-right"
        }
    }
}
```

`<extoc></extoc>` 会在此处生成`TOC`目录


## Ace Plugin

[插件地址](https://plugins.gitbook.com/plugin/ace)  

使 GitBook 支持ace 。默认情况下，line-height 为 1，会使代码显得比较挤，而作者好像没提供修改行高的选项，如果需要修改行高，可以到 `node_modules -> github-plugin-ace -> assets -> ace.js` 中加入下面两行代码 (30 行左右的位置)：
```js
editor.container.style.lineHeight = 1.25;
editor.renderer.updateFontSize();
```
不过上面的做法有个问题就是，每次使用 `gitbook install` 安装新的插件之后，代码又会重置为原来的样子。另外可以在 `website.css` 中加入下面的 css 代码来指定 ace 字体的大小
```css
.aceCode {
  font-size: 14px !important;
}
```

使用插件：
```json
"plugins": [
    "ace"
]
```
使用示例:

{%ace edit=true, lang='c_cpp'%}
// This is a hello world program for C.
#include <stdio.h>

int main(){
  printf("Hello World!");
  return 1;
}
{%endace%}
