---
title: 파이썬 리스트 배우기 (5)
author: move78s
date: 2024-03-03 09:09:09 +0900
categories: [python, list]
tags: [python, list, list comprehension, list length]
---

# 파이썬 리스트 배우기 (5)

리스트의 기본부터 고급 기능까지 숙지했다면, 이제 이러한 지식을 활용하여 더 실용적이고 복잡한 문제를 해결할 준비가 되었습니다. 이 단계에서는 실제 데이터를 다루고 분석하는 과정을 통해 파이썬 리스트의 강력한 활용 사례를 살펴보겠습니다.

## 실용적인 데이터 분석: 날씨 데이터 처리하기

예를 들어, 한 달간의 최고 기온 데이터가 리스트로 주어졌다고 가정해 봅시다. 우리의 목표는 이 데이터를 분석하여 평균 최고 기온을 찾고, 최고 온도와 최저 온도를 확인하는 것입니다.

```python
daily_temperatures = [22, 24, 26, 31, 32, 33, 30, 29, 28, 22, 21, 20, 24, 26, 27, 28, 30, 31, 32, 33, 34, 35, 36, 37, 38, 39, 40, 22, 21, 19]
```

### 평균 기온 계산

```python
average_temp = sum(daily_temperatures) / len(daily_temperatures)
print("Average temperature for the month:", average_temp)
```

### 최고 기온과 최저 기온 찾기

```python
max_temp = max(daily_temperatures)
min_temp = min(daily_temperatures)
print("Maximum temperature for the month:", max_temp)
print("Minimum temperature for the month:", min_temp)
```

이 코드는 단순하지만, 실제 생활에서 유용하게 활용할 수 있는 데이터 분석의 예입니다.

## 프로젝트: 간단한 주식 데이터 분석

주식 시장 데이터를 분석하는 간단한 프로젝트를 생각해 봅시다. 여러분은 특정 주식의 일별 종가 데이터를 리스트로 가지고 있으며, 이를 기반으로 평균 종가를 계산하고, 가장 높았던 종가와 가장 낮았던 종가를 찾아내고 싶습니다.

```python
closing_prices = [120, 122, 125, 123, 119, 122, 126, 130, 128, 135, 138, 140, 145, 148, 147, 149, 150, 152, 151, 153, 155, 150, 149, 147, 148, 150, 152, 153, 149, 145]
```

### 평균 종가 계산

```python
average_price = sum(closing_prices) / len(closing_prices)
print("Average closing price:", average_price)
```

### 최고 종가와 최저 종가 찾기

```python
max_price = max(closing_prices)
min_price = min(closing_prices)
print("Maximum closing price:", max_price)
print("Minimum closing price:", min_price)
```

이러한 분석은 투자 결정을 내리는 데 도움을 줄 수 있으며, 파이썬 리스트를 사용하여 쉽게 수행할 수 있습니다.

## 결론

파이썬 리스트를 사용하여 복잡한 데이터를 쉽게 처리하고 분석할 수 있습니다. 실제 문제를 해결하는 과정에서 이러한 기술을 활용해 보세요. 데이터 분석, 재고 관리, 금융 계산 등 다양한 분야에서 파이썬 리스트는 매우 유용한 도구가 될 것입니다. 계속해서 연습하고 새로운 프로젝트에 도전함으로써 여러분의 파이썬 프로그래밍 실력을 한층 더 향상시키세요.
