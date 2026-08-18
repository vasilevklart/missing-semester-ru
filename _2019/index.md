---
layout: page
title: "Лекции 2019"
description: >
  Конспекты и видео лекций курса Missing Semester, MIT IAP 2019.
permalink: /2019/
phony: true
---

{% assign lecture_date = site['2019'] | group_by: 'date' | sort: 'name' %}
{% for date in lecture_date %}
  {% if date.name == "" %}{% continue %}{% endif %}
  {% assign wd = date.name | date: '%u' %}
  {% case wd %}
    {% when '1' %}{% assign wd_ru = 'Понедельник' %}
    {% when '2' %}{% assign wd_ru = 'Вторник' %}
    {% when '3' %}{% assign wd_ru = 'Среда' %}
    {% when '4' %}{% assign wd_ru = 'Четверг' %}
    {% when '5' %}{% assign wd_ru = 'Пятница' %}
    {% when '6' %}{% assign wd_ru = 'Суббота' %}
    {% else %}{% assign wd_ru = 'Воскресенье' %}
  {% endcase %}
  <h2>{{ wd_ru }}, {{ date.name | date: '%-d.%-m' }}</h2>
  {% assign lectures = date.items | sort: 'order' %}
  <ul>
  {% for lecture in lectures %}
    {% if lecture.phony != true %}
      <li>
        <a href="{{ lecture.url }}">{{ lecture.title }}</a>
      </li>
    {% endif %}
  {% endfor %}
  </ul>
{% endfor %}

# За пределами MIT

Мы делимся этим курсом и за пределами MIT в надежде, что эти материалы пригодятся и другим. Публикации и обсуждения можно найти на

- [Hacker News](https://news.ycombinator.com/item?id=19078281)
- [Lobsters](https://lobste.rs/s/h6157x/mit_hacker_tools_lecture_series_on)
- [r/learnprogramming](https://www.reddit.com/r/learnprogramming/comments/an42uu/mit_hacker_tools_a_lecture_series_on_programmer/)
- [r/programming](https://www.reddit.com/r/programming/comments/an3xki/mit_hacker_tools_a_lecture_series_on_programmer/)
- [Twitter](https://twitter.com/Jonhoo/status/1091896192332693504)
- [YouTube](https://www.youtube.com/playlist?list=PLyzOVJj3bHQuiujH1lpn8cA9dsyulbYRv)

# Благодарности

Этот курс проводился в рамках [SIPB IAP 2019](https://sipb.mit.edu/iap/2019/) при совместной поддержке [SIPB](https://sipb.mit.edu/) и [MIT EECS](https://www.eecs.mit.edu/).
