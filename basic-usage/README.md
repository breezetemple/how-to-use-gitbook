# 基本使用

**README.md** 和 **SUMMARY.md** 是两个必须文件，README.md 是对书籍的简单介绍：

```bash
$ cat book/README.md 
# README

This is a book powered by [GitBook](https://github.com/GitbookIO/gitbook).
```

SUMMARY.md 是书籍的目录结构。内容如下：

```bash
$ cat book/SUMMARY.md 
# SUMMARY

* [Chapter1](chapter1/README.md)
    * [Section1.1](chapter1/section1.1.md)
    * [Section1.2](chapter1/section1.2.md)
        * [Section1.2.1](chapter1/section1.2.1.md)
* [Chapter2](chapter2/README.md)
```
不被`SUMMARY.md`包含的文件不会被gitbook处理.

* **gitbook help**

可以查看gitbook支持的命令，常用：

```bash
gitbook init
gitbook build
gitbook serve
```


* **gitbook init**

```bash
$ > gitbook init
info: init book at /data/OpenSourceCode/gitbook/test 
info: detect structure from SUMMARY (if it exists) 
info: found README.md 
info: create chapter1/README.md 
info: create chapter1/section1.1.md 
info: create chapter1/section1.2.md 
info: create chapter1/section1.2.1.md 
info: create chapter2/README.md 
info: initialization is finished 

Done, without error
$ > tree
.
├── chapter1
│   ├── README.md
│   ├── section1.1.md
│   ├── section1.2.1.md
│   └── section1.2.md
├── chapter2
│   └── README.md
├── README.md
└── SUMMARY.md

2 directories, 7 files
```

* **gitbook build**

* **gitbook serve**

书籍目录结构创建完成以后，就可以使用`gitbook serve`来编译和预览书籍了：

```bash
$ > gitbook serve
Live reload server started on port: 35729
Press CTRL+C to quit ...

info: loading book configuration....OK 
info: load plugin gitbook-plugin-highlight ....OK 
info: load plugin gitbook-plugin-search ....OK 
info: load plugin gitbook-plugin-sharing ....OK 
info: load plugin gitbook-plugin-fontsettings ....OK 
info: load plugin gitbook-plugin-livereload ....OK 
info: >> 5 plugins loaded 
info: start generation with website generator 
info: clean website generatorOK 
info: generation is finished 

Starting server ...
events.js:85
      throw er; // Unhandled 'error' event
                  ^
```

**更换端口:**

```bash
$ > gitbook serve --port 50000
Live reload server started on port: 35729
Press CTRL+C to quit ...

info: loading book configuration....OK 
info: load plugin gitbook-plugin-highlight ....OK 
info: load plugin gitbook-plugin-search ....OK 
info: load plugin gitbook-plugin-sharing ....OK 
info: load plugin gitbook-plugin-fontsettings ....OK 
info: load plugin gitbook-plugin-livereload ....OK 
info: >> 5 plugins loaded 
info: start generation with website generator 
info: clean website generator
info: OK 
info: generation is finished 

Starting server ...
Serving book on http://localhost:50000
```

`gitbook serve`命令实际上会调用`gitbook build`编译书籍，完成以后会打开一个 web 服务器，监听在本地端口

现在，可以用浏览器打开`http://localhost:50000`查看书籍的效果

在文件修改过程中，每一次保存文件，`gitbook serve`都会自动重新编译，所以可以持续通过浏览器来查看最新的书籍效果！
