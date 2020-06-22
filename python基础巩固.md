# **python基础巩固**

1.字符串

``` 
s = 'py study'
lst = ['i', 'love', 'you']
s.center(2,'-')    =>     --py study--
s.count('y',0,7)  => 1
s.startswith('py')/s.endswith('dy')   => True
s.find('y')  => 1       如果未找到返回-1,若找到返回第一次出现的下标
'43'.isdigit() => True
' '.join(lst)  => i love you   元组也可以，如果是字典则是得到键的字符串
s.replace(' ', 'h') => pyhstudy 返回的是一个新的字符串, 可以传入次数，当次数为-1，表示全部
s.split() =>默认空格， 可以传入需要分割的’字符'
```

2.列表

```
lst = ['apple', 'pear']
lst1 = ['tiger', 'lion']
添加元素：lst.append('banana')
插入元素：lst.insert(2, 'peach')  =>在第二个元素之前插入
合并列表: lst.extend(lst1)

删除元素：del lst[1]
		lst.pop()  =>返回删除的最后一个元素
		lst.remove('banana') => 删除第一个出现的元素
		
清空列表：lst.clear()

查找：lst.index('pear') => 返回第一个出现下标
元素个数：lst.count('pear')
切片设置步长：lst[::2]
列表排序：lst.sort()
索引和对应的值：
for i in enumerate(lst):
	print(i)
	
```

内置函数拓展

``` 
abs(arg)  #绝对值
all(arg)  #arg为iter，若元素中有0，则返回False
any(arg)  #若元素中有非0，则返回True
chr(arg)  #arg对应的ascii字符
dir() #当前程序下的变量名
locals()  #当前程序的变量名和变量值
map(func, iter)  #func只能带一个参数，返回一个迭代对象，只有在循环中才执行
ord('a')   #返回ascii码
round(num, 2) #保留两位小数
zip(iter1, iter2) #拉链，把两个iter的对应元素合并
filter(func, iter)  #把iter中符合func的元素筛选出来


```

装饰器

装饰器就像是给房子装修

装饰器遵循开放封闭原则（在不改变原有代码及其调用方式的前提下，添加新的功能）

装饰器的应用：登录认证

```python
def decorate(f):
	def inner(*args, **kwargs):
        # 添加函数调用前的新功能
        r = f(*args, **kwargs)
        # 添加函数调用后的新功能
        # return r 根据情况而定
     return inner
```

例如：

```python
import time


def timmer(f):
    def inner():
        start_time = time.time()
        f()
        end_time = time.time()
        print(f'测试的结果为{end_time-start_time} seconds')
    return inner

@timmer       # 相当于login1 = timmer(login1)
def login1():
    '''.............'''
    time.sleep(2)
    print('login1 finished')


def login2():
    time.sleep(2)
    print('login2 finished')

# login1 = timmer(login1)
login1()
```

