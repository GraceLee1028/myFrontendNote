#  分支管理
> `git switch -c dev`:创建并切换到新的dev分支；【分支切换常用switch】

> `git switch master`：直接切换到已有的master分支【或者git checkout master】

> `git checkout -b dev`:创建dev分支，然后切换到dev分支：git checkout命令加上-b参数表示创建并切换，相当于以下两条命令 [git branch , git checkout]

     `git branch`:  查看当前所有分支，当前分支前面会标一个*号 
     `git branch 新的分支名`: 创建分支  
     `git checkout 分支名`: 切换到某分支

> `git merge 指定分支` ：合并某分支到当前分支：这次合并是“快进模式”，也就是直接把master指向dev的当前提交 

> `git branch -d 指定分支`： 删除某指定分支  

>`git merge --no-ff -m "merge with no-ff" dev` :准备合并dev分; --no-ff参数，表示禁用Fast forward；本次合并要创建一个新的commit，所以加上-m参数，把commit描述写进去
# 常用命令

* git init 把这个目录变成Git可以管理的仓库
    > `git init` 

*****
* git add:告诉Git，把文件添加到仓库  
注解：_把文件修改添加到暂存区_
    > `git add 文件名`

    > `git add 文件名1 文件名2`

* git commit:告诉Git，把文件提交到仓库；-m后面输入的是本次提交的说明  
注解：_暂存区的所有内容提交到当前分支_
    > `git commit -m "提交注释"`

    ###  提交修改和提交新文件都有执行两步：git add 和 git commit
* git checkout：让这个文件回到最近一次git commit或git add时的状态
    > `git checkout -- 文件名`  
注解：_丢弃工作区的修改_，git checkout其实是用版本库里的版本替换工作区的版本，无论工作区是修改还是删除，都可以“一键还原
* git rm:从版本库中删除该文件
    > `git rm 文件名`：执行后要再执行git commit

* git remote:关联一个远程库;[在本地创建了一个Git仓库后，又想在GitHub创建一个Git仓库，让这两个仓库进行远程同步]
    > `git remote add origin https://github.com/lifengand1992/gitNote.git`:
    https://github.com/lifengand1992/gitNote.git :远程仓库地址 

    注解：_添加后，远程库的名字就是origin；这是Git默认的叫法，也可以改成别的_
* git push:把本地库的所有内容推送到远程库上
    > `git push -u origin master`：第一次推送master分支的所有内容
    > `git push origin master`：推送最新修改
*****
* git reset:版本回退
    > `git reset --hard HEAD^`: 回退到上一个版本 

    > `git reset --hard 1094a`: 回退到某一版本，1094a:表示某一版本的版本号的开头几位
* git status:仓库当前的状态
    > `git status`

* git diff:查看具体修改的内容
    > `git diff`
* git log:从近至远显示提交日志
    > `git log`
* git reflog:用来记录你的每一次命令
    > `git relog`

*****
* git的特点：  
    >为什么Git比其他版本控制系统设计得优秀，因为Git跟踪并管理的是修改，而非文件








