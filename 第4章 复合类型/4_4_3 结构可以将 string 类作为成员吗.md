##结构可以将 string 类作为成员吗

```javascript
    #include <string>
    struct StudentInfo
    {
    //    char name[20];
        std::string name;
        int age;
    };
```