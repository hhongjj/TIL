# 웹크롤링(Web Crawling)

> 조직적, 자동화된 방법으로 웹을 탐색하는 것.



![](03_WebCrawling.assets/web.jpg)

### requests

- 파이썬이 주소에 대한 요청을 보냄
- $ pip install requests 

```python
import requests

requests = requests.get('주소')        #'주소'에 요청(request)를 보내서, 정보를 받아줘(get)
requests = requests.get('주소').text   #'주소'에 요청 보내서, 정보 받아서, 글(text)만 뽑아줘
requests = requests.get('주소').status_code #'주소'에 요청 보내서, 정보 받아서, 상태(status_code)만 뽑아줘
```



### Beautifulsoup

- pip install beautifulsoup4
- 받은 문서를 검색하기 좋게 만들어줌

```python
from bs4 import BeautifulSoup

html = BeautifulSoup(response,'html.parsing')
data = html.select('selector')      # 문서 안에 있는 특정 내용을 뽑아줘(select)
data = html.select_one('selector')  # 문서 안에 있는 특정 내용을 하나만 뽑아줘(select_one)
```




