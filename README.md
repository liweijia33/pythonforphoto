import urllib.request

#网址  
url = "http://www.douban.com/"  
  
#请求  
request = urllib.request.Request(url)  
  
#爬取结果  
response = urllib.request.urlopen(request)  
  
data = response.read()  
  
#设置解码方式  
data = data.decode('utf-8')  

#将数据写入到本地磁盘
urllib.request.urlretrieve(url,r"E:\python\file\text.html")

#打印结果  
print(data)  
  
###打印爬取网页的各类信息  

#打印类
#print(type(response))

#打印网址
#print(response.geturl())  

#unknown
#print(response.info())

#打印大小
print(response.getcode())
