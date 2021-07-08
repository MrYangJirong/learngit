[TOC]

##### 一.开始

###### 1.概念

![image-20210708201132660](https://i.loli.net/2021/07/08/rjREZ1uM5vowxiK.png)

![image-20210708201432165](https://i.loli.net/2021/07/08/RxdBVIjhk4U9FZL.png)

###### 2.简单命令

1.1`git init`：初始化git仓库

1.2`git add`：把文件添加到**暂存区**（称为stage或者index），`git add readme.txt`,可以一次add多个文件：`git add file2.txt file3.txt`。**`commit`新文件或者修改的已有文件都执行本命令**。

1.3`git commit`：把暂存区的所有内容提交到当前分支，`git commit -m "wrote a readme file"`，`-m`后面输入的是本次提交的说明，`commit`可以一次提交很多文件。`commit`相当于一个本地快照。

1.4 `git status`：查看仓库当前的状态（是否有修改）。

1.5 `git diff`：查看某个文件的修改`git diff readme.txt` ，`git diff HEAD -- readme.txt` 。

1.6`git log`：显示提交日志（不包括回退的版本）。可以使用`git log --pretty=oneline`显示简略版的提交日志。

1.7`git reset`：回退版本、丢弃工作区或暂存区的修改。

​	A.回退版本：`git reset --hard 版本号`或`git reset --hard HEAD~2`(回退到前2个版本)。在Git中，用`HEAD`表示当前版本，上N个版本是`HEAD~N`。

​	B.丢弃工作区修改：`git restore readme.txt`。

​	C.丢弃暂存区修改：把暂存区的修改丢回工作区`git restore --staged readme.txt`

1.8`git reflog`：查看命令历史，可以查看到所有的提交记录。可以用这个命令查看版本号然后回退到相应版本。

1.9`git rm`：删除文件。从版本库中删除某文件`git rm test.txt`。

1.10`git restore`：恢复已删除的文件。恢复某文件`git restore test.txt`。

1.11关联一个远程仓库，使用命令：`git remote add origin git@server-name:path/repo-name.git`。关联一个远程库时必须给远程库指定一个名字，`origin`是默认习惯命名；关联后，使用命令`git push -u origin master`第一次推送master分支的所有内容；此后，每次本地提交后，只要有必要，就可以使用命令`git push origin master`推送最新修改；

