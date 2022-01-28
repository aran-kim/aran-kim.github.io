---
title: "Python Summary"
date: 2022-01-28
categories:
  - algorithm
tags:
  - algorithm
  - summary
  - python
toc: ture
toc_sticky: true
toc_label: "Table of Contents"
sidebar:
  nav: "categories"
---

# 파이썬 문법 정리

## 자료형
1. 수 자료형

- 정수형
- 실수형
  - 지수표현 : 유효숫자e지수 = 유효숫자 * 10^지수
  - 반올림 표현 : round()
<br><br>
- 수 자료형의 연산
  - 연산
    ```python
    print(a/b) # 나누기
    print(a%b) # 나머지
    print(a//b) # 몫
    print(a**b) # 거듭제곱
    ```

2. 리스트 자료형
- 여러 개의 데이터를 연속으로 담아 처리하기 위해 사용
- 배열의 기능 포함
- 연결리스트의 자료구조 : append(), remove() 메서드 지원
- 리스트 선언
  ```python
  a = list() # 리스트 선언 1
  a = [] #리스트 선언 2
  a = [1,2,3,4]
  ```
- 리스트 컴프리헨션
  - 리스트를 초기화 하는 방법
  - 대괄호 안에 조건문과 반복문을 넣는 방식
    ```python
    # N X M 크기의 2차원 리스트 초기화
    n = 3
    m = 4
    array = [[0] * m for _ in range(n)]
    print(array) #[[0,0,0,0],[0,0,0,0],[0,0,0,0]]
    ```
- 리스트 관련 메서드
  ```python
  a = list()
  a.append() #원소 삽입 : O(1)
  a.sort() #오름차순으로 정렬 : O(NlogN)
  a.sort(reverse=True) #내림차순으로 정렬 : O(NlogN)
  a.reverse # 리스트의 순서를 뒤집음 : O(N)
  a.insert(삽입할 위치 인덱스, 삽입할 값) #O(N)
  a.count(특정 값) #특정값 개수 셈 : O(N)
  a.remove(특정 값) #특정값 제거, 여러개면 하나만 제거 : O(N)
  ```
3. 문자열 자료형
- 문자열 안에 따옴표
  ```python
  name = "\`kim a ran\`" # 백슬래시를 사용하여 작성
  ```
- 문자열 연산
  - 내부적으로 리스트와 같이 처리
  ```python
  a = "Hello"
  b = "world"
  print(a + " " +b) # Hello world
  ```
4. 튜플 자료형
   - 한번 선언된 값을 변경할 수 없음
   - 소괄호 ()를 이용
   - 그래프 알고리즘을 구현할 때 자주 사용
5. 딕셔너리 자료형
   - key, value의 쌍을 데이터로 가지는 자료형
   - hash table을 이용하므로 데이터의 검색 및 수정을 O(1)에 처리
  ```python
  data = dict()
  data['이름'] = '김아란'

  # 키 데이터만 담은 리스트
  key_list = data.keys()
  # 값 데이터만 담은 리스트
  value_list = data.values()
  ```
6. 집합 자료형
- 중복을 허용하지 않음
- 순서가 없음
- 검색 : O(1)
```python
# 집합 초기화
data = set([1,1,2,3,4,5]) 
data = {1,1,2,3,4,5} # {1,2,3,4,5}

data.add(특정값) # 새로운 원소 추가
data.update([값1,값2]) # 여러개의 원소 추가
data.remove(특정값) # 값 삭제
```

## 조건문
- if문
  - if ~ elif ~ else 문
  ```python
  if 조건문 1 :
    ~
  elif 조건문 2 :
    ~
  else:
    ~
  ```
  - 아무것도 처리하고 싶지 않으면 pass문 사용
- in/not in 연산자
  - 리스트, 튜플, 문자열, 딕셔너리 자료형에 존재

## 반복문
- while문
  ```python
  while 조건문:
    ~
  ```
- for문
  ```python
  for i in range(5):
    ~
  ```

## 함수
```python
def 함수명(매개변수):
  실행할 소스코드
  return 반환 값
```

## 입출력
- 문자열 -> 정수로 입력
  ```python
  # 각 데이터를 공백으로 구분하여 입력
  data = list(map(int,input().split())) 
  ```
- 빠르게 입력 받는 법
  - 입력의 개수가 많을 때
  ```python
  import sys
  sys.stdin.readline().rstrip()
  ```
