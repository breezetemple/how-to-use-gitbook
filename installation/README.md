# 安装

* **环境**

> ubuntu 15.10 X64

* **安装nodejs**

```bash
sudo apt-get update
sudo apt-get install nodejs 
sudo apt-get install npm
```

* **验证**

```bash
$ node -v
v0.12.2
$ npm -v
2.7.4
```

* **安装gitbook**

```bash
$ > sudo npm install -g gitbook-cli
/usr/local/bin/gitbook -> /usr/local/lib/node_modules/gitbook-cli/bin/gitbook.js
gitbook-cli@2.1.3 /usr/local/lib/node_modules/gitbook-cli
├── bash-color@0.0.3
├── q@1.4.1
├── semver@5.1.0
├── lodash@4.5.1
├── tmp@0.0.28 (os-tmpdir@1.0.1)
├── commander@2.9.0 (graceful-readlink@1.0.1)
├── optimist@0.6.1 (wordwrap@0.0.3, minimist@0.0.10)
├── npm@3.7.5
├── user-home@2.0.0 (os-homedir@1.0.1)
├── fs-extra@0.26.5 (klaw@1.2.0, jsonfile@2.3.0, graceful-fs@4.1.4, path-is-absolute@1.0.0, rimraf@2.5.2)
└── npmi@1.0.1 (semver@4.3.6, npm@2.15.5)
```

必须使用`sudo`来执行安装


* **验证gitbook**

```bash
$ > gitbook version
2.1.3
```
