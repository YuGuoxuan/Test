# Git学习

## 1.基础设置
- 设置用户名:   
`git config --global user.name 'YuGuoxuan'`
- 设置邮箱:   
`git config --global user.email '11706862@qq.com'`
## 2.初始化
- 建立目录
- 进入目录
- git init 进行初始化 
## 3.向仓库添加文件
- 创建文件
- 添加到暂存区:   
`git add filename`
- 提交到仓库:   
`git commit -m '提交描述'`
## 4.修改仓库文件
- 修改文件内容
- 添加到暂存区:   
`git add filename`
- 提交到仓库:   
`git commit -m '提交描述'`
## 5.删除文件
- 删除文件
- 从Git中删除文件:  
`git rm filename`
- 提交删除操作:  
`git commit -m '提交描述'`
## 6.提交到远程仓库
- 克隆远程仓库  
`git clone 仓库地址`
- 添加到暂存区  
`git add filename`
- 提交到本地仓库  
`git commit -m '提交描述'`
- 推送到远程仓库  
`git push`