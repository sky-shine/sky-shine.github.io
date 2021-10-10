---
title: "git"
excerpt: "Post displaying uses of git"
header:
  teaser: "assets/images/markup-syntax-highlighting-teaser.jpg"
tags: 
  - code
  - git
---
# Git命令

新建文件夹 然后git init

git remote add + 名字+连接地址

ep:   git remote add origin http://github.com/xxx

文件上传 git add -A 提交所有变化

向新的空仓库推文件 git push -u 仓库名  分支

查看提交记录 git log

回退以前提交的版本 git reset  - - hard <commit的id>

撤销回退，利用git reflog，该命令记录每一次命令

## SSH

~/.ssh或者~/.ssh ls 查看电脑上是否有ssh文件夹

创建SSHkey

ssh-keygen -t rsa -C "your email"

然后输入文件名保存key代码，默认生成id_rsa和id_rsa.pub两个秘钥文件

然后设置密码和确认密码

github上的setting设置SSH

~/.ssh ls找到SSHkey所在位置，用记事本打开id_rsa.pub文件，将其内容复制到github设置里

输入ssh -T git@github.com

…or create a new repository on the command line

```c
echo "# git_test" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/sky-shine/git_test.git
git push -u origin main
```

…or push an existing repository from the command line

```c
git remote add origin https://github.com/sky-shine/git_test.git
git branch -M main
git push -u origin main
```

```c
//first step:
git init
git clone + repo's address
git remote add origin(the name we call remote repo)+repo's address

//update step:
git pull origin

//create new branch step:
git branch 'new branch '

//change to new branch step:
git checkout 'new branch'

//push new file step:
git add -A
commit -m "comment"

//push file step:
git push origin+ new branch's name

//look at push history
git log

//delete remote branch
git push origin --delete branch's name
//delete local branch
git branch -d local branch's name

//create new local branch
git checkout -b new branch's name
//create new remote branch
git push origin branch's name:branch's name

//relate to remote branch
git branch --set-upstream-to=origin/new remote branch's name

//look at branch information
git branch -vv

```

```c
git stash list
git stash clear
git pull origin master
```

update local tags

```c
git fetch --tags -f
```