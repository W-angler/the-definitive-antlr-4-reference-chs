## antlrС��ţ��

������������ʼ���ǵĵ�һ��������Ŀ��

�������ǻṹ��`C`������������������`Java`��һ���﷨�Ӽ�����ϸ��˵������ʶ����`{1,2,3}`����`{1,{2,3},4}`�������ɴ����Ű�Χ�ģ���Ƕ�ף�������������ṹ�������������飬Ҳ�п����ǽṹ��ĳ�ʼ��������﷨�ںܶ�����¶��Ǻ����õģ����磬���ǿ�������������һ��������`int`����ת��Ϊ�ֽ����飨�����������г�ʼֵ��С����һ���ֽ��ڵĻ�����C����Դ���ع����ߡ�����Ҳ����������﷨����Java��`short`����ת��Ϊ�ַ��������磬���ǿ��Խ�����Ĵ��룺

    static short[] data = {1,2,3};

����ת��ΪΪ��

    static String data = "\u0001\u0002\u0003"; // Java���ַ����޷��ŵ�short

����`Unicode`ʹ���ĸ�ʮ������λ����ʾ16λ���ַ�ֵ,����`\u0001`��

��������֮����Ҫ�����ת��������Ϊ����Java��`.class`�ļ��У�����һЩ���ơ���Java��`.class`�ļ��У�����ĳ�ʼ������`data[0]=1;data[1]=2; data[2]=3;`��������ʽ��ֵ��ʼ����������һ��������ʼ�����ݵĽ��մ���顣��ΪJava�淶�������˳�ʼ�������Ĵ�С����������ĳ�ʼ��СҲ�������ˡ�����ͬ���ǣ���Java`.class`�ļ��У��ַ�������������`short`���е���ʽ�洢�ģ����ԣ�������ת��Ϊ�ַ����������ɸ����յ�`.class`�ļ�������ͻ�Ƴ�ʼ�������Ĵ�С���ơ�

����ͨ�����������Ŀ���㽫��ѧϰ��antlr��`�﷨����`�﷨�������﷨�ļ���������Щ��������ν���Java�����а���antlr���ɵ��﷨���������룬�Լ����ʹ�ü�����������һ����������

### 3.1 antlr�Ĺ��ߡ�����ʱ���Լ����ɵĴ���

To get started, let��s peek inside ANTLR��s jar. There are two key ANTLR components: the ANTLR tool itself and the ANTLR runtime (parse-time) API. When we say ��run ANTLR on a grammar,�� we��re talking about running the ANTLR tool, class org.antlr.v4.Tool. Running ANTLR generates code (a parser and a lexer) that recognizes sentences in the language described by the grammar. A lexer breaks up an input stream of characters into tokens and passes them to a parser that checks the syntax. The runtime is a library of classes and methods needed by that generated code such as Parser, Lexer, and Token. First we run ANTLR on a grammar and then compile the generated code against the runtime classes in the jar. Ultimately, the compiled application runs in conjunction with the runtime classes. 












