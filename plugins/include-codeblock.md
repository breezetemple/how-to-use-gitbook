# Include Codeblock

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
