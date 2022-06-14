

**Course overview + Shell**

shell可以帮助我们做很多事情

command line 远比button有用

power shell

bash

easy to download

个性化你的shell

`date`	show the date now

`echo` 	print back of what you input such as `echo "Hello World"` `echo Hello\ World`

how shell know what the program you key



just like **system_call**

**shell scripting** you can use shell with while loops 、for loops、conditions

computer has many function built in machine environment variable

we can use echo to cat these

`echo $PATH`	show the current path in environment

`which`	find the program such as `which python`  find the python in our computer

absolute path is the full path of the file

relative path is relative current directory

`pwd`	can find the current working directory

`cd`	can change current working directory

we run a program default in our pwd

`ls`	can show the file under pwd

`ls -a\i\g\l`	command often have many options

`ls -l`	can get more plenty file information

`-rwxr-xr-x`	在文件的开头 代表创建者 组 其他人可以访问的权限 

可以写但不能删除 可以读就可以使用echo访问其中的内容

`cd -`	不知道是啥意思 直接就返回到了工作文件目录了

`mv old_file new_file`	可以移动或者重命名文件

`cp resoure dest`	可以复制文件到指定地方

`rm (-r)`	可以用来删除文件或者dir（必须使用-r递归删除）

`man`	可以用来查看手册manual page

output stream 和 input stream一般都是键盘或者显示器

**文件重定向**	

`<file`	代表把file作为输入源

`>file`	代表把file作为输出源

`cat < hello.txt`	可以访问文件中的具体内容

`cat < hello.txt >hello2.txt`	cat可以读取内容然后写入内容

`>> file`	代表以追加的方式写入

`|`	pipe技术可以将output交付给另外一个程序作为输入 十分有用

`file tail -n1`	代表取出文件的末尾1行进行打印输出

`tail`	can return the last line 

`curl`	可以访问指定的url网站获得信息

**root** 代表super user `sudo`  can do this

`cd /sys`	可以访问计算机的系统内容 kernel

`echo data > file`	可以把data写入file中

`sudo su`	切换到root用户模式

`ctrl d`	可以从当前指定的用户模式中退出 或者 `exit`

`tee file`	可以从标准输入上读取内容 然后写入到后续指定的文件中 以及stdout

`find`	可以在linux中查找文件 `find -type f -name file_name`



# 2022 6 1 





