##C++ 预处理和 iostream 文件

```javascript
    #include <iostream>
    using namespace std;
```

&emsp;&emsp;C++ 和 C 一样，也使用一个预处理器，该程序在进行主编译之前对源文件进行处理（有些 C++ 实现使用翻译器程序将 C++ 程序转换为 C 程序。虽然翻译器也是一种预处理器，但这里只讨论以名称 # 开头的编译指令）。不必执行任何特殊的操作来调用该预处理器，它会在编译程序时自动运行。

```javascript
    #include <iostream>
```

&emsp;&emsp;该编译指令导致预处理器将 `iostream` 文件的内容添加到程序中。这是一种典型的预处理器操作：在源代码被编译之前，替换或添加文本。

&emsp;&emsp;`#include` 编译指令导致 `iostream` 文件的内容随源代码文件的内容一起被发送给编译器。实际上，`iostream` 文件的内容将取代程序中的代码行 `#include <iostream>`。原始文件没有被修改，而是将源代码文件和 `iostream` 组合成一个复合文件，编译的下一阶段将使用该文件。

>&emsp;&emsp;**注意：使用 `cin` 和 `cout` 进行输入和输出的程序必须包含文件 `iostream`。**