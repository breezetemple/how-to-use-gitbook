# mermaid

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
