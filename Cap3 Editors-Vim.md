# Cap3 Editors-Vim

`vim`	is a very good editor in system

写代码和写文章不一样

use one editor well

vscode 在图形编辑最佳

vim在命令行编辑最佳

vim is a model editor it has many kind of modes

writing changing reading 多种使用场景 vim都可以有相应的模式

1. normal mode `esc`

2. insert mode `i`

3. replace mode `r`

4. selection visual line `shift v`  可以选中一行 比较方便 即 `V`
5. selection visual block `ctrl v`

`:help :w`	可以用来查看帮助文档 帮助:w的使用 而不是直接 `:help w`

`:sp`	可以分隔出两个相同的屏幕

`:qa`	可以关闭所有分隔出的窗口

vim 的normal mode就像一个program language interface所以用好normal mode会更强

### vim normal mode

1. `e` 前进到单词末尾
2. `b`后退到上一单词末尾
3. `ctrl f` 前进一页
4. `ctrl b` 后退一页
5. 0 到行首
6. $ 到行尾
7. a 可以开启追加模式 在e移动到单词末尾的时候使用a
8. `ctrl d` 可以前进半页
9. `ctrl u` 可以后退半页
10. `ctrl f` 可以前进一页
11. `ctrl b` 可以后退一页
12. `gg` 到文件末尾
13. `G` 可以到文件头
14. `L` 到页面的末尾
15. `M` 到页面的中央
16. `H` 到页面的首部
17. `f o(char)` 可以在行中查找后续char 然后定位到该处
18. `F x` 则可以反向查找指定的char
19. `t char` 可以jump to到指定的字符
20. `T char` 同样是反向查找
21. `d` 用于删除 `dw` 删除一个word  `de`相似 `dd` 删除一行
22. `cc` 删除一行内容然后可以进行key in
23. `x` 可以用来删除内容 normal mode下的del
24. `u` 用来撤销操作 undo
25. `ctrl R` 用来redo

26. `y` 代表copy `p` 代表paste

    这两个键和d相似 都可以和其他键进行组合 如 `yw` 代表copy一个单词

27. `v` 进入visual mode 可以进行select 然后y 或者 p

28. `cw`  删除且进入insert mode `dw` 不切换状态删除

#### normal mode 就是一种编程语言 `4j` 代表向下移动4行

操作可以带上数字 避免重复操作

`3 ctrl b`

还可以带上修饰符

`.`	 可以在不同的位置执行上一次相同的操作 批量修改时很有用

#### tmux 很有用 一边vim 一边run

### TMUX

1. 上下分屏：ctrl + b  再按 " （要加shift）
2.  左右分屏：ctrl + b  再按 % 
3. 切换屏幕：ctrl + b  再按o 
4. 关闭一个终端：ctrl + b  再按x 
5. 上下分屏与左右分屏切换： ctrl + b  再按空格键

`~/.vimrc` 提供了许多vim配置 而且可以加入许多vim的插件 使vim更牛逼

`~/.bashrc` 可以修改命令行配置 `set -o vi` 可以设置默认的编辑工具为vim

`fish bash zsh`	都是一系列好用的shell



### 在editor上花时间去学习会大有裨益

## END 2022 6 2

