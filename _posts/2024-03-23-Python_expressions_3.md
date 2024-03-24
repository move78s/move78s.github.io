---
title: 파이썬 조건문/반복문 배우기 (3)
author: move78s
date: 2024-03-23 09:09:09 +0900
categories: [python, expressions]
tags: [python, 조건문, 반복문, conditional, loop, Pythonic]
---

# while 반복문의 파이써닉한 사용

파이썬에서 `while` 반복문은 특정 조건이 참인 동안 코드 블록을 반복 실행합니다. 하지만 무분별한 사용은 코드의 가독성을 해칠 수 있으며, 때로는 `for` 반복문이나 다른 파이썬 기능으로 대체할 수 있는 경우가 많습니다. 그럼에도 불구하고, 특정 상황에서 `while` 반복문의 파이써닉한 사용이 필요할 수 있습니다. 이번 포스트에서는 `while` 반복문을 효율적으로 사용하는 방법에 대해 살펴보겠습니다.

## 조건이 명확한 경우 사용하기

`while` 반복문을 사용할 때는 종료 조건이 명확해야 합니다. 종료 조건이 불분명하면 무한 루프에 빠질 위험이 있습니다.

```python
count = 0
while count < 5:
    print(f"Count is {count}")
    count += 1
```

위 코드는 `count`가 5보다 작은 동안 반복 실행되며, 매 반복마다 `count`를 1씩 증가시킵니다.

## 무한 루프와 break 사용하기

때로는 무한 루프를 의도적으로 사용하고, 특정 조건이 충족될 때 `break` 문을 사용하여 반복문을 종료할 수 있습니다.

```python
while True:
    response = input("Enter 'quit' to exit: ")
    if response == 'quit':
        break
```

위 코드는 사용자가 'quit'을 입력할 때까지 무한히 반복됩니다.

## else 절과 함께 사용하기

파이썬의 `while` 반복문은 `else` 절과 함께 사용할 수 있으며, `while` 루프가 더 이상 실행되지 않을 때 한 번 실행됩니다. 단, `while` 루프가 `break` 문으로 종료되면 `else` 블록은 실행되지 않습니다.

```python
n = 5
while n > 0:
    print(n)
    n -= 1
else:
    print("Loop is finished")
```

위 코드에서 `while` 반복문은 `n`이 0보다 클 동안 실행되며, 루프가 정상적으로 종료되면 `else` 블록이 실행됩니다.

## 결론

`while` 반복문은 파이썬에서 유용한 도구이지만, 사용할 때는 조건이 명확하도록 주의해야 합니다. 또한, 파이써닉한 코드 작성을 위해 무한 루프와 `break`, 그리고 `else` 절과의 조합을 적절히 활용해 보세요. 코드의 목적이 분명하고 읽기 쉬운지 항상 확인하면서, 효율적이고 파이써닉한 `while` 반복문 사용법을 실습해 보시길 바랍니다.
