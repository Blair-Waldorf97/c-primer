c++primer exercises5-7

​																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																																		5.1

空语句是：语法上需要一条语句但是逻辑不需要，最常见的情况是，循环的全部工作在条件的地方就可以完成。

eg,

```c++
while(cin>>s&&s!=sought)
```

5.2

{}

5.4

(b)中有错误，自爱循环外部无法访问bool status

6.7

局部静态变量：在程序的执行路径第一次经过对象定义语句时被初始化，直到程序结束才被销毁，应用：计算程序被调用的次数。

```c++
int count()
{
    static int  i=0;
    return i++;
}

int main()
{
    int j;
    for(j=0;j<10;j++)
    {
        cout<<count()<<endl;
    }
    return 0;
}
```

  struct

```c++
#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
using namespace std;
struct Student{
    int age;
    string first_name;
    string last_name;
    int standard;
    
};
/*
    add code for struct here.
*/

int main() {
    Student st;
    
    cin >> st.age >> st.first_name >> st.last_name >> st.standard;
    cout << st.age << " " << st.first_name << " " << st.last_name << " " << st.standard;
    
    return 0;
}

```

class

```c++
#include <iostream>
#include <sstream>
using namespace std;

/*
Enter code for class Student here.
Read statement for specification.
*/

int main() {
    int age, standard;
    string first_name, last_name;
    
    cin >> age >> first_name >> last_name >> standard;
    
    Student st;
    st.set_age(age);
    st.set_standard(standard);
    st.set_first_name(first_name);
    st.set_last_name(last_name);
    
    cout << st.get_age() << "\n";
    cout << st.get_last_name() << ", " << st.get_first_name() << "\n";
    cout << st.get_standard() << "\n";
    cout << "\n";
    cout << st.to_string();
    
    return 0;
}

```

## Classes and Objects

```c++
#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
#include <cassert>
using namespace std;
// Write your Student class here
class Student{
 
    int scores[5],sum=0; 
    int count;
    public:
    void input()
    {
        
            for (int j=0;j<5;j++)
            {
            cin>>scores[j];
            }
            

    }
    int calculateTotalScore()
    {
      for (int j=0;j<5;j++)
            {
                sum=sum+scores[j];
            }
        return sum;
    }
        
};

int main() {
    int n; // number of students
    cin >> n;
    Student *s = new Student[n]; // an array of n students
    
    for(int i = 0; i < n; i++){
        s[i].input();
    }

    // calculate kristen's score
    int kristen_score = s[0].calculateTotalScore();

    // determine how many students scored higher than kristen
    int count = 0; 
    for(int i = 1; i < n; i++){
        int total = s[i].calculateTotalScore();
        if(total > kristen_score){
            count++;
        }
    }

    // print result
    cout << count;
    
    return 0;
}

```

