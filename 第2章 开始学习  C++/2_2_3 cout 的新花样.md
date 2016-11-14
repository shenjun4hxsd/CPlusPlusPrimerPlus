##cout 的新花样

&emsp;&emsp;使用 `cout` 打印变量，该变量的值是一个整数：
```javascript
    cout << carrots;
```
&emsp;&emsp;C 语言的多功能输出函数 `printf()`:

```javascript
    printf("Printing a string: %s\n", "25");    // 使用 %s 指定打印字符串
    printf("Printing a integer: %d\n", 25);     // 使用 %d 指定打印整数
```
&emsp;&emsp;如果让 `printf()` 打印字符串，但又错误地提供了一个整数，由于 `printf()` 不够精密，因此根本发现不了错误。它将继续处理，显示一堆乱码。

&emsp;&emsp;`cout` 的智能行为源自 C++ 的面向对象特性。实际上，C++ 插入运算符（ `<<` ）将根据其后的数据类型相应地调整其行为，这是一个运算符重载的例子。
