---
layout: post
title: 프로그래머스 내적 (python 파이썬)
subtitle: 프로그래머스 내적
comments: true
categories: [Algorithm]
tags: [Algorithm]
sitemap :
changefreq : daily
priority : 1.0
---
프로그래머스 내적 문제를 Python으로 해결한 문제이다.  

* [프로그래머스 내적 문제 링크](https://programmers.co.kr/learn/courses/30/lessons/70128){:target="_blank"}

### 문제 
길이가 같은 두 1차원 정수 배열 a, b가 매개변수로 주어집니다. a와 b의 내적을 return 하도록 solution 함수를 완성해주세요.

이때, a와 b의 내적은 ```a[0]*b[0] + a[1]*b[1] + ... + a[n-1]*b[n-1]``` 입니다. (n은 a, b의 길이)

### 제한사항
* a, b의 길이는 1 이상 1,000 이하입니다.
* a, b의 모든 수는 -1,000 이상 1,000 이하입니다.

### 입출력 예

|a|b|result|
|-----|-----|-----|
|[1,2,3,4]|[-3,-1,0,2]|3|
|[-1,0,1]|[1,0,-1]|-2|

### 입출력 예 설명
**예제 #1**  
a와 b의 내적은 ```1*(-3) + 2*(-1) + 3*0 + 4*2 = 3``` 입니다.

**예제 #2**  
a와 b의 내적은 ```(-1)*1 + 0*0 + 1*(-1) = -2``` 입니다.

### 문제풀이
* 파이썬의 zip 함수를 이용하여 두 배열의 값을 곱한 후 더해주면 된다.


### 코드
```python
def solution(a,b):
    answer = 0

    for num1,num2 in zip(a,b):
        answer += num1 * num2
        
    return answer
```