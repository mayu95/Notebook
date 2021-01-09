# Git
Git and Github

## Connect to a github file and update
* if it is a new file and have not been upload to a repository:
	
``` git
git branch -M main

% if build a new repository
git remote add origin https://...
% if already exist
git remote set-url origin https:

git push -u origin main
```
	
* if it is cloned from a repository:
		
``` git 
git push
```
		
> if there is a warning "Changes not staged for commit":

``` git
git commit		% find the deleted files
git add			
git commit -a 	% commit all
```

## 其他操作