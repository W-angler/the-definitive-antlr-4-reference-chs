## ��ʶantlr

�����Ȿ���һ���ֵ�Ŀ�����ô�Ҷ�`antlr`��������һ��ֱ�۴��µ��˽⣬���ҿ���̽��`����Ӧ��`���ó̡������Ƕ���`antlr`���˴��µ��˽�����ǽ�����`�ڶ�����`���Ķ�ϵͳ��ʹ��һϵ����ʵ�����е�������ѧϰ`antlr`����Ȼ���ڿ�ʼ��Щ֮ǰ��������Ҫ��װ`antlr`�����ҳ�������һ��`Hello world`����������ѧϰ��

### 1.1 ��װantlr

����`antlr`��ʹ��`java`��д���ɵģ��������㿪ʼ֮ǰ�����������ĵ����ϰ�װ`java`�����л�����1.6���߸��ߵİ汾�������Ǳ���ģ���ʹ������`antlr`�����ɱ������д�ɵ�`parser`������`C#`��`C++`������ϣ���ڲ��õĽ�����������������Ŀ���������ԣ���

****
> #### **Ϊʲô�Ȿ��ʹ�������л�����**

> ���Ȿ���У���ʼ�������Ƕ���ʹ�������У�`shell`����`cmd`��������`antlr`�͹������ǵ�Ӧ�ó�����Ϊÿ������Ա��ʹ�õĿ��������Ͳ���ϵͳ����һ����������ϵͳ�������нӿ�ȴ�����������еġ�ʹ��������Ҳ��ʹ��������ѧϰ����Ӧ�ÿ����е�ÿһ����ú���ȷֱ�ס����������У���ʹ�õ���Mac OS X��`shell`��������Щ����������Ҳ�ǿ������κ�`��unixϵͳ`��`shell`��`windows`�����еġ�

****

������װantlr�ܼ򵥣���ֻ��Ҫ�������µ�antlr��jar�ļ�������ע������ʹ�õ���4.0�汾������ʹ�õ�4.5.3������������벿�ֳ��ְ汾��һ������ӣ������Ӱ�죩������:[antlr-4.5.3-complete.jar](http://www.antlr.org/download/antlr-4.5.3-complete.jar)��Ȼ��������һ�����ʵ�λ�þͺ��ˡ����jar�ļ�������antlr�����һ�������������ֱ������`antlr��������`�Լ����롢ִ����antlr���ɵ�ʶ����򣨴ʷ����������﷨�������ȣ����򵥵�˵��antlr���Խ���������﷨ת��Ϊһ������ʶ���������﷨�ľ��ӵĳ������磬����һ��`json`���﷨��antlr�����Զ�����һ�����򣬶�ͨ��һЩ��antlr����ʱ��������֧���������������࣬����Ժܷ����ʶ���������json�ı���


�������jar�ļ�Ҳ�������������������õ���⣺һ�������[tree layout](http://code.google.com/p/treelayout)���[StringTemplate](http://www.stringtemplate.org)��һ���������ɴ�����������ṹ���ı��ĺ����õ�ģ�����棩����antlr 4.0��ʹ��antlr v3д�ģ�����ע�������Ծ٣�[ά���ٿ�](https://en.wikipedia.org/wiki/Bootstrapping_#40compilers#41)��[���������Ծ�ԭ����ʲô��](http://www.zhihu.com/question/28513473)�������������jar�ļ���Ҳ������֮ǰ�汾��antlr��

****

> #### **StringTemplateģ������**

> StringTemplate��һ��Java��д����������Դ���롢��ҳ���ʼ������������ṹ���ı���ģ�����棨�ṩ��C#��Python��Ruby��Scala�Ľӿڣ���StringTemplate�ر��ó�������Ϊ�������Ŀ�ꡢ�����վ�����ģ������������Ҳ֧�ֹ��ʻ�/���ػ���[jGuru.com](http://www.jguru.com)���������˶���Ŀ�����StringTemplateҲ����������antlr�Ĺ�����������������ǿantlr v3��antlr v4�Ĵ�������������������Բ鿴����[����](http://www.stringtemplate.org/about.html)��

****

������������������antlr��[����](http://www.antlr.org)����antlr�����ߣ���Ҳ����ʹ�������й���`curl`����ȡ��

    $ cd /usr/local/lib
	$ curl -O http://www.antlr.org/download/antlr-4.5.3-complete.jar

������Unix�ϣ�`/usr/local/lib`�Ǵ洢��antlr�������ļ��ľ���λ�á�����Windows�ϣ��ƺ�û�й涨�ĸ��ļ�����ר�ŷ�����ģ����������ֱ�ӽ�������������ĿĿ¼�¡�������Ŀ�����������Ҫ���㽫jar�ļ��������`����Ӧ��`��Ŀ�������б�����ע������`Eclipse`��`Build Path`���С���Ҳ����Ҫ�޸����ýű����������ļ�֮��ġ���������Ҫ���Ľ�����ȷ��JRE֪����ôȥ�������jar�ļ�������ע�����£�ȷ����������`CLASSPATH`�������jar�ļ�����


������Ϊ�����ʼ���ն���ʹ��������������antlr�������ڴ�֮ǰ������Ҫ��һ����Ҳ��Ψһ��һ�����������£�����`CLASSPATH`�������������ú�`CLASSPATH`��JRE�Ϳ����ҵ�antlr���ߺ�����ʱ�����ˡ���Unixϵͳ�ϣ������ִ�����µ��������ֱ����ӵ�shell��`�����ű�`������ע��`.bash_rc`����`.bash.profile`����shell�����������Ҳ������ӵ�`/etc/profile`���

    export CLASSPATH=".:/usr/local/lib/antlr-4.5.3-complete.jar:$CLASSPATH" 

�����Ǹ�`.`����ǰĿ¼�ı�־����һ���ܹؼ��ĵط���û������java�ı�������JVM����ӵ�ǰĿ¼�µ�`.class`�ļ����ڱ����У����롢���Զ����ڵ�ǰĿ¼�½��еġ�

���������Щ֮����Ϳ���ͨ�����в��������в�����antlr���������antlr�Ƿ�װ�ɹ����������`java -jar`������jar�ļ�������ֱ������`org.antlr.v4.Tool`��

    $ java -jar /usr/local/lib/antlr-4.5.3-complete.jar
	    ANTLR Parser Generator  Version 4.5.3
	    -o ___              specify output directory where all output is generated
	    -lib ___            specify location of grammars, tokens files
	    ....
	
	$ java org.antlr.v4.Tool 
	    ANTLR Parser Generator  Version 4.5.3
	    -o ___              specify output directory where all output is generated
	    -lib ___            specify location of grammars, tokens files
	    ....

�������һֱ����ͨ��������ô��������������antlr�����ǽ���һ���ǳ�ʹ������飬���ԣ�����ø���Щ������һ��`������alias��`�������У��һ�ʹ��`antlr4`����������unix���������壺

    alias antlr4='java -jar /usr/local/lib/antlr-4.5.3-complete.jar' 

�������ߣ���Ҳ���Խ����µĽű��������`/usr/local/bin`�£�����ע���ļ���һ�е�`#!/bin/sh`��Ҫ��ϵͳ��������

    #!/bin/sh
	java -cp "/usr/local/lib/antlr-4.5.3-complete.jar:$CLASSPATH" org.antlr.v4.Tool $*

������Windows�ϣ������������һ�����������jar�ļ�����`C:\libraries`�£���

    java -cp C:\libraries\antlr-4.5.3-complete.jar;%CLASSPATH% org.antlr.v4.Tool %* 

����������Щ����Ϳ���ֱ������`antlr4`�����ˡ�

    $ antlr4
	    ANTLR Parser Generator  Version 4.5.3
	    -o ___              specify output directory where all output is generated
	    -lib ___            specify location of grammars, tokens files
	    ....

����������ܿ������к���ֵİ�����Ϣ��˵�����Ѱ�װ�ɹ��ˣ����Ѿ�׼���ó�Ϊantlr��˾���ˡ�

	
### 1.2 ִ�С�����antlr���ɹ���

��������һ��ʶ����`hello parrt`��`hello world`�����ľ��ӵ��﷨��

`Hello.g4`

    grammar Hello; //����һ����Hello���﷨
    r : 'hello' ID; //ƥ��ؼ���hello�͸����ں���ı�ʶ��
	ID : [a-z]+; //ƥ��Сд��ĸ��ɵı�ʶ��
	WS : [ \t\r\n]+ -> skip; //��������������Щ�ַ� 

����Ϊ�˱���һ�е����࣬���ǿ��԰��﷨�ļ�`Hello.g4`����ĳ���������ļ����У�����`/tmp/test`��Ȼ�����ǾͿ�������antlr���ұ������ɵĽ���ˡ�

    $ cd /tmp/test
	$ #����ճ����������Hello.g4��/tmp/test
	$ antlr4 Hello.g4 #����lexer��parser
	$ ls
	Hello.g4 HelloLexer.java HelloParser.java Hello.tokens HelloLexer.tokens HelloBaseListener.java HelloListener.java 
	$ javac *.java #����antlr���ɵĴ���

������Hello.g4������antlr���߽�������һ����ִ�е�ʶ��������`HelloParser.java`��`HelloLexer.java`��,�������ǲ�û��`main����`������ʶ�������������ǽ�������һ��ѧϰʲô��`lexer`��`parser`����������һ����Ŀ��ʼʱ�����������ľ������ڿ�������������Ӧ��֮ǰ���㽫��ͼ�����ͬ�ļ��﷨�򽻵�������������Ա���Ϊÿ���﷨дһ��`main����`�����nice��

�������ң�antlr������ʱ�����ṩ��һ�����������ԵĲ��Թ���`TestRig`��������ʶ����ʶ��`�ļ�����`��`��׼����`�Ĺ����г��ֺܶ����Ϣ��`TestRig`ͨ��ʹ��java��`�������`�����ñ�����ʶ��������֮ǰһ���������Ҳ��������һ����������д��`shell�ű�`����`�������ļ�`�С���֮���������`grun`����Ȼ����Ҳ��������Ϊ�����ġ�

    alias grun='java org.antlr.v4.runtime.misc.TestRig' 

����������Թ���ʹ��`�﷨����`��`��ʼ�﷨����`�Լ�һЩ��������ѡ�������ʽ��ѡ����Ϊ������`��ʼ�﷨����`������`main()`������������������Ҫ��ӡ��ʶ������й�����`token`��`token`����ؼ���`hello`�ͱ���`parrt`�����ĵ��ʣ���Ϊ�˲�������﷨�����ǿ���������һ��������`grun`��

    $ grun Hello r -tokens #��ʼʹ��TestRig�����﷨Hello��r������token����ʽ���
	hello parrt #��������Ҫʶ����ı�
	EOF # unix����ctrl-D��Windows����Ctrl+Z
	[@0,0:4='hello',<1>,1:0] #��������grun�����
	[@1,6:10='parrt',<2>,1:6]
	[@2,12:11='<EOF>',<-1>,2:0]

��������`grun`����û����з�֮�󣬿���̨�������ĵصȴ�������`hello parrt`��һ�����з�������㻹��������`EOF`����ֹ��׼���룬����������򽫻�һֱ���㣬ֱ����ĵ��ϡ�һ��ʶ������ȡ�����е����룬`TestRig`�����ӡ�����е�token��ʹ��`-tokens`��������

���������ÿһ�д���һ��token�����Ὣʶ�����token��ÿ����Ϣ����ӡ�˳��������磬`[@1,6:10='parrt',<2>,1:6]`�������������token�ǵڶ���token��������0��ʼ����token�������Ǵ�`6`��`10`���ַ�������Ҳ�Ǵ�0��ʼ����������`parrt`��token������`2`����`��1��`����1��ʼ������`��6��`��ʼ��������0��ʼ��`tab`�����ǵ�����һ���ַ�����

��������Ҳ���Ժ����׵ش�ӡ`Lisp���`���﷨������������ע��`Lisp���`�����ҿ�������`�����﷨��`�������У���ʼ��һ�������ĸ��ڵ㣬֮�������Ǹýڵ��֦Ҷ����

    $ grun Hello r -tree
	hello parrt
	EOF
	(r hello parrt)

������Ȼ�������и�ֱ�۵ķ�ʽ����ʾʶ���������ʶ��������ı��ġ������ӻ�����������`-gui`��������TestRig�������ᴴ��һ����������ĶԻ���

![](http://www.w-angler.com/static/images/2016-10-09_AACD48F85B667001077EBB8997E59C2D.png)

����������������`TestRig`�������һЩ������Ϣ��

    $ grun
	java org.antlr.v4.runtime.misc.TestRig GrammarName startRuleName [-tokens] [-tree] [-gui] [-ps file.ps] [-encoding encodingname] [-trace] [-diagnostics] [-SLL] [input-filename(s)]
	Use startRuleName='tokens' if GrammarName is a lexer grammar. Omitting input-filename makes rig read from stdin.

������������ѧϰ�����룬���ǽ�����ʹ����Щ���������¼�̽���һ�����ǵ��ô���

* `-tokens` ��ӡtoken����
* `-tree` ��ӡLisp�����﷨��������
* `-gui` ����һ���Ի�����ӻ���ʾ�﷨��������
* `-ps file.ps` ����һ����`PostScript`��ʾ�Ŀ��ӻ��﷨����������������`file.ps`�С����µ��﷨����������ʹ��`-ps`���ɵġ�
* `-encoding encodingname` �ر�ָ��`TestRig`�������ļ��ı��루������ڱ��ػ����⣬��������Ļ��������磬�ں�����½��У�������Ҫʹ���������������һ��ʹ���ձ������XML�ļ���
* `-trace` �����롢�˳�ÿ���﷨����ʱ����ӡ�﷨��������ƺ͵�ǰtoken��
* `-diagnostics` �򿪽���ʱ�������Ϣ�����������һЩ�ض�����µ������Ϣ�����磬������ı����ж����ԡ�
* `-SLL` ʹ�ø��쵫��΢������һЩ�Ľ������ԡ�

****



�������ڣ������Ѿ���װ����antlr������������һ���򵥵��﷨�������Է�â�������ǻع�ͷ����Ϥһ��antlr������ʹ�����̣�����һ�£����ǽ���ѧϰһЩ��Ҫ��`����`���������ǽ��᳢��һ��������Ŀ����������ʶ���ҷ����������顣����֮�����ǽ����ڵ�����ͨ��һϵ����Ȥ��������֤��antlr��ǿ���Լ��������õ�����


