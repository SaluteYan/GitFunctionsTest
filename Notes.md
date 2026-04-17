# Git Learning Notes

[TOC]

## 配置

`git config` 用来配置或读取相应的工作环境变量，这些变量可以存放在以下三个不同的地方：

* Git/etc/gitconfig 文件：系统中对所有用户都普遍适用的配置，若使用 git config 时用 --system 选项，读写的就是这个文件
* ~/.gitconfig 文件：用户目录下的配置文件只适用于该用户，若使用 git config 时用 --global 选项，读写的就是这个文件
* 当前项目的 Git 目录中的配置文件（也就是工作目录中的 .git/config 文件）

### 配置用户信息

配置个人的**用户名称**和**电子邮件地址**，这是为了在每次提交代码时记录提交者的信息：

```bash {.line-numbers}
    git config --global user.name "runoob"
    git config --global user.email test@runoob.com
```

***Remark***: 如果用了 --global 选项，那么更改的配置文件就是位于你用户主目录下的那个，以后你所有的项目都会默认使用这里配置的用户信息；如果要在某个特定的项目中使用其他名字或者电邮，只要去掉 --global 选项重新配置即可，新的设定保存在当前项目的 .git/config 文件里

### 查看配置信息

`git config --list` 检查已有的配置信息，空格实现翻页，q退出查看

### 生成SSH密钥

如果你需要通过 SSH 进行 Git 操作，可以生成 SSH 密钥并添加到你的 Git 托管服务（如 GitHub、GitLab 等）上

