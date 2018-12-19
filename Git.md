# Git/Github

* Connect to a github file and update
	* if it is a new file and have not been upload to a repository:
	
		``` git
		git remote		% see the tutorial while building
		--> git push
		```
	
	* if it is cloned from a repository:
		
		``` git 
		git push
		```
		
	> if there is a warning "Changes not staged for commit":
	
	``` git
	git commit			% find the deleted files
	--> git add			
	--> git commit -a 	
		% commit all
	
	