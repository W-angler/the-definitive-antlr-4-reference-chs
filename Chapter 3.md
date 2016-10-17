## antlr小试牛刀

　　接下来开始我们的第一个入门项目。

　　我们会构建`C`或者它的派生语言如`Java`的一个语法子集。详细点说，就是识别像`{1,2,3}`或者`{1,{2,3},4}`这样的由大括号包围的（或嵌套）的整数。这个结构可能是整数数组，也有可能是结构体的初始化。这个语法在很多情况下都是很有用的，例如，我们可以用它来构建一个用来将`int`数组转换为字节数组（如果数组的所有初始值大小都在一个字节内的话）的C语言源码重构工具。我们也可以用这个语法来将Java的`short`数组转换为字符串，例如，我们可以将下面的代码：

    static short[] data = {1,2,3};

　　转化为为：

    static String data = "\u0001\u0002\u0003"; // Java的字符是无符号的short

　　`Unicode`使用四个十六进制位来表示16位的字符值,例如`\u0001`。

　　我们之所以要做这个转换，是因为，在Java的`.class`文件中，存在一些限制。在Java的`.class`文件中，数组的初始化是像`data[0]=1;data[1]=2; data[2]=3;`这样的显式赋值初始化，而不是一个包含初始化数据的紧凑代码块。因为Java规范中限制了初始化方法的大小，所以数组的初始大小也被限制了。而不同的是，在Java`.class`文件中，字符串是以连续的`short`序列的形式存储的，所以，将数组转换为字符串可以生成更紧凑的`.class`文件，并且突破初始化方法的大小限制。

　　通过这个入门项目，你将会学习，antlr的`语法定义`语法，它将语法文件生成了哪些东西，如何将在Java程序中包含antlr生成的语法分析器代码，以及如何使用监听器来构建一个翻译器。

### 3.1 antlr的工具、运行时，以及生成的代码

To get started, let’s peek inside ANTLR’s jar. There are two key ANTLR components: the ANTLR tool itself and the ANTLR runtime (parse-time) API. When we say “run ANTLR on a grammar,” we’re talking about running the ANTLR tool, class org.antlr.v4.Tool. Running ANTLR generates code (a parser and a lexer) that recognizes sentences in the language described by the grammar. A lexer breaks up an input stream of characters into tokens and passes them to a parser that checks the syntax. The runtime is a library of classes and methods needed by that generated code such as Parser, Lexer, and Token. First we run ANTLR on a grammar and then compile the generated code against the runtime classes in the jar. Ultimately, the compiled application runs in conjunction with the runtime classes. 












