c++primer exercises3

3.1-3.13略

3.14-15

```c++
int main()
{
    string word;
    vector<string> str;
    while(cin>>word)
    {
        str.push_back(word);
    }
    return 0;
}

```

3..16

```c++
int main()
{
    string word;
    int i;
    vector<string> str;
    while(cin>>word)
    {
        str.push_back(word);
    }
    int m=str.size();
    for(i=0;i<m;i++)
        cout<<str[i]<<endl;
    return 0;
}

```

本来可以用范围for语句处理vector中的元素，但是c98不允许使用，

c++11可以

```c++
for(auto &i : str)
```

3.17

```c++
#include <iostream>
#include<vector>
#include"Sales_item.h"
using namespace std;

int main()
{
    string word;
    int i,j;
    vector<string> str;
    while(cin>>word)
    {
        str.push_back(word);
    }
    int m=str.size();
    for(i=0;i<m;i++){
        for(j=0;j<str[i].size();j++)
    {
        str[i][j]=str[i][j]-32;
    }
        cout<<str[i]<<endl;}
    return 0;
}

```

3.21

```c++
int main()
{
    string word;
    int i,j;
    vector<string> str;
    while(cin>>word)
    {
        str.push_back(word);
    }
    for(auto it=str.begin();it!=str.end()&& !isspace(*it);++it)
        cout<<*it;
    return 0;
}
```

3.22-3.23

```c++
int main()
{
    string word;
    int i,j;
    vector<string> str;
    while(cin>>word)
    {
        str.push_back(word);
    }
    for(auto it=str.begin();it!=str.end();++it)
    {
        for(auto m=it->begin();m!=it->end()&& !isspace(*m);++m)
    {
        toupper(*m);
    }
        cout<<*it;
    }
    return 0;
}

```

ctype.h文件中包含的函数有：isspace()检验非空，toupper将小写改为大写



