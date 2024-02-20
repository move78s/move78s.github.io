---
title: Markdown 연습
author: Move78s
date: 2024-02-18 09:09:00 +0900
categories: [general]
tags: [markdown, blog]
published: false
---

[Test Post]({% link _posts/2024-02-17-test_post.md %})

## 개요

---

blog 작성을 위한 markdown 설명 페이지이다.<br>
blar blar <br>
어쩌고 저쩌고 <br>
<br>

## Markdown이란?

---

HTML을 사용한 웹 콘텐츠와 문서 작성은 복잡성과 낮은 가독성 문제를 가지고 있었습니다. <br>
HTML 태그를 정확히 기억하고 사용하는 것은 비전문가에게 어려웠으며, 많은 태그로 인해 실제 내용 파악이 힘들었습니다. <br>
이러한 문제를 해결하기 위해 Markdown이 개발되었습니다. <br>
Markdown은 간결한 문법으로 누구나 쉽게 사용할 수 있도록 설계되었으며, <br>
이를 통해 문서의 가독성이 향상되고 작성자는 내용에 더 집중할 수 있게 되었습니다. <br>
HTML로 쉽게 변환될 수 있는 Markdown은 웹 퍼블리싱을 간소화하며, <br>
기술 문서, 블로그, 포럼 글쓰기 등 다양한 분야에서 사용되어 생산성과 효율성을 높이고 있습니다.<br>
<br>

- Markdown 소개

  - 경량 마크업 언어로, 텍스트에 스타일을 적용하기 위한 간결한 문법 제공.
  - 웹 콘텐츠 작성 및 문서 편집을 위해 설계, HTML로 쉽게 변환됩니다.

- 배경 및 필요성

  - HTML 사용의 복잡성과 낮은 가독성 문제 해결 필요성에서 출발.
  - 사용자가 콘텐츠에 집중하고 효율적으로 작업할 수 있도록 만들어짐.

- 역사

  - 2004년 John Gruber와 Aaron Swartz에 의해 창안.
  - 목적은 최대한 읽기 쉽고, 쓰기 쉬운 웹 콘텐츠 생성.

- 주요 사용 분야

  - 기술 문서, 블로그 포스팅, 온라인 포럼 글쓰기 등.
  - 코드 스니펫 공유, 프로젝트 문서화 등 개발자 커뮤니티에서 널리 사용.

- 장점
  - 간단한 문법으로 누구나 쉽게 웹 콘텐츠를 작성할 수 있음.
  - 문서의 가독성과 편집 용이성 향상.
  - 다양한 플랫폼과 에디터에서 지원, 널리 사용됨.

<br>
<br>

---

#### 질문: Jekyll Chirpy 테마에서 Markdown으로 내 블로그의 글을 링크하려면 어떻게 작성해야 하나요?

Jekyll Chirpy 테마를 사용할 때 Markdown으로 내 블로그의 글을 링크하고 싶다면, 해당 글의 URL을 Markdown 링크 구문에 삽입하는 방법을 사용해야 합니다. 특히, Jekyll 사이트에서는 글의 상대 경로를 이용해 링크를 생성하는 것이 일반적입니다.

Markdown에서 Jekyll 글을 링크하는 예시는 다음과 같습니다:

```markdown
# 제목 1

## 제목 2

### 제목 3

- 목록형 1
  - 목록형 2

[링크 제목은 여기](https://www.google.com)
```

## 기본 기능

---

### 제목

- `전체 구조` : rule set이라고 합니다
- `선택자(selector)` : HTML의 요소 이름입니다. html요소, id, class등 어떤것을 꾸밀지 선택합니다.
- `속성(property)` : 선택자로 선택된 요소를 꾸미는 방법입니다. rule 안에서 여러가지 속성이 사용 될 수 있습니다. 속성은 반드시 속성 값을 가집니다.
- `속성 값(property value)` : 속성의 값입니다.
- `선언(declaration)` : 속성과 속성값을 아우릅니다. 각 선언들은 `세미콜론(;)으로 구분`됩니다
- `주석(comment)` : 한줄주석은 `//`, 여러줄 주석은 `/*주석입니다*/`의 형식으로, 코드에는 영향을 주지 않는 Comment입니다.

아래 이미지를 참고하면 쉽게 이해하실 수 있습니다.
![Desktop View](/assets/img/2021-10-30/1.PNG){: width="90%" }

선택자, 속성, 값은 여러가지가 존재합니다. 이미지와 같이 중첩으로도 사용할 수 도 있습니다.

이번에도 순서대로 알아봅시다!
<br>
<br>

## CSS 적용 방법

---

[HTML - 많이 사용되는 태그 28선 - style태그](https://wlqmffl0102.github.io/posts/The-Thirty-Two-Elements-Used-On-Most-Pages/#style-%ED%83%9C%EA%B7%B8)에서 기술하였으나, 동일하게 한번 더 작성하도록 하겠습니다.

html 및 태그에 관해서 잘 모르신다면 [HTML 사용해보기 - HTML기본](https://wlqmffl0102.github.io/posts/Try-Using-Html/#html-%EA%B8%B0%EB%B3%B8)을 참고 부탁드립니다.

CSS 적용방법에관해서 3가지 방법이 존재합니다.

- 인라인(inline) 스타일
- 내부스타일시트
- 외부스타일시트 -> 가장 권장되는 사용법입니다.

외부 스타일시트가 가장 권장되기는 하지만, 우선순위는 다음과 같습니다<br>
브라우저 디자인 정의 -> 외부스타일시트 -> 내부스타일시트 -> 인라인스타일시트

**인라인 스타일** : style적용을 하고 싶은 태그에 style 속성을 작성

```html
<!DOCTYPE html>
<html>
  <body>
    <p style="color:red; font-size:20px;">Dodev 하다</p>
  </body>
</html>
```

````

```

```

**내부스타일시트** : `head`태그 안에 style태그를 이용해 작성

```html
<!DOCTYPE html>
<html>
  <head>
    <style>
      body {
        background-color: black;
      }
      p {
        color: white;
        font-size: 20px;
      }
    </style>
  </head>
  <body>
    <p>Dodev 하다</p>
  </body>
</html>
```

**외부스타일시트** : 별도의 css파일을 작성한 뒤, `heaed`태그 안에 `link`태그를 사용해 현재 작성중인 html파일에 연결하여 사용. 가장 권장되는 사용법.

아래와 같이 별도의 style을 정의한 .css파일을 생성한다.

```css
body {
  background-color: skyblue;
}
p {
  color: purple;
  text-decoration: underline;
  font-size: 20px;
}
```

생성된 .css파일을 .html파일과 연결한다.

```html
<!DOCTYPE html>
<html>
  <head>
    <link rel="stylesheet" href="./test.css" />
  </head>
  <body>
    <p>Dodev 하다</p>
  </body>
</html>
```

순서대로 인라인스타일, 내부스타일시트, 외부스타일시트 사용 결과입니다!

![Desktop View](/assets/img/2021-10-16/4.PNG){: width="30%" }

![Desktop View](/assets/img/2021-10-16/5.PNG){: width="30%" }

![Desktop View](/assets/img/2021-10-16/6.PNG){: width="30%" }

<br>
<br>

## 선택자(selector)

---

선택자(selector)란 html요소, id, class 등 어떤 것을 꾸밀지 선택하는 것 입니다.

1. html 요소 선택자 : html의 요소를 선택합니다. 선택자의 이름은 태그명이 되기 때문에 태그 선택자라고 불리기도 합니다.

   - p : html내의 `p태그`를 모두 선택합니다.
   - div : html내의 `div태그`를 모두 선택합니다.

2. 아이디 선택자 : 해당하는 id속성을 가진 태그를 선택합니다. 한 태그 당 최대 1개의 아이디만을 가집니다.

   - #my-name : html의 모든 요소(태그) 중 id속성이 `my-name`인 태그를 선택합니다.<br>`<p id="my-name">` 또는 `<div id="my-name">`와 같은 태그를 선택하게 됩니다.

3. 클래스 선택자 : 해당하는 class속성을 가진 태그를 선택합니다. 태그에서 class는 다중으로 사용 가능합니다.

   - .my-name : html의 모든 요소(태그) 중 id속성이 `my-name`인 태그를 선택합니다.<br>`<p class="my-name">` 또는 `<div class="my-name">`와 같은 태그를 선택하게 됩니다.

4. 속성 선택자 : 태그에서 특정 속성을 갖는 요소를 선택합니다.

   - img[src] : `<img src="test.png">`를 선택하지만 `img태그`는 선택하지 않고, `src`속성만 선택합니다.

5. 수도(Pseudo) 클래스 선택자 : 요소의 상태에 따라 해당요소를 선택합니다. 요소의 상태란, 마우스를 움직이거나, 클릭하거나, 키보드를 입력할 때 요소의 상태는 변하게 됩니다. 그 변한 상태를 선택합니다.

- `(태그):(수도 클래스 선택자)` 의 형식을 가집니다.
- ex) a:hover
  - :hover : 해당하는 태그에 마우스를 올렸을 경우에만 선택됩니다.
  - :focus : 키보드 이벤트 및 입력 요소에서 포커스가 잡혔을 경우 선택됩니다.
  - :first-child, :last-child : 부모 요소의 자식 중, 가장 첫 번째 또는 마지막 요소를 선택합니다.
  - :active : 특정 요소를 클릭 한 경우 선택됩니다.

<br>
<br>

## 속성(property)과 속성 값(property value)

---

속성(property)과 속성 값(property value)은 말 그대로 어떠한 html요소를 선택자를 통해 선택한 뒤, 해당 요소에 어떤 속성을, 그 속성은 무슨값을 주는지를 이릅니다.

예를 들어, 아래와 같은 html 파일이 있다고 생각해봅시다.

```html
<html>
  <body>
    <h1>안녕하세요. Dodev 하다입니다.</h1>
    <div class="div_class" id="first">첫번째 div</div>
    <div class="div_class" id="second">두번째 div</div>
    <div class="div_class">세번째 div</div>
  </body>
</html>
```

어떠한 CSS도 설정되어 있지 않기 때문에 적힌 내용이 그대로 보일겁니다. 그냥 글자들의 나열이죠.
body안에 글자가 4줄 나옵니다. h1태그만 글자 크기가 다르죠.

선택자를 이용해 여러가지를 선택한 뒤, CSS를 사용해볼까요?

### 인라인스타일

**인라인 스타일**부터 시작해볼까요?

```html
<html>
  <head>
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link
      href="https://fonts.googleapis.com/css2?family=Nanum+Pen+Script&display=swap"
      rel="stylesheet"
    />
  </head>
  <body>
    <h1 style="color:blue;">안녕하세요. Dodev 하다입니다.</h1>
    <div
      class="div_class"
      id="first"
      style="width:200px; height:200px; background-color: yellow;"
    >
      첫번째 div
    </div>
    <div
      class="div_class"
      id="second"
      style="height:200px; font-size:20px; font-weight:bold; background-color:black; color: white;"
    >
      두번째 div
    </div>
    <div
      class="div_class"
      style="text-align: center; font-family: 'Nanum Pen Script', cursive; font-size: 100px;"
    >
      세번째 div
    </div>
  </body>
</html>
```

각각의 태그에 직접 `style=""`이라는 속성을 줍니다. style속성에 영향을 받아 해당 태그는 속성에 따라 변합니다.
이때, style속성안에서 세미콜론(;)으로 구분되는 녀석이 `(속성):(속성값);`입니다.
결과물은 아래와 같습니다.

![Desktop View](/assets/img/2021-10-30/1.PNG){: width="100%" }

참고로 head태그 안 link태그는 세번째 div에 폰트를 적용하기 위함입니다.

### 내부스타일시트

다음으로는 **내부스타일시트** 입니다.
동일한 스타일을 내부스타일시트를 적용하여 사용해보겠습니다.

```html
<!DOCTYPE html>
<html>
  <head>
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link
      href="https://fonts.googleapis.com/css2?family=Nanum+Pen+Script&display=swap"
      rel="stylesheet"
    />
    <style>
      h1 {
        color: blue;
      }
      #first {
        width: 200px;
        height: 200px;
        background-color: yellow;
      }
      #second {
        height: 200px;
        font-size: 20px;
        font-weight: bold;
        background-color: black;
        color: white;
      }
      .div_class {
        text-align: center;
        font-family: "Nanum Pen Script", cursive;
        font-size: 100px;
      }
    </style>
  </head>
  <body>
    <h1>안녕하세요. Dodev 하다입니다.</h1>
    <div class="div_class" id="first">첫번째 div</div>
    <div class="div_class" id="second">두번째 div</div>
    <div class="div_class">세번째 div</div>
  </body>
</html>
```

인라인 스타일과 동일한 속성과 속성값을 이용해, 선택자에 맞게 style시트를 내부로 사용했습니다!
눈에 딱 보이시겠지만 html코드와 css코드가 나뉘어있어 좀 더 편한 느낌이 있네요~!
style태그안에서 선택자를 변화시킬 `(속성):(속성값);`이 눈에 더 잘 들어옵니다.

그런데, 해당 html파일을 브라우저에서 실행해보면 인라인 스타일과 조금 다르게 나옵니다.

![Desktop View](/assets/img/2021-10-30/2.PNG){: width="100%" }

이렇게 말이지요!
인라인 스타일에서는 세번째 div에서만 텍스트 정렬과 폰트설정을 해서, 그렇게 확인이 되었는데
지금은 모든 div태그에서 정렬과 폰트가 설정되어 보입니다!

이유는 바로 세번째 div태그의 선택자 때문인데요.
첫번째 div와 두번째 div는 id를 이용해 개별선택을 한 반면, 세번째 div는 class를 이용해서 선택하였습니다. 왜냐하면 id속성이 없기 때문이죠.
이때, 세번째 div의 style속성을 위해 class를 선택하였지만, "div_class"클래스는 모든 div 태그들이 가지고 있는 class속성이죠.

그렇기에 첫번째 div, 두번째 div 마지막으로 세번째 div가 정렬 및 폰트 설정에 영향을 받게 됩니다.

근데 만약, 세번째에만 정렬과 폰트가 적용이 되었으면 좋겠다면,
다음과 같이 설정해줍니다.

```html
<!DOCTYPE html>
<html>
  <head>
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link
      href="https://fonts.googleapis.com/css2?family=Nanum+Pen+Script&display=swap"
      rel="stylesheet"
    />
    <style>
      h1 {
        color: blue;
      }
      #first {
        text-align: left;
        font-family: Verdana, Geneva, Tahoma, sans-serif;
        width: 200px;
        height: 200px;
        background-color: yellow;
      }
      #second {
        text-align: left;
        font-family: Verdana, Geneva, Tahoma, sans-serif;
        height: 200px;
        font-size: 20px;
        font-weight: bold;
        background-color: black;
        color: white;
      }
      .div_class {
        text-align: center;
        font-family: "Nanum Pen Script", cursive;
        font-size: 100px;
      }
    </style>
  </head>
  <body>
    <h1>안녕하세요. Dodev 하다입니다.</h1>
    <div class="div_class" id="first">첫번째 div</div>
    <div class="div_class" id="second">두번째 div</div>
    <div class="div_class">세번째 div</div>
  </body>
</html>
```

별 다른것은 없습니다. id속성이 first, second인 경우에는 text-align속성과 font-family설정을 미리 해두는것이죠.
CSS는 기본적으로 가장 처음의 속성값을 활용합니다. first와 second id속성을 가진 요소에서 text-align속성과 font-family속성을 미리 정의해둔다면,
아래쪽에 나오는 .div_class의 text-align속성과 font-family속성은 무시하게 되죠.

반대로, .div_class속성이 가장 위에 작성된 경우에는 해당 속성이 사용됩니다.

또 다른 방법으로는 세번째 div에 id속성을 설정하고, 설정된 id를 선택자로 사용하면 됩니다.

### 외부스타일시트

마지막으로 **외부스타일시트** 입니다
html소스 안에 style태그를 사용해 작성하였던 내부스타일시트형식을, .css파일로 완전 분리를 하는것입니다.
다음과 같이 새로운 test.css파일을 하나 작성합니다.

```css
h1 {
  color: blue;
}
#first {
  text-align: left;
  font-family: Verdana, Geneva, Tahoma, sans-serif;
  width: 200px;
  height: 200px;
  background-color: yellow;
}
#second {
  text-align: left;
  font-family: Verdana, Geneva, Tahoma, sans-serif;
  height: 200px;
  font-size: 20px;
  font-weight: bold;
  background-color: black;
  color: white;
}
.div_class {
  text-align: center;
  font-family: "Nanum Pen Script", cursive;
  font-size: 100px;
}
```

.css파일을 작성한 뒤, head태그 안에서 link태그를 이용해 .css파일을 연결해줍니다.

```html
<!DOCTYPE html>
<html>
  <head>
    <link rel="stylesheet" href="./test.css" />
  </head>
  <body>
    <h1>안녕하세요. Dodev 하다입니다.</h1>
    <div class="div_class" id="first">첫번째 div</div>
    <div class="div_class" id="second">두번째 div</div>
    <div class="div_class">세번째 div</div>
  </body>
</html>
```

작성방법 및 적용순서 등은 내부스타일시트와 동일합니다.

CSS(디자인)과 html(뼈대)가 완전 분리되어 있기 때문에 코드를 작성, 확인 및 수정 등의 관리가 용이합니다.
처음 css를 작성하실때에는 인라인스타일이 태그에서 바로 적용되어 편하지 않을까 생각되기도 하지만,
사용하다 보면 생각보다 코드 관리가 굉장히 귀찮고 번거롭다는것을 알 수 있게 됩니다.

CSS는 좀 더 발전하여 SASS와 SCSS라는 새로운 녀석도 등장했습니다. CSS문법을 좀더 간결하게 사용하고, 유지보수의 용이성을 더 높인것입니다.
<br>
<br>

## 주석(comment)

---

- html과 동일 내용입니다! 주석의 형식만 다릅니다.

프로그래밍에 관해 조금이라도 아신다면 주석이야 다 아시겠지만, 주석이 무엇인지 잘 모르시는 분들을 위해 끼워 넣습니다.

주석이란, 작성된 CSS에서 아무런 기능을하지않는 메모입니다. 아무런 역할이 없습니다.
`//주석입니다(한줄 주석)` 또는 `/* 주석입니다(다중 주석) */`와 같은 형식으로 사용됩니다.

사실 많은 초보자분들이 주석을 잘 쓰지 않습니다. 오히려 반대로 시간이 가면 갈 수록 많은 분들이 주석의 참된 의미를 알게되죠.

주석은 `메모`입니다. 사실 혼자 모든 코드를 짜게 되면, 그래서 어느 위치에 어떤 코드가 어떤 역할을 하는지, 어디와 함께 연결되는지를 잘 안다면 메모는 필요가 없죠.

협업을 하면서 이 코드가, 혹은 데이터가 무엇인지, 왜 있는지 등에 대한 정보가 필요합니다. 함께 일하는 다른분들을 위해서 현재 내가 작성하는 이 코드가 무엇인지, 왜있는지 등 여러가지 정보를 남겨야 합니다. 그렇지 않으면 매번 코드를 분석하거나 코드를 작성한 분께 가서 여쭤봐야할지도 모르죠.
그래서 적어도 메모를 남겨두는 것입니다.

또는, 처음부터 끝까지 작성한 코드가 있다고 생각해봅시다. 코드를 작성할때에는 문제가 되지 않습니다. 하지만 1년동안 그 코드를 보지 않았다고 생각해봅시다. 1년 뒤에 그 파일을 열어서 보면 작성할때와는 사뭇 다른 느낌을 받으실겁니다. 그렇기에 본인을 위해서도 주석을 잘 남겨둬야하죠.

<br>
<br>

## 마무리

---

이번에도 어김없이 포스팅이 길어졌습니다.
워낙 방대한 양이라 한 포스팅에서 다루기가 어려운것같습니다. html도, css도, 다음으로 다룰 JS또한 말이죠.

기본적인 내용입니다만, 무리없이 편하게 읽을 수 있는 포스팅이 되었으면 합니다.

감사합니다.

```

```
````
