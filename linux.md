# linux

## 1.linux命令格式

命令 【命令选项】【参数】

{必选项} [可选项]

如  ls -a /tmp   =>    ls --all /tmp

简写用-， 全写用--

使用type来区分是内部命令还是外部命令

echo表示打印

如echo $PATH  

bin的命令所有用户可以用，sbin是特权命令，只有管理员可以使用

![image-20200621143750432](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200621143750432.png)

计算机进入时只能计算出整数，要用浮点数则需要scale=2表示小数点后两位，输入quit表示退出

## 文件管理

**文件创建：**

![image-20200622105021147](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200622105021147.png)

![image-20200622105558004](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200622105558004.png)

gedit 文件名   =>   对该文件一编辑器打开

touch -a filename

touch -d 2018-08-18 filename

touch -m filename

touch -r filename1 filename2

touch -t time filename

