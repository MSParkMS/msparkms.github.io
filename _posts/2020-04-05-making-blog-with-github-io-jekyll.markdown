---
layout: post
title: "Github.io + Jekyll로 블로그 만들기"
date: 2020-04-05 13:38:08 +0900
categories: [Blog]
---

# Github.io + Jekyll로 블로그 만들기

## 개요
* Github.io에 개인 프로젝트 & 공부 블로그를 만들고 싶다.
* 찾아보니 Jekyll을 이용하여 만든다고 한다.
* 어떻게 만드는지 간단하게 정리해보자.

## Github.io
* Github Pages를 이용하여 개인 프로젝트 웹사이트를 만들 수 있다.
    * [Github Pages](https://pages.github.com/ "Github Pages")
    * 위에 링크에 나온대로만 만들어주면 금방 페이지가 완성된다.
<p></p>
* 만드는 방법
    1. repository를 만들어준다.
        * username.github.io를 이름으로한 repository를 만들어준다.
    2. 만들어진 repository를 clone 해온다.
    3. 만들어진 repository 폴더에 들어가 index.html 파일을 하나 만들어준다.
    4. commit, push 하고 https://username.github.io 에 접속해본다.

## Jekyll
* Github Pages에 보면 Jekyll을 이용해서 만드는 법이 나와있다.
    * [Jekyll](https://help.github.com/en/github/working-with-github-pages/creating-a-github-pages-site-with-jekyll "Jekyll")
    * [Jekyll Installation](https://jekyllrb.com/docs/installation/windows/ "Jekyll Installation")
<p></p>
* 설치방법
    1. 내 환경은 Windows이므로 RubyInstaller를 다운 받는다.
    2. 설치 후 `ridk install`
    3. `gem install jekyll bundler`
    4. `jekyll -v` 로 설치된 버전을 확인해본다.
<p></p>
* 사이트 생성
    1. 위에서 만들어진 repository 폴더에 간다.
    2. `jekyll new .`
        * 내 경우에는 index.html을 하나 올려놓은 상태여서 빈 폴더가 아니니까 생성하려면 --force 옵션을 넣으라고 해서 넣어줌
    3. 생성이 완료되면 Gemfile을 열어서 Github Pages일 경우에는 하라는 대로 한다.
        * 위에 Jekyll을 주석처리하고 아래 github-pages를 주석해제하라고 적혀있다.
    4. `bundle exec jekyll serve`를 실행하여 로컬에서 빌드할 수 있게 한다.
        * markdown을 수정하면 바로 빌드해서 적용된다.
        * localhost:4000에 접속하면 볼 수 있다.
<p></p>
* 기본 수정
    1. _config.yml에 정보들을 내 정보로 변경해준다.
    2. about.markdown을 내 사이트에 맞게 수정한다.
    3. 기본적으로 _post에 만들어져있는 markdown을 내 post로 변경해준다.
        * YEAR-MONTH-DAY-Title.markdown 이름으로 파일을 만들어야 한다.
        * 미래 시점의 날짜를 입력할 경우 따로 옵션을 주지 않는 한은 빌드가 되지 않는다.
<p></p>
* 카테고리 추가
    1. _layouts 폴더 추가
    2. _layouts > category.html 추가
    3. _includes 폴더 추가
    4. _includes > index.html 추가
    5. category 폴더 추가
    6. category > 추가하고자 하는 카테고리이름.markdown 추가 (ex> Blog.markdown)
    7. post의 markdown에 categories : [카테고리이름] 추가
        * 자세한 내용은 아래 링크를 참고 (코드 블럭에 일부 코드가 나오지 않아서 일단 링크로)
        * [참고 사이트](https://devyurim.github.io/development%20environment/github%20blog/2018/08/07/blog-6.html "참고 사이트")