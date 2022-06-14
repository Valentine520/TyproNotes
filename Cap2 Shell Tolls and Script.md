# Cap2 Shell Tools and Script

`foo=bar`	可以对shell进行变量赋值必须是连在一起的 不可以分开

`$foo`	可以使用$访问变量的值 还可以在string中进行format string

`this is $foo`	利用foo的值创建格式化字符串

`"Hello"`  or `Hello`	双引号和单引号都可以表示字符串string

Write script into a file can simplify our 

`$1 $2`	在shell中代表跟在命令后的第一个和第二个输出

`$? $_`	在shell中可以直接使用 $_特指最后输入的内容 $?返回最后一个command结束后的状态

`echo $?`	可以获得上一条程序执行的状态

`false || echo xxx`	

`true && echo xxx`

`true ; xx`	

上述均是进行条件判断

`cat <(ls) <(ls ..)`	看似复杂 其实仅仅只是进行输入文件重定向而已

`$#`	可以用来获取跟随输入的参数的个数

`$$`	代表pid

`$@`	代表从$1到$n `for file in "$@"`

`2>`	代表重定向stderr

`>`	代表重定向stdout

`grep str file`	find the str in file

如果没有找到str的内容 就会报错

可以用 $? 进行查看上条语句执行的状态

`convert`	可以进行图像的转化



### !!!shell script在编写过程中要注意单词的seperate

#### 如果./example.sh权限不够 使用 `chmod -x example.sh`

### regx

1. script 支持regular expression
2. `example?`	必须有后缀
3. `example*`	可以没有后缀 example
4. `touch {foo,bar}/{a..j}`	表示创建foo和bar目录下的a-j文件
5. `diff (-op) file1 file2`	一行一行检查file1和file2之间的差别





**shellcheck**	可以用来静态分析.sh文件

**tldr**	可以比man更好地查看使用手册

`find`	可以用来更好地查找文件 可以用多种匹配模式	-name -path 

-size +500k -10M 表示查找的文件大小在500k到10M之间

支持多重操作 查找到之后还可以删除 -exec rm

`grep`	在所有文件中进行检查和匹配

`rg`	alias of ripgrep 可以用正则表达式在所指定的文件中进行匹配

`ack`	同样是一种查找文件内容的tool 对标find

`history`	可以用来访问指令日志

`history | grep xx`	可以用grep来执行表达式匹配

`fzf`	和管道出来的stdout使用 提供交互性更强的搜索

`cat example.sh | fzf`	更方便地定位变量位置

`history | fzf`	在历史记录中定位内容

`ls -R`	recursive list all file under all directory

`tree`	可以生成一个更容易理解的目录树

`broot`	更厉害的文件目录管理器 但不知道怎么下载安装

`cd`	虽然很强 但是跳转到最近访问的文件可以有更多快捷的方法
