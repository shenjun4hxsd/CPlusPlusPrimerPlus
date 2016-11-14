##使用 cout 进行 C++ 输出

```javascript    
    cout << "Come up and C++ me some time.";
```

&emsp;&emsp;`cout` （流）是一个预定义的对象，知道如何显示字符串、数字和单个字符等。`<<` 符号（插入运算符）表示该语句将字符串发送给 `cout` ： 该符号指出了信息流动的路径。

&emsp;&emsp;`cout` 对象表示一个输出流，其属性是在 `iostream` 文件中定义的。`cout` 的对象属性包括一个插入运算符（ `<<` ），它可以将其右侧的信息插入到流中。

>&emsp;&emsp;`<<` 运算符是一个被重载的运算符，通过重载，同一个运算符将有不同的含义。编译器通过上下文来确定运算符的含义。

>例如：`&` 符号既表示地址运算符，又表示按位 AND 运算符；
`*` 既表示乘法，又表示对指针解除引用。C++ 扩展了运算符重载的概念，允许为用户定义的类型（类）重新定义运算符的含义。


####&emsp;&emsp;1. 控制符 endl

```javascript
    cout << endl;
```

&emsp;&emsp;`endl` 是一个特殊的 C++ 符号，表示：换行。`endl` 是在头文件 `iostream` 中定义的，且位于名称空间 `std` 中。

&emsp;&emsp;**示例:**

```javascript
    cout << "The Good, the";
    cout << "Bad, ";
    cout << "and the Ukulele";
    cout << endl;
```
&emsp;&emsp;输出如下：
```javascript
    The Good, theBad, and the Ukulele
```

####&emsp;&emsp;2. 换行符

```javascript
    cout << "What's next?\n";
```

&emsp;&emsp;`\n` 被视为一个字符，名为换行符。

>&emsp;&emsp;`endl` 确保程序继续运行前刷新输出（将其立即显示在屏幕上）；而 `\n` 不能提供这样的保证，这意味着在有些系统中，有时可能在您输入信息后才会出现提示。

&emsp;&emsp;换行符是一种被称为 “转义序列” 的按键组合。



