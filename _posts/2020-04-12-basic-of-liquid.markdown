---
layout: default
title: "Liquid 문법 기초"
date: 2020-04-12 05:57:04 +0900
categories: [Blog]
---
# Liquid 문법 기초
## Liquid
* Jekyll을 잘 활용하려면 Liquid 문법을 알아둘 필요가 있다.
* 그래야 내 마음대로 커스텀하게 사용할 수 있다.

## 문법 기초
* [참고 사이트](https://jekyllrb-ko.github.io/docs/step-by-step/02-liquid/)
{% raw %}
* 맨 위에 --- / --- 로 머리말부분을 만들어주어야 동작한다.
    * 머리말에 추가해준 변수는 page를 통해 접근할 수 있다.
{% endraw %} 

### 오브젝트
{% raw %}
* 컨텐츠를 어디에 출력할 것인가를 알려준다. {{ }} 를 이용한다.
```liquid
{{ page.title }}
```
{% endraw %}
* 테스트
    * {{ page.title }}

### 태그
{% raw %}
* 탬플릿의 논리 연산과 흐름을 제어한다. {% %} 를 이용한다.
```liquid
{% if page.show_sidebar %}
    <div class="sidebar">
        sidebar content
    </div>
{% endif %}
```
{% endraw %}
* 참고로 코드블럭등 안에서도 liquid 문법이 동작한다.
    * 그래서 liquid 문법이 동작하지 않기를 원한다면 그 사이에 태그를 추가해야 한다.
    {% raw %}
    * {% %} -> raw / endraw
    {% endraw %}
    * 이 부분도 이쁘게 나타낼 수 있을 것 같은데 아직은 잘 모르곘음

### 필터
{% raw %}
* liquid 오브젝트의 출력을 변화시킨다. | 를 이용한다.
```liquid
{{ "hi" | capitalize }}
{{ "Hello World!" | downcase }}
```
{% endraw %}
* 테스트
    * {{ "hi" | capitalize }}
    * {{ "Hello World!" | downcase }}