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

//char* my_strcpy(char* dest,const char* scr)
////1.写一个函数指针pf,能够指向my_strcpy
//char* (* pf)(char*,const char*)
//
////2.写一个函数指针数组，能够存放4个my_strcpy函数的地址
//char* (* pfArr[4])(char*,const char*) 
//void menu()
//{
//	printf("*************************\n");
//	printf("****  1. add     2.sub***\n");
//	printf("****  3. mul     4.div***\n");
//	printf("****  5.xor      0. exit*\n");
//	printf("*************************\n");
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
//
//void Calc(int (*pf)(int,int))
//{
//	int x = 0;
//	int y = 0;
//	printf("请输入两个操作数:>");
//	scanf("%d%d", &x, &y);
//	printf("%d\n", pf(x, y));
//}
//int main()
//{
//	int input = 0;
//	
//	do
//	{
//		menu();
//		printf("请选择:>");
//		scanf("%d", &input);
//		switch (input)
//		{
//		case 1:
//			Calc(Add);
//			break;
//		case 2:
//			Calc(Sub);
//			break;
//		case 3:
//			Calc(Mul);
//			break;
//		case 4:
//			Calc(Div);
//			break;
//		case 0:
//			printf("退出\n");
//			break;
//		default:
//			printf("选择错误\n");
//			break;
//		}
//	} while (input);
//	return 0;
//}
//int main()
//{
//	int input = 0;
//	int x = 0;
//	int y = 0;
//    //pfArr 是一个函数指针数组 - 转移表
//	int (*pfArr[])(int, int) = { 0,Add,Sub,Mul,Div,Xor };
//	do
//	{
//		menu();
//		printf("请选择:>");
//		scanf("%d", &input);
//		if (input >= 1 && input <= 5)
//		{
//			printf("请输入两个操作数:>");
//			scanf("%d%d", &x, &y);
//			int ret = pfArr[input](x, y);
//			printf("%d\n", ret);
//		}
//		else if (input == 0)
//		{
//			printf("退出\n");
//		}
//		else
//		{
//			printf("输入错误\n");
//		}
//	} while (input);
//	return 0;
//}
//int main()
//{
//	int input = 0;
//	int x = 0;
//	int y = 0;
//	do
//	{
//		menu();
//		printf("请选择:>");
//		scanf("%d", &input);
//		printf("请输入两个操作数:>");
//		scanf("%d%d", &x,&y);
//		switch (input)
//		{
//		case 1:
//			printf("%d\n",Add(x, y));
//			break;
//		case 2:
//			printf("%d\n", Sub(x, y));
//			break;
//		case 3:
//			printf("%d\n", Mul(x, y));
//			break;
//		case 4:
//			printf("%d\n", Div(x, y));
//			break;
//		case 0:
//			printf("退出\n");
//			break;
//		default:
//			printf("选择错误\n");
//			break;
//		}
//	} while (input);
//	return 0;
//}
//int Add(int x, int y)
//{
//	return x + y;
//}
//int main()
//{
//	//1.指针数组
//	int* arr[10];
//	//2.数组指针
//	int* (* pa)[10] = &arr;
//
//	//3.函数指针
//	int (* pAdd)(int,int) = Add;//&Add
//	//int sum = (*pAdd)(1, 2);//调用函数
//	int sum = pAdd(1, 2);
//	printf("sum = %d\n", sum);
//
//	//4.函数指针的数组
//	int (*pArr[5])(int, int);
//	//5.指向函数指针数组的指针
//	int (*(* pArr)[5])(int, int);
//	return 0;
//}
void bubble_sort(int arr[], int sz)
{
	int i = 0;
	//趟数
	for (i = 0; i < sz - 1; i++)
	{
		//每一趟冒泡排序
		int j = 0;
		for (j = 0; j < sz - 1 - i; j++)
		{
			if (arr[j] > arr[j + 1])
			{
				int tmp = arr[j];
				arr[j] = arr[j + 1];
				arr[j + 1] = tmp;
			}
		}
	}
}
struct Stu
{
	char name[20];
	int age;
};

//void qsort(void* base,     //目标数组的起始位置
//	       size_t num,     //数组的大小，单位：元素 - 有几个元素
//	       size_t width,   //元素大小 - 一个元素有几个字节
//	       int (*cmp)(const void* e1, const void* e2) // 比较函数 - e1与e2是要比较的那两个元素的地址
//           );

//int cmp_int(const void* e1, const void* e2)
//{
//	//比较两个整形值的
//	return *(int*)e1 - *(int*)e2;
//}
//void test1()
//{
//	int arr[10] = { 9,8,7,6,5,4,3,2,1,0 };
//	int sz = sizeof(arr) / sizeof(arr[0]);
//	qsort(arr, sz, sizeof(arr[0]), cmp_int);
//	int i = 0;
//	for (i = 0; i < sz; i++)
//	{
//		printf("%d ", arr[i]);
//	}
//}

//int cmp_float(const void* e1, const void* e2)
//{
//	//if (*(float*)e1 == *(float*)e2)
//	//	return 0;
//	//else if (*(float*)e1 > *(float*)e2)
//	//	return 1;
//	//else
//	//	return -1;
//	return((int)(*(float*)e1 - *(float*)e2));
//}
//void test2()
//{
//	float f[] = { 9.0,8.0,7.0,6.0,5.0,4.0 };
//	int sz = sizeof(f) / sizeof(f[0]);
//	qsort(f, sz, sizeof(f[0]), cmp_float);
//	int j = 0;
//	for (j = 0; j < sz; j++)
//	{
//		printf("%f ", f[j]);
//	}
//}
#include<string.h>
int cmp_stu_by_name(const void* e1, const void* e2)
{
	//比较名字就是比较字符串
	//字符串比较不能直接用><=来比较，应该用strcmp函数 - 字符串比较函数
	return strcmp(((struct Stu*)e1)->name, ((struct Stu*)e2)->name);
}
cmp_stu_by_age(const void*e1,const void*e2)
{
	return ((struct Stu*)e1)->age - ((struct Stu*)e2)->age;//升序
}

void test3()
{
  	struct Stu s[3] = { {"zhangsan",20},{"lisi",30},{"wangwu",10} };
	int sz = sizeof(s) / sizeof(s[0]);

	qsort(s,sz,sizeof(s[0]),cmp_stu_by_age);

}
int main()
{
	test3();
	return 0;
}

// void tset4()
//{
//	int arr[10] = { 9,8,7,6,5,4,3,2,1,0 };
//	int sz = sizeof(arr) / sizeof(arr[0]);
//	//使用bubble_sort函数的程序员一定知道自己排序的是什么数据
//	//就应该知道如何比较待排序数组中的元素
//	//bubble_sort(arr, sz,sizeof(arr[0]),cmp_int);
//}
//void Swap(char* buf1, char* buf2,int width)
//{
//	int i = 0;
//	for (i = 0; i < width; i++)
//	{
//		char tmp = *buf1;
//		*buf1 = *buf2;
//		*buf2 = tmp;
//		buf1++;
//		buf2++;
//	}
//}
////实现冒泡排序函数的程序员，他是否知道未来排序的数据类型？ - 不知道
////那程序员也不知道待比较的两个元素的类型
//void bubble_sort(void* base, int sz, int width, int(*cmp)(void*e1,void*e2))
//{
//	int i = 0;
//	//趟数
//	for (i = 0; i < sz; i++)
//	{
//		//每一趟比较的对数
//		int j = 0;
//		for (j = 0; j < sz-1-i; j++)
//		{
//			//两个元素的比较
//			if (cmp((char*)base+j*width,(char*)base+(j+1)*width) > 0)//相邻两个元素的地址
//			{
//				//交换
//				Swap((char*)base + j * width, (char*)base + (j + 1) * width,width);
//			}
//		}
//	}
//}
//
//int cmp_stu_by_age(const void*e1,const void*e2)
//{
//	return ((struct Stu*)e1)->age - ((struct Stu*)e2)->age;//升序
//}
//
//int cmp_stu_by_name(const void* e1, const void* e2)
//{
//	//比较名字就是比较字符串
//	//字符串比较不能直接用><=来比较，应该用strcmp函数 - 字符串比较函数
//	return strcmp(((struct Stu*)e1)->name, ((struct Stu*)e2)->name);
//}
//
//void tset5()
//{
//	struct Stu s[3] = { {"zhangsan",20},{"lisi",30},{"wangwu",10} };
//	int sz = sizeof(s) / sizeof(s[0]);
//	//bubble_sort(s,sz,sizeof(s[0]),cmp_stu_by_age);
//	bubble_sort(s, sz,sizeof(s[0]),cmp_stu_by_name);
//}
//int main()
//{
//	test5();
//	return 0;
//}

//int main()
//{
//	int a[5] = { 1,2,3,4,5 };
//	int* ptr = (int*)(&a + 1);//这里的(&a+1)是数组，故类型是数组指针类型，不能存放到整形指针类型中去，故要强制类型转换成整形指针类型
//	printf("%d,%d\n", *(a + 1), *(ptr - 1));
//	return 0;
//}

#define _CRT_SECURE_NO_WARNINGS 1


#include<stdio.h>
#include<stdlib.h>
//F5开始调试 与F9(断点)搭配使用
//F5与F9 可以让我们快速的跳到问题所在的区域
//F5是跳到断点处，跳到的是执行逻辑上的下一个断点，而不是物理上的下一个断点
//int main()
//{
//	int i = 0;
//	for (i = 0; i < 100; i++)
//	{
//		printf("%d ", i);
//	}
//	for (i = 0; i < 100; i++)
//	{
//		printf("%d ",10 - i);
//	}
//	return 0;
//}

//void my_strcpy(char* dest,char* src)
//{
//	while (*src != '\0')
//	{
//		*dest = *src;
//		src++;
//		dest++;
//	}
//	*dest = *src;//'\0'
//}
//void my_strcpy(char* dest, char* src)
//{
//	if (dest != NULL && src != NULL)//很好的规避了问题，但不利于发现问题
//	{
//		while (*dest++ = *src++)//直接进行解引用容易形成野指针
//		{
//			;//直到拷贝'\0'，为假，循环停下来
//		}
//	}
//}
#include<assert.h>
//
//char* my_strcpy(char* dest,const char* src)//const修饰*scr,使得*scr不可被更改↓
//{
//	char* ret = dest;//先把dest地址保存在ret中
//	assert(dest != NULL);//断言
//	assert(src != NULL);//断言
//	//把src指向的字符串拷贝到dest指向的空间，包含'\0'字符
//	while (*dest++ = *src++)//↑
//	{
//			;
//	}
//	return ret;//返回目的地的起始地址
//}
//int main()
//{
//	//strcpy
//	//字符串拷贝
//	char arr1[] = "###";
//	char arr2[] = "bit";
//	;
//	printf("%s\n",my_strcpy(arr1,arr2) );
//	//一个函数的返回值作为另一个函数的参数 - 链式访问
//	return 0;
//}

//int main()
//{
//	const int num = 10;
//	int n = 100;
//
//	int* const p = &num;
//	//const可以放在*的左边和右边，且分别代表着不同的意思
//	//const放在指针变量的*左边时，修饰的是*p,也就是说：不能通过p来改变*p(num)的值
//	//const放在指针变量的*右边时，修饰的是指针变量p本身，p不能被改变
//	*p = 20;
//	p = &n;
//
//	printf("%d\n", num);
//
//	return 0;
//}
//int my_strlen(const char* str)
//{
//	int count = 0;
//	assert(str != NULL);//指针str,必然进行解引用操作，故先进行断言，保证指针的有效性
//	//使得代码更精壮
//	while (*str != '\0')//求长度就是在找里面的'\0'
//	{
//		count++;
//		str++;
//	}
//	return count;
//}
//int main()
//{
//	char arr[] = "abcdef";
//	int len = my_strlen(arr);
//	printf("%d\n", len);
//	return 0;
//}

//check_sys()
//{
//	int a = 1;
//	char* p = (char*)&a;
//	//返回1，小端
//	//返回0，大端
//	return *p;
//}

//check_sys()
//{
//	int a = 1;
//	return *(char*)&a;
//}
//int main()
//{
//	//写一段代码告诉我们当前机器的字节序是什么
//	//返回1，小端
//	//返回0，大端
//	int ret = check_sys();//函数更加独立，功能不会与其他内容交互
//	if (ret == 1)
//	{
//		printf("小端\n");
//	}
//	else
//	{
//		printf("大端\n");
//	}
//	return 0;
//}

////输出什么？
//#include<stdio.h>
//int main()
//{
//	char a = -1;
//	//1000000000000000000000000000001 - 原码
//	//1111111111111111111111111111110 - 反码
//	//1111111111111111111111111111111 - 补码
//	//11111111 - 输入
//	//输出时，从字符类型转变为整形，需要进行整形提升-根据符号位，高位补符号位到32位
//	//1111111111111111111111111111111 - 整形提升之后的结果 - 补码
//	//输出时，输出的是原码，倒回去算
//
//
//	signed char b = -1;
//	//11111111
//	unsigned char c = -1;
//	//11111111
//	//无符号char，高位不是符号位，如何整形提升？→高位补0
//	//00000000000000000000000011111111 - 整形提升后的结果 - 补码
//	//打印的时候一看高位是0，是正数，原反补码相同
//
//	printf("a=%d,b=&d,c=%d", a, b, c);
//	//a = -1，b = -1,c = 255
//	return 0;
//}
//#include<stdio.h>
//int  main()
//{
//	char a = -128;
//	//首先写成2进制序列
//	//10000000000000000000000010000000 - 原码
//	//11111111111111111111111101111111 - 反码
//	//11111111111111111111111110000000 - 补码
//	//10000000 - 1个字符，1个字节，8个比特位
//	//11111111111111111111111110000000 - 整形提升之后的结果 - 补码 也是原码↓
//
//	printf("%u\n", a);
//	//%d - 打印十进制的有符号数字
//	//&u - 打印十进制的无符号数字 - 我认为内存中放置的是无符号数 - 那么原反补码相同↑
//	return 0;
//}
//#include<windows.h>
//int main()
//{
//	unsigned int i;
//	for (i = 9; i >= 0; i--)
//	{
//		printf("%u\n", i);//死循环，因为i永远为正不可能为负
//		Sleep(100);
//	}
//	return 0;
//}

//int main()
//{
//	char a[1000];
//	int i;
//	for (i = 0; i < 1000; i++)
//	{
//		a[i] = -1 - i;
//	}
//	printf("%d\n", strlen(a));//128+127=255
//	return 0;
//}

//#include<stdio.h>
//
//unsigned char i = 0;//0-255
//int main()
//{
//	for (i = 0; i <= 255; i++)//这个条件恒成立
//	{
//		printf("hello world\n");//陷入死循环
//	}
//	return 0;
//}
