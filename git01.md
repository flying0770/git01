## 下载git

下载地址：https://git-scm.com/download/win

## 安装



## git 工作流程

### 创建本地仓库并提交

本地工作目录

暂存区

本地git仓库

git status：查看暂存区内容

git add： 把本地工作目录提交到暂存区

git commit -m ''：把暂存区内容提交到git本地仓库

git log：查看提交日志

git add .：把当前目录所有文件都提交到暂存区

本地工作目录必须先提交到暂存区，再提交到git本地仓库，否则提交失败

git diff HEAD -- 文件名：查看本地工作目录和暂存区对应文件的区别

git reset HEAD 文件名：取消上一次本地工作目录提交到暂存区的操作

### 版本回退

git log：查看版本记录

提交次数过多之后，使用git log 命令行放不下，回车显示所有内容后，输入q退出，或者使用 git log --pretty=oneline

git reset --hard HEAD^：向上回退一个版本，即把git本地仓库中的上一个版本内容覆盖到当前工作目录中

git reset --hard HEAD~3：向上回退三个版本

git reset --hard commit唯一版本号：回退到指定版本

git reflog：获取版本标识

### 删除文件

git ls-files：查看git本地仓库所有文件

删除文件：

1. 直接在本地工作目录中删除，然后再次提交
2. git rm 文件名，直接删除git本地仓库和本地工作目录文件

## 远程仓库

### 下载

1. 直接下载zip文件

2. git clone github仓库地址

3. SSH

   生产ssh公钥，绑定github

### 推送本地仓库到github

git branch -M master

git remote add origin g git@github.com:flying0770/git01.git

git push -u origin master

### git本地分支操作

git branch：查看分支，带*为当前分支

git checkout -b 分支名：新建分支，新建的分支即包含主分支所有内容

git checkout 分支名：切换分支

git branch -m 原分支名 新分支名：分支重命名

##### 合并分支内容到主干

先切换到主干，git checkout master,再合并分支，git merge 分支名

git branch -d 分支名：删除分支

### git远程分支操作

git branch -a：获取本地和远程所有分支

git push origin 分支名：把本地分支推送到远程分支

git push origin :分支名：删除远程分支

git fetch：获取远程分支的最新状态

git checkout -b 本地分支名 origin/远程分支名：把远程分支拉取到本地

##### 尽可能在推送之前先拉取最新代码，再推送

git pull：拉取最新文件

### 标签管理

git tag：获取所有标签

git tag 标签名：默认给最后一次提交添加标签

git push origin 标签名：把标签名推送到远程

git push origin --tags：把本地所有标签推送到远程

git tag -d 标签名：删除本地标签

git push origin :refs/tags/标签名：删除远程标签





测试标签
