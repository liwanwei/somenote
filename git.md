#git笔记


- `git config --global user.name "Your Name"` 
- `git config --global user.email "email@example.com"`

- `mkdir learngit` 在工作区上新建learngit的文件夹
- `cd learngit` 
	更换到learngit文件夹中
- `pwd` 用于显示当前目录

- `git init` 把这个目录变成Git可以管理的仓库：

- `git add`
- `git commit -m "修改信息"`
- `git comint` 进入vim界面后使用i进入文本编辑状态，使用shift+：进入命令行编辑状态，输入命令x！强制退出
- `git status` 查看工作区状态
- `git diff` 查看修改内容

- `git reset --hard commit_id` 退回到commit_id的代表的版本
- `git log` 查看提交历史，以便确定要回退到哪个版本
- `git reflog` 查看命令历史，以便确定要回到未来的哪个版本，拿到commit_id
###撤销修改
- `git checkout -- file` 
	- 场景1：当你改乱了工作区某个文件的内容，想直接丢弃工作区的修改时，用命令git checkout -- file。
- `git reset HEAD file` 
	- 场景2：当你不但改乱了工作区某个文件的内容，还添加到了暂存区时，想丢弃修改，分两步，第一步用命令git reset HEAD file，就回到了场景1，第二步按场景1操作。
	- 场景3：已经提交了不合适的修改到版本库时，想要撤销本次提交，参考版本回退一节，不过前提是没有推送到远程库。
###删除文件
- `git rm filename` #git rm用于删除一个文件。工作空间删除一个文件后，若工作该文件已经被提交到版本库，使用 git rm 命令删除，也可以使用git checkout --file 从暂存区中恢复。那么你永远不用担心误删，但是要小心，你只能恢复文件到最新版本，你会丢失最近一次提交后你修改的内容。

- `git clone git@github.com:liannaiqishi/gitskills.git` #从github中clone一个本地库

####推送到远程仓库
`git push -u origin master`第一次初始化时，可加参数`-u`
`git push  origin master`

###查看分支
- 查看分支：`git branch`

- 创建分支：`git branch <name>`

- 切换分支：`git checkout <name>`

- 创建+切换分支：`git checkout -b <name>`

- 合并某分支到当前分支：`git merge <name>`

- 删除分支：`git branch -d <name>`

- 删除远程分支：`git push origin :gh-pages`注意冒号之前有空格，就是把一个空的branch赋值给已有的branch，这样就删除了
