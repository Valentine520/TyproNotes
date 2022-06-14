`wc -w/l/c`	可以统计对应文件的长度 如果没有文件的话就默认来自stdout

`sort --reverse`	sort等可以对文件或者标准输出排序

`-n` 可以比较number值 `-k` 可以指定排序的key值 

### uniq	

- default对重复内容仅输出一行
-  **-u** 只输出独一无二的内容 
-  **-d** 只输出重复内容 
-  **-c** 统计重复出现的内容

可以从logfile wragling出许多有效内容

`awk '{print $2}'`  指定行进行输出

`paste -sd,`	将多个输出行利用 ，进行分隔 整合为一行

awk可以做的事情很多 可以匹配确定的内容 然后指定其进行输出

### bc Berkeley Calculator

可以用来对文件进行计算

`bc -l`	include math library

如果输出的数据很多 都散布在各个行 可以使用paste -sd+ 来拼合在一起 传递给bc进行累加

R 语言也可以用在命令行中处理相应的输出 进行benchmark

gnuplot 可以在命令行中启动画图程序 command line can do everything you need

command argument wrangling

### xargs

可以将输出转化为后续内容的参数

`-r | xargs ls`	等价于 **ls -r**

#### ffmpeg

可以转化格式 转为binary 

同样可以进行操作 只需要|到另外的程序即可

pipeline 十分强大 视频提取然后转到图像处理 访问history然后进行grep sed等正则处理 然后再sort

将杂乱的数据提取出你想要的格式







