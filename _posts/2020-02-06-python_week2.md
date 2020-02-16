---

title:  "혼공파 Week2"
excerpt: "."

categories:
  - Python
tags:
  - Python
  - 혼공파
  
---
## 기본 미션

#### 3. 사용자에게 태어난 연도를 입력받아 띠를 출력하는 프로그램을 작성해주세요. 

![pythonw2_1](\assets\images\python_w2_2.JPG)

![pythonw2_2](\assets\images\python_w2_1.PNG)

```python
str_input=input("태어난 해를 입력하세요")
birth_year=int(str_input)%12

if birth_year==0:
    print("원숭이 띠입니다.")
elif birth_year==1:
    print("닭 띠입니다.")
elif birth_year==2:
    print("개 띠입니다.")
elif birth_year==3:
    print("돼지 띠입니다.")
elif birth_year==4:
    print("쥐 띠입니다.")
elif birth_year==5:
    print("소 띠입니다.")
elif birth_year==6:
    print("범 띠입니다.")
elif birth_year==7:
    print("토끼 띠입니다.")
elif birth_year==8:
    print("용 띠입니다.")
elif birth_year==9:
    print("뱀 띠입니다.")
elif birth_year==10:
    print("말 띠입니다.")
elif birth_year==11:
    print("양 띠입니다.")

```

if, elif문을 사용하지 않고 문자열을 담은 배열을 생성한 뒤 인덱스를 사용해 간단하게 풀 수도 있다.

```python
str_input=input("태어난 해를 입력하세요")
birth_year=int(str_input)%12

animals=['원숭이','닭','개','돼지','쥐','소','범','토끼','용','뱀','말','양']

print(animals[birth_year],"띠입니다.")
```

