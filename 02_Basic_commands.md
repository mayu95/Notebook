# 02 Vim Comfiguration and Basic Commands

Vim comfiguration and some basic commands in shell and vim

## Vim configuration
Install plug manager

``` shell
curl -fLo ~/.vim/autoload/plug.vim --create-dirs\https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
```

Execute PlugInstall in vim (open any file is ok)

```
PlugInstall
```

Usually we need to re-install vim with lua support. for mac os:
```
brew reinstall vim --with-lua --with-override-system-vi
```



## Shell commands

### file
* copy directories, including all the files they contain

	```
	cp -R source_dir destination_dir
	```
	
## Vim commands

### jump
* jump to a specific line:	``` line_Number + gg ```

* jump back:	``` '' ```

* turn to visual model: ``` v ```, then use ``` c ``` or ``` f ``` or other commands.

	> ``` S + obj(right) ```

* delete the visual part: ``` d ```


### search
* find the next character in a line:	``` f + char ```, find back:	``` F + char ```. use ``` ; ``` to repeat

* find 2 characters in a line/article:		``` s + 2 chars ```, find back:	``` S + 2 chars ```. use ``` ; ``` to repeat

* search any thing: 	``` / + anything ```, use ``` n ``` to next and ``` N ``` to previous. clear highlight: ``` noh ``` or random search

* search a variable/word:		``` cursor + * ```

* jump to the head of next word: ``` w ```, end of next word: ``` e ```
> trick: jump to the first non-space: ``` w ```

* word-level jump back: ``` b ```






### edit/change
* new line:		``` o ```

* cancel operation: ``` u ```, redo: ``` ctrl + r ```

* edit pairs: (left object will add space)

	```
	c + i + obj (e.g., w, ), ] etc.)		% 'i' means 'internal'
	
	c + a + obj ('a' means 'all', including objecy)
	```

* change object pair symbol: (left object will add space)

	```
	c + s + origin_obj(right) + new_obj(right)
	```

* cancel writing command: ``` esc ```

* edit to character:
	```
	c + f + char
	```


### abbreviation
* choose the alternative option: ``` tab ``` , no need to 'return'

* open the option abbreviation: first use ``` tab ``` to choose, then ``` , + e ``` to extend

* 









