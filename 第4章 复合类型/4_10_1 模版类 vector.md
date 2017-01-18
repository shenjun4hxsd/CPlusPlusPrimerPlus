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
        
        
###Stack

empty() 堆栈为空则返回真

pop() 移除栈顶元素

push() 在栈顶增加元素

size() 返回栈中元素数目

top() 返回栈顶元素


        stack<int> p;
        for (int i = 0; i < 10; i++) {
            p.push(i);
        }
        
        printf("size = %ld\n", p.size());
        
        while (!p.empty()) {
            printf("%d\n", p.top());
            p.pop();
        }
        
        
###list

        assign() 给list赋值 
        back() 返回最后一个元素 
        begin() 返回指向第一个元素的迭代器 
        clear() 删除所有元素 
        empty() 如果list是空的则返回true 
        end() 返回末尾的迭代器 
        erase() 删除一个元素 
        front() 返回第一个元素 
        get_allocator() 返回list的配置器 
        insert() 插入一个元素到list中 
        max_size() 返回list能容纳的最大元素数量 
        merge() 合并两个list 
        pop_back() 删除最后一个元素 
        pop_front() 删除第一个元素 
        push_back() 在list的末尾添加一个元素 
        push_front() 在list的头部添加一个元素 
        rbegin() 返回指向第一个元素的逆向迭代器 
        remove() 从list删除元素 
        remove_if() 按指定条件删除元素 
        rend() 指向list末尾的逆向迭代器 
        resize() 改变list的大小 
        reverse() 把list的元素倒转 
        size() 返回list中的元素个数 
        sort() 给list排序 
        splice() 合并两个list 
        swap() 交换两个list 
        unique() 删除list中重复的元素
        
        
        list<int> p;
        for (int i = 0; i < 10; i++) {
            p.push_back(i);
//            p.push_front(i);
        }
        
        p.insert(p.begin()++, 4, 100);

        p.erase(p.begin()++);
        
        while (!p.empty()) {
            printf("size = %d\n", p.front());
            p.pop_front();
        }
        
        
🔚