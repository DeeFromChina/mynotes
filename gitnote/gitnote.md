# Git 的使用
---
### Git是什么

- [Git详解之一：Git起步](http://blog.jobbole.com/25775/)
- [Git详解之二：Git基础](http://blog.jobbole.com/25808/)
- [Git详解之三：Git分支](http://blog.jobbole.com/25877/)
- [Git详解之四：服务器上的Git](http://blog.jobbole.com/25944/)
- [Git详解之五：分布式Git](http://blog.jobbole.com/25660/)
- [Git详解之六：Git工具](http://blog.jobbole.com/26112/)
- [Git详解之七：自定义Git](http://blog.jobbole.com/26131/)
- [Git详解之八：Git与其他系统](http://blog.jobbole.com/26198/)
- [Git详解之九：Git内部原理](http://blog.jobbole.com/26209/)

---
### 下载Git客户端

- 命令行客户端 
 	* [Git Downloads](http://git-scm.com/download/)
- 图形界面客户端
	* [SourceTree（Mac或Windows）](https://www.sourcetreeapp.com/)
	* [Git Extensions（Windows）](https://sourceforge.net/projects/gitextensions/)

---	
### 创建本地Git库

- 进入命令行终端，定位到将要使用Git托管的项目目录下。
- 运行命令 **git init** 创建本地托管库。
- 在目录下创建.gitinore文件，配置要忽略不提交Git托管的文件及目录。

### 创建本地分支

- 进入命令行终端，定位到本地库所在目录。
- 运行命令 **git status** 显示当前库状态（查看当前所在分支，初始都在master分支上）。
- 运行命令 **git checkout -b <分支名称>** 创建新分支，并检出新分支作为当前工作分支。
- 运行命令 **git status** 显示当前库状态（查看当前所在分支，已经显示在新的分支上）。
- 运行命令 **git branch** 查看本地Git库存在的所有分支。
- 运行命令 **git checkout <已存在分支名称>** 切换工作的分支。

### 提交文件

- 在本地Git托管的项目目录下对文件或者目录进行修改。
- 运行命令 **git status** 显示当前库状态（查看当前所在分支哪些文件及目录被修改）。
- 运行命令 **git add .** 将所有被修改文件及目录加入暂存区。（或者运行命令 **git add <文件绝对路径>** 将指定文件或目录加入暂存区）。
- 运行命令 **git status** 显示当前库状态（查看当前所在分支哪些文件及目录被加入暂存区）。
- 运行命令 **git commit -m”first commit”** 将暂存区文件及目录提交本地Git库（当前所在分支），并添加备注信息”first commit”。

### 文件撤出暂存区

- 进入命令行终端，定位到本地库所在目录。
- 运行命令 **git reset HEAD <文件名称>** 将指定文件撤出暂存区（既文件不提交）。

### 文件还原

- 进入命令行终端，定位到本地库所在目录。
- 运行命令**git checkout -- <文件名称>** 暂存区文件来覆盖工作区中的文件，撤销自上次**git add**后的修改。
- 运行命令**git checkout <分支名称> -- <文件名称>** 撤销当前文件修改，还原为指定分支上的对应文件。

### 合并本地分支

- 进入命令行终端，定位到本地库所在目录。
- 运行命令 **git branch** 查看本地Git库存在的所有分支及当前所在分支。
- 运行命令 **git checkout <被融入的分支名称>** 切换到要被融入的分支上。
- 运行命令 **git merge <要融合入当前分支的分支名称>** 将目标分支的变化更新到当前分支。

### 删除本地分支

- 进入命令行终端，定位到本地库所在目录。
- 运行命令 **git branch** 查看本地Git库存在的所有分支及当前所在分支。
- 运行命令 **git branch -d <分支名称>** 删除已完全融入master的分支（**git branch -D <分支名称>** 强制删除未master的分支。）。


### 创建远端GitHub库

- 登录[GitHub](https://github.com)，创建远端托管库，复制远端托管库url地址
- 进入命令行终端，定位到本地Git托管库所在目录
- 运行命令 **git remote add origin <远端托管库url>** 添加名称为origin的远端托管库。

### 同步远端GitHub库

- 进入命令行终端，定位到本地库所在目录。
- 运行命令 **git push <远端名称> <远端分支名称>** 将本地Git库当前分支的变化更新到远端对应分支，若分支不存在则在远端创建该分支。
- 运行命令 **git pull <远端名称> <远端分支名称>** 将远端GitHub库对应分支的变化更新到本地Git库当前分支。

---
### Git使用建议
1. 协同开发时永远不要直接在master上工作，所有工作都应该在分支上完成。
2. 协同开发时master上只从远端库拉取更新，然后再将master融入工作中的分支。
3. 向工作分支提交修改的时候应该备注有意义的信息描述这次提交内容。
4. 不建议在本地将工作分支融入master，应该将工作分支推送到远端库，在Github上用PullRequest完成分支融入master的操作。
5. 分支在Github上融入matser后，本地库切换到master拉取更新，然后再融入到本地各个分支上。
6. 已经融入master的分支需要在远端库，本地库分别删除。

---
### Git常用命令
参考 [易代言-科技主页](http://www.52edaiyan.com/homepage/tech/git)  




