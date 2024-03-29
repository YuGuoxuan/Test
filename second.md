# Git 基本操作
- 状态查看: `git status`
- 添加到暂存区: `git add [filename]`
- 提交到本地仓库: `git commit -m '提交描述'`
# 版本操作
- 查看版本记录:   
`git log`  
`git log --pretty=oneline`  
`git log --oneline`
`git reflog`

- 版本前进后退
  * 后退:   
  `git reset --hard 索引值`  切换到某个版本  
  `git reset --hard HEAD~n` 表示后退n步  
  `git reset --hard HEAD^n` 一个^表示后退一步,n个表示后退n步
- reset命令的三个参数  
  * --soft参数  
  仅仅在本地移动指针
  * --mixed参数  
  在本地库移动指针,也会重置暂存区
  * --hard参数  
  在本地库移动指针,重置暂存区和工作区
- 删除文件找回
  * 前提:删除前,文件存在时的状态提交到了本地库  
    操作:git reset --hard [指针位置]  
    删除操作已经提交到本地库:指针位置指向历史记录  
    删除操作尚未提交到本地库:指针位置使用HEAD
- 文件比较  
`git diff [filename]` 表示和暂存区进行比较  
`git diff head^ [filename]` 和上个版本进行比较  
`git diff [版本号]` 和某个版本进行比较  

- 分支操作
  * 查看分支 `git branch -v`
  * 创新新分支 `git branch [分支名称]`
  * 切换分支 `git checkout [分支名称]`
  * 合并分支
    * 切换到接受修改的分支上
    * 执行merge操作进行合并  
    git merge [分支名称]
    * 解决合并分支时产生的冲突  
    第一步:编辑文件,删除特殊符号  
    第二步:把文件修改到满意的程序,保存退出  
    第三步:git add [文件名]  
    第四步:git commit -m "日志信息"  
      * 注:此时提交不能带文件名

- 克隆远程仓库  
`git clone 仓库地址`
- 添加到暂存区  
`git add filename`
- 提交到本地仓库  
`git commit -m '提交描述'`
- 推送到远程仓库  
`git push`
- 从远程仓库拉取  
  * pull = fetch + merge
  * `git fetch [远程地址库别名][远程分支名]`
  * `git merge [远程地址库别名/远程分支名]`
  * `git pull [远程库地址别名][远程分支名]`
