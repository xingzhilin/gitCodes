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

	-- 查看历史状态

  		$ git log

		修改时通过git status查看当前状态

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

	