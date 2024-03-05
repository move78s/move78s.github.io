---
title: Machin Learning 기초 1 - 주가 예측
author: move78s
date: 2024-03-04 09:09:09 +0900
categories: [python, Machin Learning]
tags: [python, Machin Learning]
---

# 파이썬으로 마이크로소프트 주가 데이터 가져오기

이 포스트에서는 파이썬을 사용하여 마이크로소프트의 최근 한 달 간 주가 데이터를 어떻게 가져올 수 있는지를 단계별로 안내합니다.

## 필요한 라이브러리 설치

먼저, 파이썬 환경에서 주가 데이터를 가져오기 위해 필요한 yfinance 라이브러리를 설치해야 합니다. 아래의 명령어를 사용하여 설치할 수 있습니다:

```bash
pip install yfinance
```

## 주가 데이터 가져오기

yfinance 라이브러리를 사용하여 마이크로소프트의 주가 데이터를 가져오는 코드는 다음과 같습니다:

```python
import yfinance as yf
from datetime import datetime, timedelta

# 현재 날짜에서 한 달 전 날짜를 계산
end_date = datetime.now()
start_date = end_date - timedelta(days=30)

# 마이크로소프트의 주가 데이터를 다운로드
msft_data = yf.download('MSFT', start=start_date, end=end_date)
print(msft_data)
```

## 데이터 검사 및 시각화

다운로드된 데이터는 Pandas DataFrame 형태로 반환됩니다. 데이터의 첫 부분을 확인하기 위해 msft_data.head() 함수를 사용하고, 주가의 시간에 따른 변화를 보기 위해 간단한 시각화도 수행할 수 있습니다.

## 결론

이 포스트에서는 yfinance 라이브러리를 사용하여 파이썬으로 주가 데이터를 쉽게 가져오는 방법을 소개하였습니다. 이 데이터는 머신러닝 모델을 통한 주가 예측 등 다양한 데이터 과학 프로젝트에 사용될 수 있습니다.
