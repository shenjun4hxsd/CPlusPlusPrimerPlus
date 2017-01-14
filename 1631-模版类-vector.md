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