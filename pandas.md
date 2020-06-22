# pandas

**Series**

数组|字典

创建：sr = pd.Series([arg1, arg2], index = [arg3, arg4])

整数索引：loc（按照标签索引）  iloc（按照下标索引） sr.loc(arg)

数据对齐：sr1+sr2 会按照对应的标签进行索引，但标签不同时会出现Nan

缺失数据（Nan）dropna（舍弃该行）   fillna（填充）

**DataFrame**

```
#创建
pd.DataFrame({'one':[1, 2, 3], 'two': [4, 5, 6]})       
#同样可以加index = [...]
```

   one  two
0    1    4
1    2    5
2    3    6

```
#采用Series进行数据对齐
pd.DataFrame({'one':pd.Series([1, 2, 3], index = ['a','b','c']), 'two': pd.Series([4, 5, 6, 7], index = ['a','b','c','d'])})
```

   one  two
a  1.0    4
b  2.0    5
c  3.0    6
d  NaN    7

``` 
#获取索引  index
#转置  T
#获取列索引   columns
#获取值数组  values
#统计描述   describe()
```

```
#df在索引时先列后行
df['one']['a']
#推荐：df.loc['a','one']   通过标签索引
```

```
#数据缺失   dropna()\fillna()
dropna() 删除有缺失值所在行
dropna(how='all')  删除改行是的所有数据都是缺失
dropna(axis=1，where='any')  0表示行，1表示列
```

```
#常用函数
平均值：mean()  对每一列进行求平均
对行：mean(axis=1)
求和：sum(axis=?)
排序：sort_values(by='one', ascending=True|False)
	 sort_index(ascending=..)
	 
```

```
#python时间模块datetime
datetime.datetime.strptime('2020-05-19','%Y-%m-%d')

#pandas 使用模块dateutil   其中支持'19-JAN-2020'，'2020/05/19'..
dateutil.parser.parse('2020-05-19')

#pandas将字符串转化为事件索引对象
pd.to_datetime(['2019-FEB-03','2020/05/19'])
=>DatetimeIndex(['2019-02-03', '2020-05-19'], dtype='datetime64[ns]', freq=None)

#批量生产时间对象
1.范围：pd.date_range('2020-01-01','2020-05-19')   可以添加参数periods=arg, 表示长度
freq = 'H'表示每小时生成一个，'W-SUN|W-MON..','B'(工作日)，'SM'(半月)，’T'(分)，‘1h20min'...
可以使用to_pydatetime()生成datetime对象  

#时间索引
pd.resample()采样
```

```
#文件读取
1.csv
pd.read_csv(filename, index_col = '...', parse_dates = True|False|['date'], header=None，name=[...])  (index_col表示已哪一列进行索引; parse_dates表示将文件中可以转化为时间对象的字符串转化为时间对象,header表示自动添加列名,name表示自己定义列名，seq表示指定分隔符，可以用正则表示)
read_table（分隔符为制表符）  read_csv（逗号）
```

![image-20200519110945709](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20200519110945709.png)