# C++

This is a notebook for learning C++.


## Basic Conceptions

#### Vector `A[]` 

* Define an Array using Vector:

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

* The length of a vector is `A.size()`, or we can use:

	``` c++
	int length = sizeof (A) / sizeof (A[0]);
	```
* Size_type: **do not** use `int`s in expressions that use `size()`.

	```c++
	vector<int> vec(10);
	
	for(vector<int>::size_type ix=0; ix != vec.size(); ++ix)
		vec[ix] = 6;
	```
	Here，we can ask the compiler to provide the appropriate type by using `auto` or `decltype`:
	
	```c++
	for (decltype(v.size()) ix=0; ix != v.size(); ++ix)
		vec[ix] =6;
	``` 
	
	1. Note that, in C++, we **always use** `!=` in 'for' loop, instead of `<`.  
	2. Hint that, `++x` is **not equal** to`x++`. 如果使用前缀形式，则会在表达式计算之前完成自增或自减，如果使用后缀形式，则会在表达式计算之后完成自增或自减。
	
	```c++
	int a = 21;
   int c ;
 
   // a 的值在赋值之前不会自增
   c = a++;   
   cout << "Line 1 - Value of a++ is :" << c << endl ;  
   // c = a++ = 21
 
   // 表达式计算之后，a 的值增加 1
   cout << "Line 2 - Value of a is :" << a << endl ;
   // a = 22
 
   // a 的值在赋值之前自增
   c = ++a;  
   cout << "Line 3 - Value of ++a is  :" << c << endl ;
   // a = 23
	```

* use `make_tuple` while more than one return.
	
	
## Coding Style
### Format
* 不在万不得已, 不要使用空行。  
	尤其是: 两个函数定义之间的空行**不要超过 2 行**, 函数体首尾不要留空行, **函数体中也不要随意添加空行**。
* `if`/`for`/`while` 等，`()`前后有空格。