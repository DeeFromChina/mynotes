# Git 的使用
---
### 下载Git客户端

- 命令行客户端 [http://git-scm.com/download/](http://git-scm.com/download/)
- 图形界面客户端
	* SourceTree（Mac或Windows）[https://www.sourcetreeapp.com/](https://www.sourcetreeapp.com/)
	* Git Extensions（Windows）[https://sourceforge.net/projects/gitextensions/](https://sourceforge.net/projects/gitextensions/)
	
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

### 合并本地分支

- 待添加

### 创建远端GitHub库

- 登录[GitHub](https://github.com)，创建远端托管库，复制远端托管库url地址
- 进入命令行终端，定位到本地Git托管库所在目录
- 运行命令 **git remote add origin <远端托管库url>** 添加名称为origin的远端托管库。

### 同步远端GitHub库

- 待添加
