# Python3

This is a notebook for learning Python3.

## File

* read a file and use it 

	``` python
	with open('file_name') as f:
		... ...
	```
	
* read some files in the same directory

	``` python
	import os
	
	your_directory = "dir_test"
	file_names = os.listdir(your_directory)
	for file_name in file_names:
		file_path = your_directory + "/" + file_name

	with open(file_path) as f:
		...
	```