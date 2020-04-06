---
layout: post
title: "An Introduction to Python & Algorithms 01"
date: 2020-04-07 00:19:10 +0900
categories: [Python]
---

# An Introduction to Python & Algorithms 01
## 개요
* Python을 공부하고 싶다.
* LeetCode와 같은 알고리즘 문제 풀이도 하고 싶다.
* 이 두개를 동시에 진행하기에 딱 좋은 책이 있어서 공부해보려고 한다.
    * [An Introduction to Python & Algorithms](https://github.com/bt3gl/Book_on_Python_Algorithms_and_Data_Structure)
* 이 방식이 완벽하게 Python 문법을 익히기는 어려울 수 있지만 시작을 이렇게 하고 중간에 막히는 부분을 공부해도 될듯하다.
* 실행은 로컬에서 Python 코드를 실행해도 되고 온라인으로 해도 된다.
    * [geeksforgeeks](https://ide.geeksforgeeks.org/)

## Numbers
* Number는 integer, float, complex로 표현될 수 있다.
* 또한 10진수, 2진수, 8진수, 16진수등으로 표현할 수 있다.

## Integers
* Python에서 integer는 immutable int 타입을 사용한다.
    * 참고로 immutable objects의 경우에 변수와 오브젝트 레퍼런스간의 차이가 없다.

* integer의 크기는 내장된 컴파일러에 의존되는 머신의 메모리에 의해서 제한되며 최소한 32비트이다.

```python
(999).bit_length()

10
```

* string을 integer로 casting하려면 int(s, base)를 이용하면 된다.

```python
s = '11'
d = int(s)
print(d)

11

b = int(s, 2)
print(b)

3
```