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