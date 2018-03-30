# 配置git用户和邮箱 
	$ git config --global user.name "你的github用户名"    
	$ git config --global user.email "你的github邮箱"
	* 不配置用户名和邮箱的话无法提交,因为git不知道你是谁

#查看配置
	$ git config --global user.name 
	$ git config --global user.email

#查看所有配置
	$ git config --list

#工作流
	- 工作区  ------- add ----->  暂存区   ------- commit ----->  历史区  ----- 

	-- 工作区

		通过git add 添加到暂存区
 		 $ git add '文件名'

	-- 暂存区
		特点:过渡的作用，避免误操作，保护工作区和历史区，分支处理;
		通过git commit 添加到历史区
  		$ git commit -m"注释内容"

	-- 历史区

#查看历史状态
	$ git log

	git log --pretty=oneline

	-- 你看到的一大串类似3628164...882e1e0的是commit id（版本号）

# 仓库当前的状态 
	-- $ git status

# 查看(difference) 具体修改了什么内容
	-- git diff

# 然后没什么问题了再提交   ===>  add -- status -- commit   -- status 

# 丢弃工作区的修改

	git checkout -- [fileName]

# 删除文件
	- 一是确实要从版本库中删除该文件，那就用命令git rm删掉，并且git commit：
		--  $ git rm test.txt
			rm 'test.txt'
			$ git commit -m "remove test.txt

	- 另一种情况是删错了，因为版本库里还有呢，所以可以很轻松地把误删的文件恢复到最新版本：
		--  $ git checkout -- test.txt

	***  命令git rm用于删除一个文件。如果一个文件已经被提交到版本库，那么你永远不用担心误删，但是要小心，你只能恢复文件到最新版本，你会丢失最近一次提交后你修改的内容。

#同步远程仓库
	- gitHub
		注册账号
		新建项目

	- 添加远程仓库
		$ git remote add origin "地址"

	-添加忽略文件
		$ touch .gitignore
		$ echo .DS_Store
		$ echo node_modules
		$ echo .idea

	- 推送代码
		$ git push origin master
	- 查看
		$ git remote 查看名字
		$ git remote -v 查看地址

#分支
	- 查看分支
		$ git branch 
	- 创建分支
		$ git branch [name]

	git checkout a
	git checkout -b c切换分支
	在master  git merge
	git checkout b
	git branch --merged 合并了哪些分支
	git branch --no-merged 合并了哪些分支
	git branch -d a 删除分支
	git branch -D a 删除分支


	查看分支：git branch

	创建分支：git branch <name>

	切换分支：git checkout <name>

	创建+切换分支：git checkout -b <name>

	合并某分支到当前分支：git merge <name>

	删除分支：git branch -d <name>