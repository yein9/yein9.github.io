---

title:  "[도서]혼자공부하는 파이썬 Week6"
excerpt: "."

categories:
  - Python
tags:
  - Python
  - 혼공파
  
---
## 기본 미션

#### Flask, BeautifulSoup으로 스크레이핑 하기

~~~python
from flask import Flask
from urllib import request
from bs4 import BeautifulSoup

app=Flask(__name__)
@app.route('/')

def hello():
  tartget=request.urlopen('http://www.kma.go.kr/weather/forecast/mid-term-rss3.jsp?stnId=108')

  soup=BeautifulSoup(target,'html.parser')

  output=""
  for location in soup.select('location'):
    output+="<h3>{}</h3>".format(location.select_one("city").string)
    output+="날씨: {}</br>".format(location.select_one('wf').string)
    output+='최저/최고 기온: {}/{}'.format(loction.select_one('tmn').string,location.select_one('tmx').string)
    output+='<hr/>'

  return output
~~~

cmd 창에서 `set FLASK_APP=app.py` , `flask run`으로 실행하려 했으나 `AttributeError: 'NoneType' object has no attribute 'SSLContext'` 에러가 뜬다. 아마 아나콘다 가상환경과 충돌해서 발생하는것 같다. 얼른 해결 방법을 찾아서 수정해야겠다.