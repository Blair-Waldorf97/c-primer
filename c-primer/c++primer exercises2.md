c++primer exercises2

2.1

区别是该类型数据所占的比特数，无符号整形仅能表示大于等于零的数值

2.2

本金：unsigned int 利率\付款：double   原则：1.明确数值不为负用无符号.2执行浮点数运算用double

2.3-2.4

```c++
int main()
{
    unsigned u=10,u2=42;
    cout<<u2-u<<endl;    \\32
    cout<<u-u2<<endl;    \\4294967264
    int i=10,i2=42;
     cout<<i2-i<<endl;    \\32
    cout<<i-i2<<endl;      \\-32
     cout<<i-u<<endl;     \\0
    cout<<u-i<<endl;   \\0
    return 0;
}
```

2.5-2.14略

2.15

(b)引用类型必须是一个对象

(d)引用必须初始化

2.16

把double赋值给int是很危险的

2.17

10 10