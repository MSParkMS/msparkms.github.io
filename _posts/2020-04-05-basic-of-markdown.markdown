---
layout: post
title: "Markdown 문법 기초"
date: 2020-04-05 01:07:08 +0900
categories: [Blog]
---

# Markdown 문법 기초

## 개요
* GitHub IO에 블로그를 만들었기 때문에 마크다운에 익숙해져야 한다.
* [GFM](https://github.github.com/gfm/ "github flavored markdown spec")를 기준으로 간단하게 사용할 만큼만 정리해보자.

## 헤더
* 글머리 - 6단계 지원
  ```markdown
    # This is the h1
    ## This is the h2
    ### This is the h3
    #### This is the h4
    ##### This is the h5
    ###### This is the h6
  ```

# This is the h1
## This is the h2
### This is the h3
#### This is the h4
##### This is the h5
###### This is the h6

## 블록인용
* `>` 블럭인용문자를 사용
  ```markdown
    > This is a quote1
    > > This is a quote2
    > > > This is a quote3
  ```
  > This is a quote1
  > > This is a quote2
  > > > This is a quote3

## 리스트
* 숫자 리스트 (숫자를 나열)

```markdown
  1. description1
  2. description2
  3. description3
```

1. description1
2. description2
3. description3

* 기호 리스트(`*`, `+`, `-`)

```markdown
  * description1
    * description1-1
      * description1-1-1
```

* description1
  * description1-1
    * description1-1-1

## 코드 블럭
* 코드 블럭 기호 사용법 (```)
<pre><code>
  ```CPP (highlighting을 적용하고자 하는 언어)
    printf("Hello World!\n");
  ```
</code></pre>

```CPP
  printf("Hello World!\n");
```

* 인라인 코드 블럭 (`)
```
  `인라인 코드`
```

`인라인 코드`
  
## 수평선 추가
* 다양한 방법이 가능
```markdown
  ***
  ---
```

***
---

## 링크 추가
* 외부 링크
```markdown
  Link : [GFM](https://github.github.com/gfm/ "github flavored markdown spec")
```

Link : [GFM](https://github.github.com/gfm/ "github flavored markdown spec")

* 내부 링크
```markdown
  <div id="Title">제목</div>
  [제목](#Title)
```

## 강조
* 볼드, 이탤릭, 취소등 다양한 강조 기능 제공
```markdown
  *이탤릭*
  _이탤릭_
  **볼드**
  __볼드__
  ~~취소~~
```

*이탤릭*   
_이탤릭_   
**볼드**   
__볼드__   
~~취소~~   

* 원하는 색상 넣기
```markdown
  원하는 <span style="color:red">색상</span> 넣기
```

원하는 <span style="color:red">색상</span> 넣기   

## 줄 바꿈
* 뒤에 띄어쓰기 3칸이상을 넣어준다.
```markdown
  뒤에 띄어쓰기 없음
  줄 바꿈 테스트

  뒤에 띄어쓰기 3칸   
  줄 바꿈 테스트
```

뒤에 띄어쓰기 없음
줄 바꿈 테스트

뒤에 띄어쓰기 3칸   
줄 바꿈 테스트

## 이미지 첨부
* 파일 혹은 링크를 걸면 된다.
  * 사이즈 변경등은 img 태그를 이용

```markdown
![이름](url, "제목")
```

## 표 만들기
* 테이블 생성
```markdown
  Header1 | Header2
  ------- | -------
  Content1 | Content2
  Content3 | Content4
```

Header1 | Header2
------- | -------
Content1 | Content2
Content3 | Content4

* 테이블 정렬
``` markdown
| Col1 | Col2 | Col3 | Col4 |
| ---  | :--- | :---:| ---: |
| Default | Left | Center | Right |
```

| Col1 | Col2 | Col3 | Col4 |
| ---  | :--- | :---:| ---: |
| Default | Left | Center | Right |
