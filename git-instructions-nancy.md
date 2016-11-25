####GitHub 与 Git指令
---
1.  创建账号，登录GitHub网站 [https://github.com/](https://github.com/)

2.  Windows 上安装Git Bash，常见的几个专用名词译名：
```
* Workspace: 工作区
* Index / Stage: 暂存区
* Repository: 仓库区(或本地仓库)
* Remote: 远程仓库
```

3.  新建代码库
```
# 在当前目录新建一个Git代码库
$ git init
# 新建一个目录，将其初始化为Git代码库
$ git init [project-name]
# 下载一个项目和整个代码历史记录
$ git clone [url]
```

4. 配置
Git的设置文件为`.gitconfig`，它可以用在用户主目录下（全局配置），也可以在项目目录下（项目配置）
```
# 显示当前的Git配置
$ git config --list
# 编辑Git配置文件
$ git config -e [--global]
# 设置提交代码时的用户信息
$ git config [--global] user.name "[name]"
$ git config [--global] user.email "[email address]"
```

5. 增加/删除文件
```
# 添加指定文件到暂存区
$ git add [file1][file2]...
# 添加指定目录到暂存区，包括子目录
$ git add [dir]
# 添加当前目录的所有文件到暂存区
$ git add .
# 删除工作区文件，并且将这次删除放入暂存区
$ git rm [file1][file2]...
# 停止追踪指定文件，但该文件会保留在工作区
$ git rm --cached [file]
# 改名文件，并且这个改名放入暂存区   ------此点为补充
$ git mv [file-original][file-renamed]
```

6. 代码提交
```
# 提交更新
$ git commit -m [message]
# 提交指定文件
$ git commit [file1][file2] -m [message]
# 跳过使用暂存区域，把所有已经跟踪过的文件暂存起来一并提交
$ git commit -a
# 修改最后一次提交
$ git commit --amend
# 提交时显示所有diff信息
$ git commit -v
```

7. 分支
```
# 列出所有本地分支
$ git branch
# 列出所有远程分支
$ git branch -r
# 列出所有本地分支和远程分支
$ git branch -a
# 新建test分支
$ git branch test
# 合并指定分支到当前分支
$ git merge [branch]
```

8. 查看信息
```
# 显示变更的文件状态
$ git status
#查看最近的提交日志
$ git log
# 显示commit历史以及每次commit发生变更的文件
$ git log --stat
# 显示暂存区和工作区的差异
$ git diff 
# 显示暂存区和上一个commit的差异
$ git diff --cached [file]
# 显示工作区与当前分支最新commit之间的差异
$ git diff HEAD
```

9. 远程同步
```
# 下载远程仓库的所有变动
$ git fetch [remote]
# 显示所有远程仓库
$ git remote -v
# 取回远程仓库的变化，并与本地分支合并
$ git pull [remote][branch]
# 上传本地指定分支到远程仓库
$ git push [remote][branch]
# 强行推送当前分支到远程仓库，即使有冲突
$ git push [remote] --force
# 推送所有分支到远程仓库
$ git push [remote] --all
```

10. 撤销
```
# 恢复暂存区的指定文件到工作区
$ git checkout [file]
# 恢复暂存区的所有文件到工作区
$ git checkout .
# 重置暂存区的指定文件，与上一次commit保持一致，但工作区不变
$ git reset [file]
```

11. 其他
```
# 获取命令的帮助信息
$ git help *
```