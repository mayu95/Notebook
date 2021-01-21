# GDB

This is a notebook for GDB.


## Install

#### gdb fails with “Unable to find Mach task port for process-id” error

* Reference  
	Stackoverflow: https://stackoverflow.com/questions/11504377/gdb-fails-with-unable-to-find-mach-task-port-for-process-id-error  
	Oschina(中文版): https://my.oschina.net/u/1466652/blog/823666

* Description  
	Darwin kernel出于安全考虑，在没有特殊授权的情况下不允许gdb调试任何程序，因为可以调试就掌握了进程的控制权。不过如果是root用户就没有这个问题，不过谁愿意用root来调试程序呢。
	
	解决办法：一个常用的解决方法就是给gdb授予系统完全信任的代码签名权利，以对其他进程。

* 解决方法  
	解决方式和英文版一样，且出现 can't store the certificate in the “System” keychain 问题。  
	但是在 “Finally you can sign gdb” 时，报错：
	
	```shell
	sudo codesign -s gdb-cert /usr/local/bin/ggdb
	/usr/local/bin/ggdb: No such file or directory
	```
	采用中文版解决方式：
	
	```shell
	codesign -s gdb-cert `which gdb`  // 将证书授予gdb
	sudo killall taskgated  	// 重启taskgated服务
	```
	
* 备注  
	英文版问题估计是地址写错了，应该是`sudo codesign -s gdb-cert /usr/local/bin/gdb`，而非`ggdb`。
	

#### During startup program terminated with signal ?, Unknown signal.

* Reference  
	Step 1: Stackoverflow: https://stackoverflow.com/questions/39702871/gdb-kind-of-doesnt-work-on-macos-sierra  
	Step 2: 简书(中文版): https://www.jianshu.com/p/14425059fa92
	
* Description  
	Mac OS High Sierra 版本原因。 
	 
* 解决方法  
	Step 1 无效，依旧报错 “During startup program terminated with signal SIGTRAP, Trace/breakpoint trap.”  
	后发现同时安装了`gdb 8.0.1`和`gdb 8.1`两个版本。根据 Step 2，卸载`gdb 8.1`，并重新授权证书，**重启taskgated服务**。
	
	```
	sudo codesign -s gdb-cert /usr/local/bin/gdb
	sudo killall taskgated 
	```
	