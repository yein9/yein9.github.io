---
title:  "[Programmers] level1 문자열 내림차순으로 배치하기"
excerpt: "."

categories:
  - Algorithm
tags:
  - Programmers
  - Algorithm
  - Python
---
[프로그래머스  level1 문자열 내림차순으로 배치하기](https://programmers.co.kr/learn/courses/30/lessons/12917)

#### 문제

------

문자열 s에 나타나는 문자를 큰것부터 작은 순으로 정렬해 새로운 문자열을 리턴하는 함수, solution을 완성해주세요. s는 영문 대소문자로만 구성되어 있으며, 대문자는 소문자보다 작은 것으로 간주합니다.

##### 제한 사항

- str은 길이 1 이상인 문자열입니다.

#### 풀이

------

list(s)로 문자 s를 알파벳으로 쪼개 answer에 list형태로 넣는다. 이 리스트를 sort함수로 내림차순으로 정렬하고 알파벳 원소들을 join함수를 사용해 문자로 합쳐준다.  

#### 코드

```python
def solution(s):
    answer = list(s)
    answer.sort(reverse=True)
    answer="".join(answer)
    return answer
```


