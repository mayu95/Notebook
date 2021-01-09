# C++

This is a notebook for learning C++.


## Common Types

#### Array `A[]` 

* Define an Array:

	``` c++
	#include<vector>
	vector<int> A = {};
	```

* Define an array parameter of a function:

	```c++
	#include<vector>
	void InsertSort(vector<int>& A){
	}
	```

* The length:

	``` c++
	int length = sizeof (A) / sizeof (A[0]);
	```
