---
title:  "[Programmers] level1 문자열 내 마음대로 정렬하기"
excerpt: "."

categories:
  - Algorithm
tags:
  - Programmers
  - Algorithm
  - Python
---
[프로그래머스  level1 문자열 내 마음대로 정렬하기](https://programmers.co.kr/learn/courses/30/lessons/12915?language=python3)

#### 문제

------

문자열로 구성된 리스트 strings와, 정수 n이 주어졌을 때, 각 문자열의 인덱스 n번째 글자를 기준으로 오름차순 정렬하려 합니다. 예를 들어 strings가 [sun, bed, car]이고 n이 1이면 각 단어의 인덱스 1의 문자 u, e, a로 strings를 정렬합니다.

##### 제한 조건

- strings는 길이 1 이상, 50이하인 배열입니다.
- strings의 원소는 소문자 알파벳으로 이루어져 있습니다.
- strings의 원소는 길이 1 이상, 100이하인 문자열입니다.
- 모든 strings의 원소의 길이는 n보다 큽니다.
- 인덱스 1의 문자가 같은 문자열이 여럿 일 경우, 사전순으로 앞선 문자열이 앞쪽에 위치합니다.



#### 풀이

------

풀이가 너무 간단해 설명할 것이 없다. 파이썬 sorted함수의 lamda를 사용해 우선적으로 n번째 인덱스를 기준으로 정렬하고 string 자체로 비교해 정렬하도록 했다. 



#### 코드

```python
def solution(strings, n):
    answer = []
    answer=sorted(strings, key=lambda string:(string[n],string) )
    return answer
```



##### 참고

[하나씩 점을 찍어 나가며 ](https://dailyheumsi.tistory.com/67)