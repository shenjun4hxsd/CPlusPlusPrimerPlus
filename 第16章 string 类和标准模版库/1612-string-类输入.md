##string类输入


1、对于C风格字符串，有3种方式

```javascript 
    using namespace std;
    char info[100];
    cout << "请输入：";
    cin >> info;
//    cin.getline(info, 100);
//    cin.get(info, 100);
    cin.getline(info, 100, ':');  // getline可以使用哪个字符来确定输入的边界：
    cout << info << endl;

```

2、对于string对象有2种方式

```javascript
    string stuff;
    cout << "请输入：";
    // cin >> stuff;
    // getline(cin, stuff);

    // getline可以使用哪个字符来确定输入的边界： 
    // 自动调整目标string对象的大小，使之刚好能够存储输入的字符
    getline(cin, stuff, ':');   
    cout << stuff << endl;
```

3、比较

```javascript
    char fname[10];
    // cin >> fname;             // 如果输入的内容大于9个会产生问题
    cin.getline(fname, 10);   // 最多只获取9个字符的输入
    cout << fname << endl;
```

```javascript
    string lname;
    // cin >> lname; // 输入的内容可以很长
    getline(cin, lname);
    cout << lname << endl;
```


##示例：

```javascript
    #include <iostream>
    #include <string>
    #include <fstream>
    #include <cstdlib>
    
    int main(int argc, const char * argv[]) {
        using namespace std;
        ifstream fin;
        if(fin.is_open() == false)
        {
            cerr << "Can't open file. Bye.\n";
            exit(EXIT_FAILURE);
        }
        string item;
        int count = 0;
        getline(fin, item, ':');
        while (fin) { // while input is good
            ++count;
            cout << count << " : " << item << endl;
            getline(fin, item, ':');
        }
        cout << "Done\n";
        fin.close();
        
        return 0;
    }
```




