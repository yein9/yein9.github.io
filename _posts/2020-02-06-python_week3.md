---

title:  "[도서]혼자공부하는 파이썬 Week3"
excerpt: "."

categories:
  - Python
tags:
  - Python
  - 혼공파
  
---
## 기본 미션

### 리스트

리스트는 여러가지 자료를 저장할 수 있는 자료다.  `[]`안에 `element`를 넣어 만들 수 있다. 한 리스트 내의 element의 자료형을 모두 동일해도 되고 달라도 된다. 

```python
[123,"안녕",0.345]
```

리스트의 인덱스는 0~리스트의 길이-1이고 문자열과 동일한 방법으로 슬라이싱이 된다.

##### 특이한 사용법

1. 대괄호 안에 음수를 넣어 뒤에서부터 요소를 선택할 수 있다.

```python
list_a=[123,32,'안녕',True]
list_a[-1]
>>True
list_a[-2]
>>'안녕'
```

​	2.리스트 접근 연산자를 다음과 같이 이중으로 사용할 수 있다.

```python
list_a=[123,32,'안녕',True]
list_a[2]
>>'안녕'
list_a[2][0]
>>'안'
```

​	3.리스트 안에 리스트를 사용할 수 있다.

```python
list_a=[[1,2,3],[4,5,6],[7,8,9]]
list_a[1]
>>[4,5,6]
list_a[1][1]
>>5
```



##### 리스트 연산자 : +, *, len()

```python
list_a=[1,2,3]
list_b=[4,5,6]

#+연결
list_a+list_b
>>[1,2,3,4,5,6]

#*반복
list_a*3
>>[1,2,3,1,2,3,1,2,3]

#len()
len(list_a)
>>3
```



##### 리스트 요소 추가 : append, insert

`list_name.append(요소)`는 리스트 맨뒤에 요소를 추가한다. `list_name.insert(위치,요소)`는 리스트 위치번째 인덱스에 요소를 추가한다.

###### 요소 추가와 +의 차이는 요소추가의 경우 리스트에 직접적인 영향을 주지만(파괴적 처리) +는 연산을 한 리스트에 어떠한 영향도 주지 않는다.(비파괴적 처리) 



##### 리스트 요소 제거 

1. 인덱스로 제거하기

`del list_name[index]`또는 `list_name.pop(index)`

​	2.값으로 제거하기

`list_name.remove(value)`

​	3.모두 제거하기

`list_name.clear()`



##### 리스트  내부 존재 여부 확인 : in/ not in

`value in/not in list_name`처럼 value가 list 에 존재하는지 Boolean 값으로 리턴해준다.



### 딕셔너리

지금까지 본 리스트가 인덱스를 기반으로 값을 저장한다면 딕셔너리는 'key'를 기반으로 값을 저장한다.

##### 딕셔너리 선언

```python
dictionary={
	"name"="yein"
	"state"="hungry"
}
```

   

##### 요소 접근

`dict_name["key_name"]`로  value에 접근할 수 있다.



##### 딕셔너리 값 추가/제거하기

추가는 `dict_name["new_key_name"]=new_value`처럼 제거는 `del dict_name["key_name"]`하면 된다.