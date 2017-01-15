##比较数组、vector 对象和 array 对象

```javascript
    #include <iostream>
    #include <vector> // STL C++98
    #include <array> // C++11
    
    int main(int argc, const char * argv[]) {
        
        using namespace std;
        int a1[4] = {1,2,3,4};
        vector<int> a2(4);
        
        a2[1] = 1;
        a2[2] = 2;
        a2[3] = 3;
        a2[4] = 4;
        
        array<int, 4> a3 = {3,4,5,6};
        array<int, 4> a4 = a3; // 可以直接赋值 数组须逐元素赋值
        
        cout << "a1[2] :" << a1[2] << " at " << &a1[2] << endl;  // 栈（静态存储区）
        cout << "a2[2] :" << a2[2] << " at " << &a2[2] << endl;  // 自由存储区或堆
        cout << "a3[2] :" << a3[2] << " at " << &a3[2] << endl;  // 栈（静态存储区）
        cout << "a4[2] :" << a4[2] << " at " << &a4[2] << endl;
        
        a1[-2] = 20; // 表示 *(a1-2)=20 C++也不检查这种越界错误 表明数组的行为是不安全的
        
        // vector和array也可以使用上面的方式，然后，还有其他选择
        a2.at(1) = 10;  // 使用at()时，将在运行期间捕获非法索引。
        a3.at(1) = 5;
        
        // 它们包含成员函数begin()和end()，让您能够确定边界。
        vector<int>::iterator p1 = a2.begin();
        array<int, 4>::iterator p2 = a3.end();
        
        return 0;
    }

```