---
title: 파이썬 조건문/반복문 배우기 (1)
author: move78s
date: 2024-03-19 09:09:09 +0900
categories: [python, expressions]
tags: [python, 조건문, 반복문, conditional, loop, Pythonic]
---

# 조건문의 파이써닉한 사용

조건문은 프로그래밍에서 매우 중요한 역할을 합니다. 파이썬에서는 조건문을 더 간결하고 읽기 쉽게 만들 수 있는 몇 가지 방법이 있습니다. 이러한 방법을 파이써닉하게 조건문을 사용하는 것이라고 합니다.

## Truthy와 Falsy 값 이해하기

파이썬에서는 `None`, `0`, `""`, `[]`, `{}`, `()` 등은 Falsy 값으로 간주됩니다. 따라서 다음과 같은 조건문은 파이써닉하게 간소화할 수 있습니다.

```python
# Not Pythonic
if len(my_list) > 0:
    print("The list is not empty!")

# Pythonic
if my_list:
    print("The list is not empty!")
```

## 조건문 간소화

복잡한 조건문은 가독성을 떨어뜨릴 수 있습니다. 파이썬에서는 이를 간소화할 방법을 제공합니다.

```python
# Not Pythonic
if x >= 10 and x < 20:
    print("x is between 10 and 20")

# Pythonic
if 10 <= x < 20:
    print("x is between 10 and 20")
```

## 조건부 표현식 (Conditional Expressions)

파이썬에서는 삼항 연산자를 사용하여 간결한 조건부 표현식을 작성할 수 있습니다. 이 방식은 간단한 조건에 기반한 값을 할당할 때 유용합니다.

```python
# Not Pythonic
if age >= 18:
    status = 'adult'
else:
    status = 'minor'

# Pythonic
status = 'adult' if age >= 18 else 'minor'
```

## 파일의 존재 여부 확인

파일이 존재하는지 여부에 따라 다른 작업을 수행하려면 다음과 같이 작성할 수 있습니다.

```python
import os

filename = 'example.txt'
if os.path.exists(filename):
    print(f"{filename} exists")
else:
    print(f"{filename} does not exist")

```

## 여러 조건 동시 체크

여러 조건을 동시에 체크해야 할 경우, all() 또는 any() 함수를 사용하여 코드를 간결하게 만들 수 있습니다.

```python
conditions = [True, True, False]

if all(conditions):
    print("All conditions are True")
elif any(conditions):
    print("At least one condition is True")
else:
    print("No conditions are True")
```

이러한 예제들은 파이썬에서 조건문을 더 파이써닉하게 작성하는 방법을 보여줍니다. 코드를 간결하게 만들 뿐만 아니라, 읽기도 더 쉬워집니다.
