# this is my first git repository!

## git command with notes
>http://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000

- git config --list
- git config --global user.name "xxx"
- git config --global user.email "xxx@xxx"

- git init 
创建仓库

- git add 
添加新的需要跟踪的文件到仓库，或者更新状态

- git commit -m "xxxxxx" 
提交更新

- git status 
查看仓库状态

- git diff 
查看文件改动状态

- git log 
查看仓库改动日志
- git log --pretty=oneline

- git reflog 
查看仓库改动情况

- git reset --hard commit_id 
HEAD 指向当前版本 HEAD^ 回到上一个版本 HEAD~100 表示 回到前100个版本

- git checkout -- file
丢弃工作区的修改
恢复file到版本库中的状态

- git reset HEAD file 
丢弃暂存区的修改，此时仅含有工作区的修改

- git rm file
从版本库中删除file，记得commit

- git remote add origin git@server-name:path/repo-name.git；
关联一个远程库

- git push -u origin master
关联后，使用命令第一次推送master分支的所有内容；
- git push origin master
将本地master分支推送到github

- git clone git@github.com:username/repo-name.git
克隆仓库到本地

- git branch
查看分支

- git branch <name>
创建分支：

- git checkout <name>
切换分支：

- git checkout -b <name>
创建+切换分支

- git merge <name>
合并某分支到当前分支

- git branch -d <name>
删除分支

- git log --graph --pretty=oneline --abbrev-commit
以图形式查看仓库日志

- git merge --no-ff -m "xx" dev
将合并作为一次commit记录

- git stash
保存工作现场

- git stash list 
查看工作现场列表

- git stash apply stash@{0}
恢复现场

- git stash drop stash@{0}
删除保存的现场

- git stash pop
从顶部恢复并删除

- git branch -D branch name
强制删除

- git remote [-v]
查看远程库 [详细信息]

- git push origin branch-name
从本地推送分支，如果推送失败，先用git pull

- git pull 
抓取远程的分支，如果有冲突，要先处理冲突

- git checkout -b branch-name origin/branch-name
在本地创建和远程分支对应的分支,本地和远程分支的名称最好一致

- git branch --set-upstream branch-name origin/branch-name
建立本地分支和远程分支的关联

- git tag <name> [commit_id]
用于新建一个标签，默认为HEAD，也可以指定一个commit id；

- git tag -a <tagname> -m "blablabla..."
指定标签信息

- git tag -s <tagname> -m "blablabla..."
用PGP签名标签

- git tag
查看所有标签。

- git push origin <tagname>
推送一个本地标签

- git push origin --tags
推送全部未推送过的本地标签

- git tag -d <tagname>
删除一个本地标签

- git push origin :refs/tags/<tagname>
删除一个远程标签
