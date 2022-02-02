# git

## 本地库

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
>$ git reset --hard 70e3003//回到已经删掉的版本号版本，不用写全
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

### 查看过去使用的命令

>
>
>```git
>$ git reflog
>```
>
>

### 撤销修改

>
>
>```git
>$ git checkout -- readme.txt
>```
>
>就是让这个文件回到最近一次`git commit`或`git add`时的状态。

### 从版本库中删除文件

>
>
>```
>$ git rm readme.txt
>
>$ git commit -m "del readme file"
>```
>
>

## 远程库

### 建立连接

>
>
>```git
>$ git remote add origin git@github.com:wguanga/gitstudy.git
>```
>
>

### 推送到远程库

>
>
>```git
>$ git push -u origin master
>```
>
>-u参数在第一次推送时使用，将本地库与远程库的master分支关联起来，之后推送或拉取时不再需要。

### 删除远程库

>查看远程库信息
>
>```git
>$ git remote -v
>```
>
>删除远程库
>
>```git
>$ git remote rm origin
>```
>
>

### 从远程库拉取

>
>
>```
>$ git clone git@github.com:wguanga/gitname.git
>```

## 分支管理

### 创建分支

>
>
>```
>$ git checkout -b dev
>$ git switch -c dev
>```
>
>-b表示创建并切换到dev分支,上述两句效果一样
>
>```git
>$ git branch         //查看所有分支
>$ git branch dev     //创建dev分支
>```
>
>

### 切换分支

>
>
>```git
>$ git checkout master
>$ git switch master
>```
>
>

### 合并分支

>
>
>```git
>$ git merge dev
>```
>
>将dev分支的工作合并到当前分支中

### 删除分支

>
>
>```git
>$ git branc -d dev
>```
>
>