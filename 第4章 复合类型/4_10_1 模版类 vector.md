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