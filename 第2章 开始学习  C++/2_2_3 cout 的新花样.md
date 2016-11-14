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

>**cout 和 printf()**

>&emsp;&emsp;如果已经习惯了 C 语言和 `printf()`，可能觉得 `cout` 看起来很奇怪。程序员甚至可能固执地坚持使用 `printf()`。但与使用所有转换说明的 `printf()` 相比，`cout` 的外观一点也不奇怪。更重要的是，`cout` 还有明显的优点。它能够识别类型的功能表明，其设计更灵活、更好用。另外，它是可扩展的。也就是说，可以重新定义 `<<` 运算符，使 `cout` 能够识别和显示所开发的新数据类型。如果喜欢 `printf()` 提供的细致的控制功能，可以使用更高级的 `cout` 来获得相同的效果。

🔚
