---
title: 파이썬 리스트 배우기 (2)
author: move78s
date: 2024-03-03 09:09:09 +0900
categories: [python, list]
tags: [python, list, list comprehension, list length]
---

# 파이썬 리스트 배우기 (2)

파이썬의 리스트를 초보자 수준에서 조금 더 깊게 이해하기 위한 다음 단계는 리스트의 조작 및 탐색 방법을 배우는 것입니다. 이번 글에서는 리스트의 요소를 추가, 삭제, 수정하는 방법과 리스트 내부를 탐색하는 다양한 기법에 대해 알아보겠습니다.

## 리스트에 요소 추가하기

리스트에 새로운 요소를 추가하는 방법에는 여러 가지가 있습니다. 가장 기본적인 방법은 `append()` 메서드를 사용하는 것입니다. 이 메서드는 리스트의 끝에 새로운 요소를 추가합니다.

```python
fruits = ["apple", "banana", "cherry"]
fruits.append("orange")
print(fruits)  # ['apple', 'banana', 'cherry', 'orange']
```

또 다른 방법은 `insert()` 메서드를 사용하여 리스트의 특정 위치에 요소를 삽입하는 것입니다. `insert()` 메서드는 두 개의 인자를 받으며, 첫 번째 인자는 삽입할 위치, 두 번째 인자는 삽입할 요소입니다.

```python
fruits.insert(1, "blueberry")
print(fruits)  # ['apple', 'blueberry', 'banana', 'cherry', 'orange']
```

리스트의 끝에 여러 요소를 동시에 추가하고 싶다면, `extend()` 메서드를 사용할 수 있습니다. 이 메서드는 다른 컬렉션의 모든 요소를 현재 리스트 끝에 추가합니다.

```python
additional_fruits = ["mango", "pineapple"]
fruits.extend(additional_fruits)
print(fruits)  # ['apple', 'blueberry', 'banana', 'cherry', 'orange', 'mango', 'pineapple']
```

마지막으로, 두 리스트를 연결하여 새로운 리스트를 만드는 방법도 있습니다. `+` 연산자를 사용하여 두 리스트를 간단히 결합할 수 있습니다.

```python
more_fruits = ["grape", "pear"]
new_fruits_list = fruits + more_fruits
print(new_fruits_list)  # ['apple', 'blueberry', 'banana', 'cherry', 'orange', 'mango', 'pineapple', 'grape', 'pear']
```

## 리스트에서 요소 삭제하기

리스트에서 요소를 삭제하는 방법도 다양합니다. `remove()` 메서드를 사용하면 특정 값을 가진 첫 번째 요소를 삭제할 수 있습니다.

```python
fruits.remove("banana")
print(fruits)  # ['apple', 'blueberry', 'cherry', 'orange', 'mango', 'pineapple']
```

`pop()` 메서드는 리스트의 특정 위치에 있는 요소를 삭제하고, 그 요소를 반환합니다. 위치를 지정하지 않으면, 기본적으로 리스트의 마지막 요소를 삭제합니다.

```python
last_fruit = fruits.pop()
print(last_fruit)  # 'pineapple'
print(fruits)  # ['apple', 'blueberry', 'cherry', 'orange', 'mango']
```

## 리스트 요소 수정하기

리스트의 요소를 수정하는 것은 매우 간단합니다. 특정 인덱스의 요소에 새로운 값을 할당하기만 하면 됩니다.

```python
# 리스트의 앞 부분에 요소 추가하기
fruits[0] = "strawberry"
print(fruits)  # ['strawberry', 'blueberry', 'cherry', 'orange', 'mango']

# 리스트의 마지막 부분에 요소 추가하기
fruits[-1] = "apple"
print(fruits)  # ['strawberry', 'blueberry', 'cherry', 'orange', 'mango', 'apple']

```

## 리스트 탐색하기

리스트 내에서 특정 요소를 찾거나, 리스트를 순회하고 싶을 때는 여러 방법을 사용할 수 있습니다. `in` 키워드를 사용하면 특정 요소가 리스트 내에 있는지 확인할 수 있습니다.

```python
if "blueberry" in fruits:
    print("Blueberry is in the list")
```

리스트를 순회하면서 각 요소를 처리하고 싶을 때는 `for` 루프를 사용할 수 있습니다.

```python
for fruit in fruits:
    print(fruit)
```

## 결론

리스트는 파이썬에서 가장 기본적이면서도 강력한 데이터 구조 중 하나입니다. 이번 단계에서는 리스트의 요소를 추가, 삭제, 수정하는 방법과 리스트를 탐색하는 기법을 배웠습니다.
리스트와 함께라면 복잡한 데이터 구조를 쉽게 다룰 수 있으며, 다양한 데이터 처리 작업을 간단하게 해결할 수 있습니다. 파이썬의 다른 고급 기능과 함께 사용할 때, 리스트는 더욱 강력한 도구가 됩니다.
