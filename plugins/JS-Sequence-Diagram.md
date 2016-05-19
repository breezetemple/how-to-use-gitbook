# JS Sequence Diagram

[JS Sequence Diagram Plugin](https://github.com/gmassanek/gitbook-plugin-js-sequence-diagram)用于编辑流程图

```bash
sudo npm install gitbook-plugin-js-sequence-diagram
"plugins": ["js-sequence-diagram"]
```

或者：

```bash
"plugins": ["js-sequence-diagram"]
gitbook install
```

使用方式:

```bash
'''sequence
Title: Here is a title
A->B: Normal line
B-->C: Dashed line
C->>D: Open arrow
D-->>A: Dashed open arrow
'''
```

注意：  *'* 替换为 *`*

生成如下：

```sequence
Title: Here is a title
A->B: Normal line
B-->C: Dashed line
C->>D: Open arrow
D-->>A: Dashed open arrow
```

