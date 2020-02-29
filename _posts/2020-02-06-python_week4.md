---

title:  "[도서]혼자공부하는 파이썬 Week4"
excerpt: "."

categories:
  - Python
tags:
  - Python
  - 혼공파
  
---
## 기본 미션

~~~python
def sum_all(start,end):
    output=0
    for i in range(start,end+1):
        output+=i
    
    return output
	

print("0 to 100: ",sum_all(0,100))
print("0 to 1000: ",sum_all(0,1000))
print("50 to 100: ",sum_all(50,100))
print("500 to 1000: ",sum_all(500,1000))
~~~

![pythonw4](\assets\images\python_w4_1.PNG)