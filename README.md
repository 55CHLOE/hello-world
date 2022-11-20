# hello-world
My first repositort
#define _CRT_SECURE_NO_WARNINGS 1

#include<stdio.h>
//科学计数法
//9.0
//1001.0
//(-1)^0 * 1.001 * 2^3
//(-1)^s *  M    * 2^E
//s - 0
//M - 1.001
//E - 3
//
//0.5
//0.1
//(-1)^0 * 1.0 * 2^-1
//实际情况中E可以为负数
//s - 0
//M - 1.0
//E - -1
//E+127 = 126
//int main()
//{
//	int n = 9;
//	//0 00000000 00000000000000000001001 - 补码
//	//
//	float* pFloat = (float*)&n;
//	printf("n的值为:%d\n", n);//整形的形式放进去，整形的形式拿出来//9
//	printf("*pFloat的值为:%f\n", *pFloat);//整形的形式放进去，浮点数的形式拿出来//0.0000000
//	//(-1)^0 * 0.00000000000000000001001 * 2^-126
//	//是否可以说明整形和浮点型存储和拿出来的方式是不一样的？
//
//	*pFloat = 9.0;
//	//1001.0
//	//1.001 * 2^3
//	//(-1)^0 * 1.001 * 2^3
//	//0 10000010 00100000000000000000000 - 正数--->原反补码相同--->可视为补码
//	
//	printf("num的值为:%d\n", n);//浮点数的形式放进去，整形的形式拿出来//1091567616
//	printf("*pFlaot的值为:%f\n", *pFloat);//浮点数的形式放进去，浮点数的形式拿出来//9.0
//	return 0;
//}

//int  main()
//{
//	float f = 5.5;
//		//5.5
//		//101.1
//		//(-1)^0 * 1.011 * 2^2
//		//s - 0
//		//M - 1.011
//		//E - 2
//		//0 2+127 011
//		//0 10000001 01100000000000000000000
//		//因为内存中显示的是十六进制的数，故需要先将二进制转换为十六进制
//		//0x40b00000
//		//
//		return 0;
//}
//void test(int arr[])
//{
//	int sz = sizeof(arr) / sizeof(arr[0]);
//	printf("%d\n", sz);//64平台打印出来为2
//}
//int main()
//{
//	int arr[10] = { 0 };
//	test(arr);
//	return 0;
//}

//int main()
//{
//	char ch = 'w';//字符变量ch
//	char* pc = &ch;//字符指针变量pc
//	*pc = 'w'//解引用字符指针变量pc，得到'w'
//	return 0;
//}

//int main()
//{
//	char arr[] = "abcdef";//把字符串放到数组arr当中//数组名arr是首元素地址
//	char* pc = arr;//字符指针存放数组名，数组名是首元素a地址
//	printf("%s\n", arr);
//	printf("%s\n", pc);
//	return 0;
//}

//int main()
//{
//	const char* p = "abcdef";//写法正确，"abcdef"是一个常量字符串，p中存放的是首元素a的地址
//	//*p = 'w';//程序崩溃
//	//printf("%c\n", *p);//a
//	printf("%s\n", p);//abcdef
//	return 0;
//}

//int main()
//{
//	char arr1[] = "abcdef";
//	char arr2[] = "abcdef";//arr1与arr2首元素地址不同，故打印haha
//	const char* p1 = "abcdef";//是常量字符串，不可修改，只能被使用，故只需开辟一处空间即可
//	const char* p2 = "abcdef";//p1和p2指向的是同一块儿空间的起始位置，故打印hehe
//	if (p1 == p2)
//	{
//		printf("hehe\n");
//	}
//	else
//	{
//		printf("haha\n");
//	}
//	return 0;
//}

//指针数组 是数组，用来存放指针的
//int main()
//{
//	int arr[10] = { 0 };//整形数组
//	char ch[5] = { 0 };//字符数组
//	int* parr[4];//存放整形指针的数组 - 指针数组
//	char* pch[5];//存放字符指针的数组 - 指针数组
//	return 0;
//}

//int main()
//{
//	int a = 10;
//	int b = 20;
//	int c = 30;
//	int d = 40;
//	int* arr[4] = { &a,&b,&c,&d };
//	int i = 0;
//	for (i = 0; i < 4; i++)
//	{
//		printf("%d ", *(arr[i]));
//	}
//	return 0;
//}

//int main()
//{
//	int arr1[] = { 1,2,3,4,5 };
//	int arr2[] = { 2,3,4,5,6 };
//	int arr3[] = { 3,4,5,6,7 };
//
//	int* parr[] = { arr1,arr2,arr3 };
//	int i = 0;
//	for (i = 0; i < 3; i++)
//	{
//		int j = 0;
//		for (j = 0; j < 5; j++)
//		{
//			printf("%d ", * (parr[i] + j));
//		}
//		printf("\n");
//	}
//	return 0;
//}
//数组指针 是指针
//int main()
//{
//	int* p = NULL;//p是整形指针 - 指向整形的指针 - 可以存放整形的地址
//	char* pc = NULL;//pc是字符指针 - 指向字符的指针 - 可以存放字符的地址
//	                //数组指针 - 指向数组的指针 - 可以存放数组的地址
//	/*int arr[10] = { 0 };*/
//	//arr - 首元素地址
//	//&arr[0] - 首元素地址
//	//&arr - 数组的地址
//
//	int arr[10] = { 1,2,3,4,5,6,7,8,9,10 };
//	//int* pc[10] = &arr;//
//	//上面的pc是存放指针的数组
//
//	int (*p)[10] = &arr;//数组的地址要存起来
//	//上面的p是指向10个整形元素的数组指针
//	return 0;
//}

//int main()
//{
//	char* arr[5];//arr是指针数组
//	char*(*pa)[5] = &arr;//pa是数组指针，指向的数组5个元素类型是char*
//
//	int arr2[10] = { 0 };
//	int(*pa2)[10] = &arr2;
//	return 0;
//}

//int main()
//{
//	int arr[10] = { 1,2,3,4,5,6,7,8,9,10 };
//	int* p = arr;
//	int i = 0;
//	for (i = 0; i < 10; i++)
//	{
//		printf("%d ", *(p + i));
//	}
//	return 0;
//}

//数组指针要用到二维数组以上才比较方便
//参数是数组的形式
//void print1(int arr[3][5], int x, int y)
//{
//	int i = 0;
//	int j = 0;//利用c,y遍历数组的每个元素
//	for (i = 0; i < x; i++)
//	{
//		for (j = 0; j < y; j++)
//		{
//			printf("%d ", arr[i][j]);
//		}
//		printf("\n");
//	}
//}
////参数是数组指针的形式
//void print2(int(*p)[5], int x, int y)
//{
//	int i = 0;
//	for (i = 0; i < x; i++)
//	{
//		int j = 0;
//		for (j = 0; j < y; j++)
//		{
//			printf("%d ", p[i][j]);
//			printf("%d ", *(p[i] + j));
//			printf("%d ", * (*(p + i) + j));//找到i行j列的元素
//			printf("%d ", (*(p + i))[j]);
//		}
//		printf("\n");
//	}
//}
//int main()
//{
//	int arr[3][5] = { {1,2,3,4,5},{2,3,4,5,6},{3,4,5,6,7} };//把这个二维数组打印一下，即分装print函数
//	print1(arr, 3, 5);//不仅要传数组名，还要传几行几列
//	print2(arr, 3, 5);
//	return 0;
//}

//int main()
//{
//	int arr[10] = { 1,2,3,4,5,6,7,8,9,10 };
//	int i = 0;
//	int* p = arr;
//	for (i = 0; i < 10; i++)
//	{
//		printf("%d ", p[i]);
//		printf("%d ", *(p + i));
//		printf("%d ", *(arr + i));
//		printf("%d ", arr[i]);//arr[i] == *(arr+i) == *(p+i) == p[i]
//	}
//	return 0;
//}
//int main()
//{
//	char ch = 'w';//字符变量ch中放了一个字符w
//	char* p = &ch;//字符指针p
//	const char* p2 = "abcdef";//当你把一个字符串赋值给字符指针p2时，其实是把字符串中首字符a的地址赋值给字符指针p2
//	//p2指向这个字符串，p2存放的是a的地址
//	//这个字符串是常量字符串，不允许被修改，故最合理的书写方式是在char*前加上const
//	return 0;
//}

//int main()
//{
//	//指针数组 - 数组 - 存放指针的数组
//	int* arr[10];
//	char* ch[5];
//
//	//数组指针 - 指向数组的指针
//	//int* p3;//整形指针 - 指向整形的指针
//	//char* p4;//字符指针 - 指向字符的指针
//	int arr2[5];
//	int (* pa)[5] = &arr2;//取出数组的地址,pa就是一个数组指针
//	//数组指针类型：去掉名字pa即int(*)[5]:是一个指针，指向有5个元素的数组
//	return 0;
//}
//void test(int arr[3][5])                //√
//{}
//void test1(int arr[][5])//把行给省去      √  
//{}
//void test2(int arr[3][])//把列给省去      ×
//{}
//void test3(int arr[][])//把行、列全省去   ×
//{}
//void test4(int* arr)//                    ×
//{}
//void test4(int** arr)//                   ×
//{}
//void test5(int(* arr)[5])               //√
//{}
//
//int main()
//{
//	int arr[3][5];
//
//	test(arr);//二维数组传参
//
//	return 0;
//}

//void test1(int* p)
//{}
//void test2(char*p)
//{}
//int main()
//{
//	int a = 10;
//	int* p1 = &a;
//	test1(&a);//ok  可以存放变量的地址
//	test1(p1);//ok  可以存放一级指针的变量
//
//	char ch = 'w';
//	char* pc = &ch;
//	test2(&ch);//ok
//	test2(pc);//ok
//	return 0;
//}
//void test(int** p)
//{}
//int main()
//{
//	int* ptr;
//	int** pp = &ptr;
//	test(&ptr);//一级指针的地址   ok
//	test(pp);//二级指针变量本身   ok
//
//	int* arr[10];
//	test(arr);//指针数组也可以    ok
//	return 0;
//}
//
//数组指针 - 是指向数组的指针
//函数指针 - 是指向函数的指针 - 存放函数地址的一个指针
//int Add(int x, int y)
//{
//	int z = 0;
//	z = x + y;
//	return z;
//}
//int main()
//{
//	int a = 10;
//	int b = 20;
//	//int arr[10] = { 0 };
//	//int(*p)[10] = &arr;
//	//&arr
//	//arr
//	//printf("%d\n",Add(a, b));
//	
//	//&函数名 和 函数名 都是函数的地址
//	/*printf("%p\n", &Add);
//	printf("%p\n", Add);*/
//
//	int (* pa)(int,int) = Add;//存储函数地址
//	printf("%d\n",(*pa)(2, 3));//调用函数要传参
//	return 0;
//}

//不同函数指针的定义方式，不同函数的地址的存储，定义的函数指针也不相同
//void Print(char* str)
//{
//	printf("%s\n", str); 
//}
//int main()
//{
//	int(*p)[10] = &arr;
//	void (*p)(char*) = Print;
//	(* p)("hello bit");
//	return 0;
//}
//signal是一个函数声明
//signal函数的参数有2个，第一个是int类型，第二个是函数指针，改函数指针指向的函数的参数是int,返回类型是void
//signal函数的返回类型也是一个函数指针：该函数指针指向的函数的参数是int，返回类型是void
////
//void(*         signal(int, void(*)(int))    )(int);
//
////typedef - 关键字 - 可以让某些类型变得简单一些
//
//typedef void(* pfun_t)(int);//而对于函数指针来说，把void(*)(int)类型重新起个名字叫pfun_t
//pfun_t signal(int, pfun_t);
////以上两句合起来就是第一行的意思
//
//typedef unsigned int uint;//把unsigned int 类型重新起个名字叫 unit

//int Add(int x, int y)
//{
//	int z = 0;
//	z = x + y;
//	return z;
//}
//int main()
//{
//	int a = 10;
//	int b = 20;
//
//	int (*pa)(int, int) = Add;//存储函数地址
//	printf("%d\n", pa(2, 3));//pa存放了Add的地址，与下方Add用法理解起来是一致的              //5
//	printf("%d\n", Add(2, 3));//调用函数的时候，函数名是个地址                               //5
//
//	printf("%d\n", (*pa)(2, 3));//pa是个函数指针，对其进行解引用*找到函数本身，然后传参调用  //5
//
//	printf("%d\n", *pa(2, 3));//此处()优先级高于*，故先结合pa(2,3),为5，然后再*5，出现问题   //程序出现问题
//	return 0;
//}
//int Add(int x, int y)
//{
//	return x + y;
//}
//int Sub(int x, int y)
//{
//	return x - y;
//}
//int Mul(int x, int y)
//{
//	return x * y;
//}
//int Div(int x, int y)
//{
//	return x / y;
//}
//int main()
//{
//	//指针数组
//	int* arr[5];
//	//需要一个数组，这个数组可以存放4个函数的地址 - 函数指针数组
//	int (* pa)(int,int) = Add;//Sub/Mul//Div
//	int (*parr[4])(int, int) = {Add,Sub,Mul,Div};//函数指针的数组
//	int i = 0;
//	for (i = 0; i < 4; i++)
//	{
//		printf("%d\n",parr[i](2, 3));//5,-1,6,0
//	}
//	return 0;
//}
