# scrapy

​    在终端输入

1. 创建工程

   ```
   scrapy startproject 工程名称
   ```

2. 进入项目当前路径并且在spider文件夹里创建一个爬虫文件

   ```
   cd 工程名称
   scrapy genspider 爬虫文件名 www.xxx.com
   ```

3. 执行工程

   ```
   scrapy crawl 爬虫文件名
   scrapy crawl 爬虫文件名 --nolog   则不显示日志及错误信息 
   ```

   

