##在多函数程序中使用 using 编译指令

&emsp;&emsp;`cout` 位于名称空间 `std` 中。

```javascript
    #include <iostream>
    using namespace std;
    
    void simon(int);

    int main()
    {
        simon(3);
        cout << "Pick an integer: ";
        int count;
        cin >> count;
        cout << "Done!" << endl;
        return 0;
    }

    void simon(int n)
    {
        cout << "Simon says touch your toes" << n << " times." << endl;
    }
```

&emsp;&emsp;● 将 `using namespace std` 放在函数定义之前，让文件中所有的函数都能够使用名称空间 `std` 中所有的元素。