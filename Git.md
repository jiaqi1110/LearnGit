# 命令
## Git 创建仓库

创建git仓库方式：
- `git init` 初始化一个git仓库
- `git clone`克隆一个git仓库 
## Git基本指令

git常用的命令：
- `git config`配置信息
- `git add`添加文件到缓存
- `git status` 查看文件的状态
- `git diff` 查看更新的详细信息
- `git commit` 提交命令
- `git rm` 删除
- `git mv` 移动或重命名

## Git分支管理

git分支常用命令：
- `git branch` 查看分支
- `git branch(branchname)` 创建分支
- `git checkout -b (branchname)` 创建分支且切换分支
- `git merge` 合并分支
- `git branch -d (branchname)` 删除分支

## Git查看提交历史

- `git log` 查看提交日志
	- `--oneline` 查看日志的简洁版本
	- `--graph` 查看日志中什么时候出现了分支、合并
	- `--reverse` 逆向显示所有日志
	- `--author` 查找指定用户的提交日志
	- `--since --before --until --after` 指定筛选日期
	- `--no--merges` 选项以隐藏并提交

## Git标签

- `git tag -a vx.x` 创建一个标签
- `git tag` 查看标签

## Git远程仓库

远程仓库常用指令：
- `git remote add` 添加远程仓库
- `git remote` 查看当前的远程仓库
- `git fetch` 或`git pull` 都可提取远程仓库
	- `git fetch` 从远程获取最新版本到本地，<span style="background:#b1ffff">不会自动合并</span>。
	- `git pull` 从远程获取最新版本到<span style="background:#b1ffff">合并</span>到本地。
- `git push` 推送到远程仓库
- `git remote rm` 删除远程仓库
## 存在问题
### git问题error: remote origin already exists.
- 先输入`git remote rm origin` 删除关联的origin的远程库
- 然后再继续关联自己的仓库 `git remote add origin https://github.com/xxxx.git`
- 最后`git push origin main` 

### 出现HTTP/2 stream 1 was not closed clreanly before end of the underlying stream
- `git config --global http.version HTTP/1.1` 
## 使用git在github更新文件
- 查看当前git仓库状态`git status` 
- 更新全部`git add *` 
- `git commit -m "更新说明"` 
- `git pull` 拉取当前分支最新代码
- `git push origin main` push到远程main分支上
