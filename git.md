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


    testetsts
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








