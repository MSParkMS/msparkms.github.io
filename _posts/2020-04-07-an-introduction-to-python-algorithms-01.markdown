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
    * base값은 2~36까지 가능하다.

```python
s = '11'
d = int(s)
print(d)

11

b = int(s, 2)
print(b)

3
```

## Floats
* 분수타입의 숫자는 immutable float 타입으로 표현된다.
* 32-bits 실수는 1bit는 부호, 23bits는 가수부, 8bits는 지수부이다.
    * 지수부는 127을 더해줘야 원래의 값을 얻을 수 있다.

### 실수 비교
* 실수는 정확도의 한계를 가진다.
* 실수값이 잘릴 수 있다.
* 그렇기 때문에 같은지 비교하려면 특정 정밀도를 정해서 비교해야만 한다.

```python
def a(x, y, places = 7):
    return round(abs(x-y), places) == 0
```

### 정수, 실수 메소드
* / 연산자는 항상 Floats를 리턴한다.
* floor(버림)은 // 연산자로 계산할 수 있다.
    * round(반올림)은 소수점 아래 places 위치에서 반올림한다.
* 나머지는 % 연산자로 계산할 수 있다.
* divmod()는 몫과 나머지를 한번에 계산할 수 있다.

```python
divmod(45, 6)

(7, 3)
```

* as_integer_ratio()는 정수로 분수를 표현해준다.

```python
2.75.as_integer_ratio()

(11, 4)
```

## Complex Number
* 복소수타입은 immutable float의 pair값을 가진다.
    * 실수부, 가수부, 켤레를 구할 수 있다.
* 복소수타입은 cmath 모듈에서 임포트된다.
    * 삼각함수나 로그함수의 복소수 버전이 제공된다.
    * 복소수용 함수도 존재한다.
        * cmath.phase()
        * cmath.polar()
        * cmath.rect()
        * cmath.pi
        * cmath.e
    * 자세한 내용은 아래 링크 참고
        * [cmath](https://docs.python.org/ko/3.9/library/cmath.html)

## ETC
* Faction은 분수를 다룬다.
* Decimal은 10진법 부동소수점을 다룬다.
    * floats에서 있던 문제들을 효과적으로 다룬다.
    * math, cmath와 적합하지는 않고 Decimal에 있는 함수를 이용해야한다.
* bin(), hex(), oct()으로 진법을 변환할 수 있다.
* random 모듈을 이용하면 난수를 생성할 수 있다.
* NumPy 패키지 크거나 다차원 배열이나 행렬을 처리할 수 있다.
    * NumPy의 array가 기본 lists보다 효율적이라고 한다.