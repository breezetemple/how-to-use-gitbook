# 编辑书籍

创建了书籍后，可以使用免费的在线编辑器进行编辑，
也可以使用 [gitbook editor](https://github.com/GitbookIO/editor) 编辑，甚至使用任何喜欢的文本编辑器来编辑。

## 在线编辑

点击 `Edit your book` 进入在线编辑器

## 本地安装Gitbook Editor

`gitbook editor` 实际上就是一个本地应用版的在线编辑器，使用方式和在线编辑器类似，所见即所得

## Git & Markdown

使用文本编辑器，编写 `Markdown` 文档，然后，使用 `Git` 提交到书籍的远程项目，
提交前，最好在本地使用 `gitbook` 预览效果；
提交后，GitBook.com 会自动生成更新书籍的内容。

### 建立初始化git仓库

GitBook.com 上的每本书都使用 Git 项目来管理.
所以，这里首先需要建立需要编辑书籍的 Git 项目，[教程](https://help.gitbook.com/books/how-can-i-use-git.html)

Create a new repository on the command line:

```bash
touch README.md SUMMARY.md
git init
git add README.md SUMMARY.md
git commit -m "first commit"
git remote add gitbook https://git.gitbook.com/{{UserName}}/{{Book}}.git
git push -u -f gitbook master
```

Push an existing repository
```bash
git remote add gitbook https://git.gitbook.com/{{UserName}}/{{Book}}.git
git push -u -f gitbook master
```

从`/settings/Publication/Git URL`得到仓库地址：

```bash
$ git clone https://git.gitbook.com/breezetemple/how-to-use-gitbook.git
正克隆到 'how-to-use-gitbook'...
Username for 'https://git.gitbook.com': breezetemple
Password for 'https://breezetemple@git.gitbook.com': 
remote: Counting objects: 9, done.
remote: Compressing objects: 100% (7/7), done.
remote: Total 9 (delta 1), reused 9 (delta 1)
展开对象中: 100% (9/9), 完成.
检查连接... 完成。

$ l
总用量 28K
 .  ..  chapter1.md .git .gitignore README.md SUMMARY.md
```
### 编辑内容

编辑 `README.md` 、`SUMMARY.md` 以及各章节内容，完成后提交

```bash
git ci -a "init book"
```

### 发布

推送到gitbook以完成发布

```bash
git push
```

### 阅读地址

`https://breezetemple.gitbooks.io/how-to-use-gitbook`




