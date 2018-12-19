# 01 Shell Environment Configuration

This section includes shell configuring and several basic commands of vim/shell.

Acknowlege：yukun


## Basic concept
**vim:** ~/.vimrc: configure of vim; ~/.vim: data, plugins

**zsh:** ~/.zshrc: configure of zsh; ~/.oh_my_zsh: data, plugins

## Configure shell
This tutor is for mac/linux.

### Install
download the config file from github
 
``` git
git clone https://github.com/mayu95/env_config.git
```

install oh-my-zsh (also need on linux)
> **wget** is used to download files from website given a url. If wget is not existed, "brew install wget".

```shell
sh -c "$(wget https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O -)"
```

run the config file (if there is update, ``` git pull ``` first)

``` shell
sh set_env.sh
```

if on linux, add below codes in 
```
~/.bash_profile
```

```
zsh -l
```

restart shell
> load config for iTerm2:
> 
> * **com.googlecode.iterm2.plist:** config of item2, e.g., cursor shape
> * **NeoDark.itemcolors:** color theme: preference -> profile -> color -> color presets -> import -> select NeoDark
> * **text setting:** text -> text rendering
> * **transparency:** profiles -> window -> transparency


### Note
If **gdircolors** can not be installed, you should "brew install coreutils" on your mac. (This problem will not show on linux.)


## Basic Commands
### shell
* delete words before the cursor

	```
	"crl" + "u"
	```
	
* complete parameters

	```
	 press "tab"
	```
	
* complete the command based on your frequency

	```
	"crl" + "f"
	```
	
*  jump to a directory

	```
	"z" + keyword: jump to some used directory containing the keyword 
	1: return to the previous directory
	cd: return to home
	```

* list files in a fashion way

	```
	l
	```

* the size of file

	```
	du -hs file_name
	```
	
* execute script those can be read or have head informaion

	```
	command + file
	```
	> e.g., "python tmp.py", "sh tmp.sh"
	>
	> or "./tmp.py", "./tmp.sh"
	
* calendar

	```
	cal
	```
	
### vim

* creat a new file
	> linux: everything is file

	```
	touch file_name
	```
	
* search

	```
	"/": search 
	"n": next matched result
	"N": previous mathed result
	```






