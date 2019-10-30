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
    
