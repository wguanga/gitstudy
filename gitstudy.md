# git

### 安装初始化

>
>
>```git
>$ git config --global user.name "yourname"
>$ git config --global user.email "youremail"
>```
>
>--global参数是设置这台机器上所有用户的git使用

### 创建库

>
>
>```git
>$ git init
>```
>
>

### 添加提交文件

>
>
>```git
>$ git add readme.txt
>
>$ git commit -m "wrote a readme file"
>```
>
>commit将上方所有的添加全部提交

### 回滚

>
>
>```git
>$ git reset --hard HEAD^
>```
>
>HEAD是当前版本，HEAD^是上一个版本，HEAD^^是上上个版本，HEAD~100是上100个版本

### 查看版本

>
>
>```git
>$ git log
>
>$ git log --pretty=oneline
>```
>
>

查看过去使用的命令

>
>
>```git
>$ git reflog
>```
>
>