<center><h2>ANTLR文档（中文简体）</h2></center>

　　antlr是一个用于读写、处理、执行、翻译结构化文本或者二进制文件的解析生成器。它被广泛的使用在编译语言、开发工具和框架中。通过解析特定的文法，antlr可以生成能够进行词法分析（lexer）和语法树解析（parser）的自动化程序，并且具有较强的定制性、拓展性。

　　在入坑PLT之前就接触过antlr，而这个学期的解释器构造课程又需要使用，其官方文档很全面，但是网上所能找到的中文翻译都比较粗糙，刚好大三上学期还要再刷高一点六级的分数，于是便有了自己翻译的想法，提高英语，顺便造福他人。

## 前言

　　这是第一次翻译，估计所有的英语都已经还给老师了。

　　翻译要求`信、达、雅`，我只能说尽量以简单易懂的方式进行表述，不要出现那种翻译腔吧！

　　在翻译的过程中，有些术语用中文可能会更让人迷惑，例如`Token`，翻译为`令牌 `、`标记`、`记号`都会让人很迷惑，所以，有些术语在本书的翻译过程中可能并不翻译。在这里提前让大家了解一下这些术语，便于对整本书的了解。

 * Token：单词，记号，标记，或者其他之类的翻译，是用来表述语法分析中的最小单位的一个术语，它一般是一个字符串字面值加上一些对这个字面值的简单描述，如token出现的`行列号`、`token类型`等等。相当于英语中的一个单词，中文中的一个词语。
 * Lexer：词法分析器，又称扫描器，用于将我们编写的文本代码流解析为一个一个的`Token`，分析得到的`Token`以供后续语法分析使用。
 * Parser：语法分析器，它的作用是进行语法检查、并构建由输入的单词组成的数据结构（一般是语法树、抽象语法树（AST）等层次化的数据结构）。语法分析器需要从词法分析器中获取`token流`。

　　而有些涉及到文法的二义性的问题，这个则与英语和汉语之间的差异性有关。例如在书中有一个` You Can’t Put Too Much Water into a Nuclear Reactor`的例子，用中文是很难表述出二义性的。这个我尽量结合英语的一些语法来解释一下。
## 协议

　　如果无意中对原文作者侵犯了著作权，本人承诺会马上删除并承担相应的责任。

　　当然，我会尽量与作者取得联系，争取他的同意。

　　本书翻译采用`MIT`协议：
> MIT License

> Copyright (c) 2016 汪鹏程

> Permission is hereby granted, free of charge, to any person obtaining a copy

> of this software and associated documentation files (the "Software"), to deal

> in the Software without restriction, including without limitation the rights

> to use, copy, modify, merge, publish, distribute, sublicense, and/or sell

> copies of the Software, and to permit persons to whom the Software is

> furnished to do so, subject to the following conditions:

> The above copyright notice and this permission notice shall be included in all

> copies or substantial portions of the Software.

> THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR

> IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,

> FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE

> AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER

> LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,

> OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE

> SOFTWARE.

