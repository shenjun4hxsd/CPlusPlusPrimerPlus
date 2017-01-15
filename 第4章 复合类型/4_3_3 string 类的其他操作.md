##string 类的其他操作

```javascript
    #include <cstring> // 提供C语言函数库中字符串处理的相关函数
    
    strcpy(charr1, charr2); // 将字符串复制到字符数组中
    strcat(charr1, charr2); // 将字符串附加到字符数组末尾。
```

```javascript
    using namespace std;
    char charr1[] {"name:"};
    char charr2[] {"shenjun"};
    string str1;
    string str2 {"name"};
    strcpy(charr1, charr2);  // 把charr2的内容拷贝到charr1中
    str1 = str2;
    
    
    strcat(charr1, charr2);    // 把charr2中的内容添加到charr1的后面
    str1 += str2;
    
    int len1 = strlen(charr1);
    int len2 = str1.size();
```

🔚