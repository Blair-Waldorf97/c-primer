c++primer exercises

1.1

```c++
#include <iostream>

using namespace std;

int main()
{
    return 0;
}

```

1.2

0 error(s), 0 warning(s)

1.3

```c++
cout<<"Hello, World"<<endl;
```

1.4

```c++
cout<<2+3<<endl;
    cout<<2*3<<endl;
```

1.5

```c++
 cout<<2+3<<5*6<<endl;
```

1.6不合法，“；”表示这条语句已经结束，所以需要去掉那些逗号。

1.7

||=== Build: Debug in test (compiler: GNU GCC Compiler) ===|
D:\code_cpp\test\main.cpp|9|warning: "/*" within comment [-Wcomment]|
D:\code_cpp\test\main.cpp||In function 'int main()':|
D:\code_cpp\test\main.cpp|9|error: 'j' was not declared in this scope|
D:\code_cpp\test\main.cpp|9|error: expected primary-expression before '/' token|
D:\code_cpp\test\main.cpp|10|error: expected primary-expression before 'return'|
||=== Build failed: 3 error(s), 1 warning(s) (0 minute(s), 1 second(s)) ===|

1.8

1.  ```c++
    cout<<"/*";正确输出
    ```

2. ```c++
   cout<<"*/";正确输出
   ```

3. ```c++
   cout<</*"*/"*/不合法
   ```

4. ```c++
   cout<</*"*/"/*"/*" */;合法输出/*
   ```


1.9 

```c++
int main()
{
    int i=50,sum=0;
    while(i<=100)
    {
        sum+=i;
        i++;
    }
    cout<<sum;
    return 0;
}
```

1.10

```c++
int main()
{
    int i=10;
    while(i>=0)
    {
        cout<<i<<endl;
        i--;
    }

    return 0;
}
```

1.11

```c++
int main()
{
    int m,n,i;
    cout<<"please input m and n(n>m)";
    cin>>m>>n;
    for(i=m;i<=n;i++)
    {
        cout<<i<<endl;
    }
    return 0;
}

```

1.12

-100到100的数相加，0

1.13略

1.14

for适合循环次数固定的场合，但是while适合满足一定的条件的循环

1.15略

1.16

读入数量不定的输入数据：

```c++
int main()
{
    int m=0,sum=0;
    while(cin>>m)
    {
        sum=sum+m;
    }
    cout<<sum;
    return 0;
}
```

注意的是这里是文件需要知道何时结束：win下用ctrl+z+enter表示文件输入结束

或者这里m是int，随便最后输入abc也会结束

1.17-1.18

1occurs9times

1occurs1times
2occurs1times
3occurs1times
4occurs1times
5occurs1times
6occurs1times
7occurs1times
8occurs1times

1.19 if else 

1.20

```c++
int main()
{
    Sales_item book;
    cin>>book;
    cout <<book<<endl;
return 0;
}
```

1.21

```c++
int main()
{
    Sales_item book1,book2;
    cin>>book1;
     cin>>book2;
    cout <<book1+book2<<endl;
return 0;
}

```

1.22

```c++
int main()
{
    Sales_item book1,book2,book3;
    cin>>book1;
    while(cin>>book2)
    {
        book3=book1+book2;
    }
    cout<<book3;
return 0;
}
```

注意我之前写的程序是

```c++
int main()
{
    Sales_item book1,book2;
    cin>>book1;
    while(cin>>book2)
    {
        book2=book1+book2;
    }
    cout<<book2;
return 0;
}
```

我输入三本书的数据，但是输出来是0 0 0 ，是因为这里最后cin读入book2之后循环不满足于是跳出，book2这里读入的是一个不恰当的值，所以只能输出0 0 0

1.23-1.25

```c++
int main()
{
    Sales_item total;
    if(cin>>total){
        Sales_item trans;
        while(cin>>trans){
            if(total.isbn()==trans.isbn())
            {
                total+=trans;
            }
            else{
                cout<<total<<endl;
                total=trans;
            }

        }
       cout<<total;
    }

    else{cout<<"No input!"<<endl;}
return 0;
}
```

