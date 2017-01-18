##模版类 vector

```javascipt
        // 容器
//        vector<int> a {1,2,3,4,5};
        vector<int> a;
        for (int i = 0; i < 5; i++) {
            a.push_back(i);
        }
        
        a.insert(a.begin()+3, 10);   //  插入
        a.erase(a.begin()+2);        //  删除
        
//        for (int i = 0; i < a.size(); i++) {
//            printf(" %d \n", a[i]);
//        }
        
        for (vector<int>::iterator it = a.begin(); it != a.end(); it++) {
            printf("%d\n", *it);
        }
        
        a.clear();
        
```


###Queue


queue 模板类的定义在<queue>头文件中。
与stack 模板类很相似，queue 模板类也需要两个模板参数，一个是元素类型，一个容器类
型，元素类型是必要的，容器类型是可选的，默认为deque 类型。
定义queue 对象的示例代码如下：
queue<int> q1;
queue<double> q2;

queue 的基本操作有：

        入队，如例：q.push(x); 将x 接到队列的末端。
        出队，如例：q.pop(); 弹出队列的第一个元素，注意，并不会返回被弹出元素的值。
        访问队首元素，如例：q.front()，即最早被压入队列的元素。
        访问队尾元素，如例：q.back()，即最后被压入队列的元素。
        判断队列空，如例：q.empty()，当队列空时，返回true。
        访问队列中的元素个数，如例：q.size()
        
        
          queue<int> q;
        for (int i = 0; i < 10; i++) {
            q.push(i);
        }
        
        printf("size = %ld\n", q.size());
        
        while (!q.empty()) {
            printf("%d\n", q.front());
            q.pop();
        }