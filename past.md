---
layout: page
title: Прошлые выпуски
description: >
  Здесь собраны все прошлые выпуски «Пропущенного семестра».
---

{% comment %} pop to remove default "posts" collection {% endcomment %}
{% assign sorted_collections = site.collections | sort: 'label' | pop | reverse %}
<ul>
{% for collection in sorted_collections %}
    <li><a href="{{ site.baseurl }}/{{ collection.label }}/">{{ collection.label }}</a></li>
{% endfor %}
</ul>

Лекции каждого года полностью самодостаточны. Мы рекомендуем начинать с самой свежей версии материала. Набор тем от года к году меняется, поэтому мы продолжаем размещать конспекты и видео более ранних версий этого курса.
