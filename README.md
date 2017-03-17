import urllib.request
url = "http://www.douban.com/"  
request = urllib.request.Request(url)  
response = urllib.request.urlopen(request)  
data = response.read()   
data = data.decode('utf-8')  
urllib.request.urlretrieve(url,r"E:\python\file\text.html") 
print(data) 
print(response.getcode())
