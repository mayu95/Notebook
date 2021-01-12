# Git
Git and Github

## Connect to a github file and update
* if it is a new file and have not been upload to a repository:
	
	```
	git branch -M main
	
	// if build a new repository
	git remote add origin https:...
	// if already exist
	git remote set-url origin https:
	
	git push -u origin main
	```
	
* if it is cloned from a repository:
		
	``` 
	git push
	```
		
> if there is a warning "Changes not staged for commit":

```
git commit		// find the deleted files
git add			
git commit -a 	// commit all
```

## 实用技巧
### Cancle file tracking

	```
	git rm -r --cached   + filename　//不删除本地文件
	git rm -r --f   + filename　//删除本地文件
	```

### Searching
搜索框输入:
`in:description xx stars:>xx forks:>xx pushed:>xx-x-x`


	

## Github进行fork后如何与原仓库同步
#### Before merge
* 执行命令 `git remote -v` 查看远程仓库的路径，若只有`origin`，则需要：
	
	```
	git remote add upstream   + URL
	```
* 执行命令 `git status` 检查本地是否有未提交的修改。

#### Merge and upload
* 执行命令 `git fetch upstream` 抓取原仓库的更新。
* 执行命令 `git checkout master` 切换到 master 分支。
* 执行命令 `git merge upstream/master` 合并远程的master分支。
* 执行命令 `git push` 把本地仓库向github仓库。