##模版类 vector

在头文件vector中定义了一个vector模版。

要创建vector模版对象，可以使用通常的<type>表示法来指出要使用的类型。另外，vector模版使用动态内存分配，因此可以用初始化参数来指出需要多少的矢量：


```javascript
    using namespace std;
    vector<int> ratings(5);
    
    int n;
    cin >> n;
    vector<double> scores(n);
    
    // 创建vector后，可以使用数组表示法来访问各个元素：
    ratings[0] = 9;
    for (int i = 0; i < n ; i++) {
        cout << scores[i] << endl;
    }
```

```javascript
    const int NUM = 5;
    int main()
    {
        using namespace std;
        vector<int> ratings(NUM);
        vector<string> titles(NUM);
    
        for (int i = 0; i < NUM; i++) {
            cout << "输入Tile :" << i + 1 << endl;
            getline(cin, titles[i]);
            cout << "输入等级：" << i + 1 << endl;
            cin >> ratings[i];
            cin.get();
        }
        
        cout << "======" << endl;
        
        for (int i = 0; i < NUM; i++) {
            cout << "Title :" << titles[i] << ", rating :" << ratings[i] << endl;
        }
    }
```

🔚