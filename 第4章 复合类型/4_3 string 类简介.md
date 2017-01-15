##string 类简介

可以使用C风格字符串来初始化string对象。
可以使用cin来将键盘输入存储到string对象中。
可以使用cout来显示string对象。
可以使用数组表示法来访问存储在string对象中的字符。


#include <string>

int main()
{
    using namespace std;
    
    string name = "shenjun";
    
    cout << name << end;
    
    return 0;
}