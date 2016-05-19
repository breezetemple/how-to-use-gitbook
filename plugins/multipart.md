# multipart

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
