这里用的是python的Scrapy框架，pip安装这个框架。                        
首先命令行输入 scrapy startproject 'project_name' 生成项目。                  
然后编辑items.py文件，定义抓取的数据字段名。                  
cd进入spiders文件夹下，输入scrapy  genspider  'spider_name'  "start_url"，就会得到一个编写爬虫逻辑的文件“文件名.py”。         
然后到pipelines.py文件中编写保存数据的逻辑。              
为了是最后得到的json文件不乱码，在seeting.py文件中加入FEED_EXPORT_ENCODING = 'utf-8'。          
最后输入scrapy crawl  "spider_name"运行，输入Scrapy crawl  "spider_name" -o "spider_name".json保存为json文件，爬取得结果保存在Json文件夹中。
