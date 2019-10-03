# 配置

## GitHub 集成

`GitBook.com` 为每本书籍都创建了一个 Git 项目，并且使用这个 `Git` 项目来管理书籍.
正如在 [编辑书籍](/edit.html) 中介绍的那样，我们可以通过向书籍的 `Git` 项目提交内容来更新书籍.

另外，`GitBook.com` 还可以集成 [GitHub](https://github.com)，所以用户可以将书籍的源码通过 `GitHub` 上的项目来管理.

与Github连接 使得我可以将本地`Repo Push` 到`Github Repo` 就可以更新Gitbook书籍内容, 这个需要配置 `webhook`.

在 `/settings/GitHub` 进行设置

* `github` 中建立关联的仓库：`/Create New repository` ： `breezetemple/how-to-use-gitbook`
* `gitbook` 中关联 `github`：`/settings/GitHub/GitHub Repository` ： `breezetemple/how-to-use-gitbook`
* `gitbook` 设置 `/settings/GitHub/Integration/add webhook` ： 
>  You need to grant permissions to GitBook to manage this repository. 
* 如果出现上述提示，在 `gitbook` 中设置 `/settings/GitHub/GitHub Repository/Manage permission` ，修改为 `With access to public repository`
* 重现设置 `add webhook`

### 常见的错误

书本没有被更新/没有任何的构建

如果你连接了你的GitHub仓库至一个GitBook项目，但是编辑它的内容却没有触发GitBook任何的构建操作。验证webhook被正确的添加到了你的GitHub仓库中（GitHub仓库设置->Webhook），如果webhook不存在或无效，之后添加它到你书本的设置中。

## GitHub 测试

`GitBook` 与 `GitHub` 绑定之后，访问书籍出现如下错误：

>Bad Gateway

表示 `webhook` 设置出错，**仔细检查设置过程中出现的提示信息！！**

本地测试：

```
$ > gitbook build
info: loading book configuration....OK 
info: load plugin gitbook-plugin-highlight ....OK 
info: load plugin gitbook-plugin-search ....OK 
info: load plugin gitbook-plugin-sharing ....OK 
info: load plugin gitbook-plugin-fontsettings ....OK 
info: >> 4 plugins loaded 
info: start generation with website generator 
info: clean website generator
info: OK 
info: generation is finished 

Done, without error
```

说明你的书籍吻合 `gitbook` 规约,可以从本地编译成功，可以推送到 `GitHub`


## 绑定域名

可以绑定自己的自定义域名来进行解析到你的书籍

在 `/settings/domains` 进行设置：

[官方教程](https://help.gitbook.com/books/can-i-use-custom-domain.html)
