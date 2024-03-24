---
title: 파이썬 조건문/반복문 배우기 (2)
author: move78s
date: 2024-03-20 09:09:09 +0900
categories: [python, expressions]
tags: [python, 조건문, 반복문, conditional, loop, Pythonic]
---

# for 반복문의 파이써닉한 사용

파이썬의 `for` 반복문은 다양한 시퀀스(리스트, 튜플, 문자열 등)를 순회하며, 각 요소에 대해 블록을 실행할 때 사용됩니다. 하지만 파이썬에서는 `for` 반복문을 더 파이써닉하게 사용할 수 있는 몇 가지 방법이 있습니다. 이 방법들을 활용하면 코드의 가독성과 효율성을 높일 수 있습니다.

## 1. 리스트 컴프리헨션 사용하기

리스트 컴프리헨션은 `for` 반복문을 사용하여 새 리스트를 만드는 간결하고 효율적인 방법입니다. 조건문을 함께 사용할 수도 있어 코드를 더욱 짧게 만들 수 있습니다.

```python
squares = [x**2 for x in range(10)]
```

위 코드는 0부터 9까지의 숫자에 대한 제곱값을 리스트로 만듭니다.

## 2. enumerate 사용하기

`enumerate` 함수는 리스트의 요소를 순회할 때 인덱스도 함께 필요한 경우 유용합니다. 이는 튜플 형태로 인덱스와 요소를 제공합니다.

```python
fruits = ['apple', 'banana', 'cherry']
for index, fruit in enumerate(fruits):
    print(f'{index}: {fruit}')
```

위 코드는 각 과일과 그에 해당하는 인덱스를 출력합니다.

## 3. zip 함수 사용하기

`zip` 함수를 사용하면 여러 리스트를 동시에 순회할 수 있습니다. 이는 병렬적인 데이터 구조를 만들 때 특히 유용합니다.

```python
names = ['Alice', 'Bob', 'Charlie']
ages = [24, 50, 18]
for name, age in zip(names, ages):
    print(f'{name} is {age} years old')
```

위 코드는 각 이름과 나이를 함께 출력합니다.

## 4. 딕셔너리 순회하기

딕셔너리를 순회할 때는 `.items()` 메서드를 사용해 키와 값을 함께 얻을 수 있습니다.

```python
person_info = {'name': 'Alice', 'age': 30, 'city': 'New York'}
for key, value in person_info.items():
    print(f'{key}: {value}')
```

이 코드는 딕셔너리의 각 항목에 대한 키와 값을 출력합니다.

## 결론

파이썬에서 `for` 반복문을 사용하는 방법은 다양합니다. 파이써닉한 접근 방식을 사용하면 코드를 더 간결하고 읽기 쉽게 만들 수 있습니다. 리스트 컴프리헨션, `enumerate`, `zip`, 그리고 딕셔너리의 `.items()` 메서드를 활용하여 보다 효율적인 코드를 작성해 보세요.

## 추가 예제: 필터링과 정렬

`for` 반복문을 사용하여 복잡한 데이터 구조에서 필터링, 정렬 등의 작업을 수행할 수도 있습니다. 파이써닉한 방법을 사용하여 이러한 작업을 보다 효율적으로 수행해 보겠습니다.

### 데이터 필터링하기

주어진 데이터에서 특정 조건을 만족하는 요소만 선택하고 싶을 때, 리스트 컴프리헨션과 `for` 반복문을 사용할 수 있습니다.

```python
data = [19, -3, 15, 36, -21, 7]
filtered_data = [num for num in data if num > 0]
print(filtered_data)
```

위 예제는 리스트에서 양수만을 선택하여 새 리스트를 만듭니다.

### 데이터 정렬하기

데이터를 특정 기준에 따라 정렬하려면, 리스트의 `sort()` 메소드를 사용할 수 있습니다. 더 파이써닉한 방법은 `sorted()` 함수와 함께 `for` 반복문을 사용하는 것입니다.

```python
names = ['Charlie', 'Alice', 'Bob']
for name in sorted(names):
    print(name)
```

이 예제는 이름을 알파벳 순으로 정렬하여 출력합니다.

### 중첩 반복문

리스트 컴프리헨션은 중첩 반복문도 지원합니다. 이를 활용하여 다차원 데이터를 처리할 수 있습니다.

```python
matrix = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
flattened = [num for row in matrix for num in row]
print(flattened)
```

위 코드는 2차원 리스트를 평탄화하여 1차원 리스트를 만듭니다.
