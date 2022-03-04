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

git reset --hard HEAD~3：向上回退到第三次提交