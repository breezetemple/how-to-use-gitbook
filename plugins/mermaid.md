# mermaid

[gitbook-plugin-mermaid](https://github.com/JozoVilcek/gitbook-plugin-mermaid)用于编辑显示流程图：


```bash
npm install gitbook-plugin-mermaid
"plugins": ["mermaid"]
```

或者：

```bash
"plugins": ["mermaid"]
gitbook install
```

使用方式：

```bash
{% mermaid %}
graph TD;
A-->B;
A-->C;
B-->D;
C-->D;
{% endmermaid %}
```

生成如下：

{% mermaid %}
graph TD;
A-->B;
A-->C;
B-->D;
C-->D;
{% endmermaid %}
