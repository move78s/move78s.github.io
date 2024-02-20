---
title: 엑셀에서 공백을 제외한 글자수 세는 방법
author: move78s
date: 2024-02-20 09:09:09 +0900
categories: [lang, vba]
tags: [excel, vba, count, 글자수, length, statusbar]
---

## 서론

엑셀에서 텍스트 데이터를 다룰 때, 특정 셀 내의 문자 수를 세는 것은 매우 유용한 작업 중 하나입니다. <br>
특히, 공백을 제외한 순수한 글자수를 파악하는 것은 데이터 분석, 텍스트 처리, 보고서 작성 등 다양한 상황에서 필요할 수 있습니다. <br>
이 글에서는 엑셀에서 공백을 제외한 글자수를 세는 세 가지 방법을 소개합니다.<br>

---

## 방법 1: 기본 함수 사용하기

가장 간단한 방법은 엑셀의 `LEN` 함수와 `SUBSTITUTE` 함수를 조합하는 것입니다. `LEN` 함수는 문자열의 길이를 반환하며, `SUBSTITUTE` 함수는 문자열에서 특정 문자를 다른 문자로 대체합니다. 이 두 함수를 사용해 공백을 제거한 후 글자수를 세어보겠습니다.

**예시:**

```excel
=LEN(SUBSTITUTE(A1, " ", ""))
```

이 수식은 A1 셀에 있는 텍스트에서 모든 공백을 제거한 후, 남은 문자의 수를 계산합니다.

---

## 방법 2: VBA 사용자 정의 함수 만들기

보다 고급 기능을 원하거나, 특정 조건에 맞는 글자수를 세고 싶다면, VBA를 사용하여 사용자 정의 함수를 만들 수 있습니다. 아래는 공백을 제외한 글자수를 세는 VBA 함수의 예입니다.

1. `Alt + F11`을 눌러 VBA 편집기를 엽니다.
2. `메뉴` > `삽입` > `모듈`을 클릭하여 새 모듈을 생성합니다.
3. 다음 코드를 모듈에 복사하고 붙여넣습니다:

   ```vb
   Function CountCharsExcludingSpaces(rng As Range) As Integer
       Dim cleanText As String
       cleanText = Replace(rng.Value, " ", "")
       CountCharsExcludingSpaces = Len(cleanText)
   End Function

   ```

4. VBA 편집기를 닫고 엑셀로 돌아가서 다음 수식을 사용합니다:
   ```excel
   =CountCharsExcludingSpaces(A1)
   ```

이 사용자 정의 함수는 선택한 셀에서 공백을 제외한 글자수를 계산합니다.

---

## 방법 3: 셀 선택 시 상태바에 글자수 표시하기

마지막으로, 셀을 선택할 때마다 자동으로 공백을 제외한 글자수를 엑셀의 상태바에 표시하는 방법입니다. 이 방법은 VBA를 사용하여 구현됩니다.

1. `Alt + F11`을 눌러 VBA 편집기를 엽니다.
2. `현재_통합_문서` 선택 > `보기` > `코드` (F7)를 선택하여, 현재 통합 문서 코드창을 오픈합니다.
3. 해당 워크시트의 코드 창에 다음 스크립트를 복사하고 붙여넣습니다:

   ```vb
   Private Sub Worksheet_SelectionChange(ByVal Target As Range)
       If Target.Cells.Count = 1 Then
           Dim cleanText As String
           cleanText = Replace(Target.Text, " ", "")
           Application.StatusBar = "글자수: " & Len(cleanText)
       Else
           Application.StatusBar = False
       End If
   End Sub
   ```

   이 코드는 셀을 선택할 때마다 해당 셀의 공백을 제외한 글자수를 상태바에 표시합니다.

---

<details>
<summary><strong>기타 : 글자수 입력 제한 설정 방법</strong></summary>
엑셀에서 데이터 유효성 검사(Data Validation) 기능을 사용하여 셀에 입력할 수 있는 글자수를 제한할 수 있습니다. <br>
이 기능은 사용자가 셀에 입력할 수 있는 값의 범위, 글자수 제한 및 잘못된 데이터의 입력을 방지할 수 있습니다. <br>
글자수를 기준으로 입력을 제한하는 방법은 다음과 같습니다.<br>

<ol>
  <li>데이터 유효성 검사 설정
    <ul>
      <li>먼저, 글자수 제한을 적용할 셀이나 셀 범위를 선택합니다.</li>
      <li>리본 메뉴에서 데이터 탭을 클릭합니다.</li>
      <li>데이터 유효성 검사 버튼을 클릭합니다. (데이터 도구 그룹에 있음)</li>
    </ul>
  </li>
  <li>유효성 검사 조건 설정
    <ul>
        <li>데이터 유효성 검사 대화 상자에서 설정 탭을 선택합니다.</li>
        <li>허용 드롭다운 메뉴에서 텍스트 길이를 선택합니다.</li>
        <li>데이터 드롭다운 메뉴에서 글자수 조건(예: 사이)을 선택하고, 적절한 최소값과 최대값을 입력합니다.</li>
    </ul>
  </li>
  <li>설정 완료
    <ul>
        <li>모든 설정을 마친 후 확인 버튼을 클릭하여 설정을 완료합니다.</li>
    </ul>  
  </li>
</ol>

</details>
