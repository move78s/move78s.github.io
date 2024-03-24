---
title: 파이썬 리스트 배우기 (3)
author: move78s
date: 2024-03-03 09:09:09 +0900
categories: [python, list]
tags: [python, list, list comprehension, list length]
---

# 파이썬 리스트 배우기 (3)

리스트를 사용하는 기본적인 방법을 익혔다면, 이제 파이썬에서 리스트를 더 효과적으로 활용하는 방법을 배워볼 차례입니다. 이 단계에서는 리스트의 고급 기능과 다양한 리스트 조작 기법에 대해 알아볼 것입니다. 이를 통해 데이터를 더욱 효율적으로 처리하고, 파이썬 프로그래밍의 가능성을 확장할 수 있습니다.

## 리스트 슬라이싱

리스트 슬라이싱은 리스트의 특정 부분을 선택하여 새로운 리스트를 만드는 기능입니다. 이는 리스트의 일부분만을 추출하거나 복사할 때 유용합니다.

```python
fruits = ["apple", "banana", "cherry", "date", "elderberry", "fig", "grape"]
selected_fruits = fruits[2:5]
print(selected_fruits) # ['cherry', 'date', 'elderberry']
```

슬라이싱을 사용할 때, 시작 인덱스는 포함되지만 종료 인덱스는 포함되지 않습니다. 또한, 시작 또는 종료 인덱스를 생략하면 리스트의 시작 또는 끝을 의미합니다.

## 리스트 정렬

리스트의 요소를 정렬하는 것은 데이터를 분석하거나 출력할 때 중요할 수 있습니다. `sort()` 메서드를 사용하면 리스트 자체가 변경되며, `sorted()` 함수는 리스트의 정렬된 복사본을 반환합니다.

```python
numbers = [3, 1, 4, 1, 5, 9, 2, 6, 5]
numbers.sort()
print(numbers) # [1, 1, 2, 3, 4, 5, 5, 6, 9]
```

정렬 시 문자열 리스트의 경우 알파벳 순으로, 숫자 리스트의 경우 숫자의 크기 순으로 정렬됩니다. 역순으로 정렬하려면, `sort()` 메서드나 `sorted()` 함수에 `reverse=True` 매개변수를 추가합니다.

## 리스트 컴프리헨션

리스트 컴프리헨션은 파이썬의 강력한 기능 중 하나로, 새로운 리스트를 생성하는 간결한 방법을 제공합니다. 이 방법을 사용하면 for 루프와 if 문을 사용하여 리스트를 구성하는 복잡한 로직을 한 줄의 코드로 줄일 수 있습니다.

```python
squared_numbers = [x ** 2 for x in range(10)]
print(squared_numbers) # [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
```

조건을 추가하여 특정 조건을 만족하는 요소만으로 새 리스트를 생성할 수도 있습니다.

```python
even_numbers = [x for x in range(20) if x % 2 == 0]
print(even_numbers) # [0, 2, 4, 6, 8, 10, 12, 14, 16, 18]
```

문자열을 포함한 리스트에서 특정 문자를 포함하는 요소만을 필터링하는 경우에 매우 유용합니다.

```python
# 'a'를 포함하는 단어만 새로운 리스트에 추가
words = ["apple", "banana", "cherry", "date"]
words_with_a = [word for word in words if 'a' in word]
print(words_with_a) # 결과: ['apple', 'banana', 'date']
```

## 리스트와 다른 데이터 구조

리스트 외에도 파이썬에는 다양한 데이터 구조가 있습니다. 예를 들어, 튜플은 변경할 수 없는 리스트이고, 세트는 중복을 허용하지 않는 요소의 집합입니다. 각 데이터 구조는 사용하는 경우에 따라 장단점이 있으며, 이들을 리스트와 함께 사용함으로써 프로그램의 효율성을 높일 수 있습니다.

## 결론

이 단계에서는 파이썬 리스트의 고급 기능과 다양한 조작 기법을 배웠습니다. 리스트 슬라이싱부터 정렬, 리스트 컴프리헨션까지 다루며, 리스트와 다른 데이터 구조의 비교를 통해 파이썬 프로그래밍의 유연성을 살펴보았습니다. 이러한 고급 기능을 이해하고 활용함으로써, 여러분의 파이썬 코드는 더욱 강력하고 효율적이 될 것입니다.