---
layout: page
title: Пропущенный семестр вашего CS-образования
description: >
  Освойте мощные инструменты, которые сделают вас более продуктивным специалистом по computer science и программистом.
# subtitle: IAP 2026
subtitle: "2026"
nositetitle: true
---

Учебные курсы рассказывают о продвинутых темах computer science – от операционных
систем до машинного обучения, – но есть один критически важный предмет, который
почти никогда не преподают, а оставляют студентам осваивать самостоятельно:
умение владеть своими инструментами. Мы научим вас уверенно работать в командной
строке, пользоваться мощным текстовым редактором, применять продвинутые
возможности систем контроля версий и многому другому!

За время учёбы студенты проводят с этими инструментами сотни часов (а за карьеру –
тысячи), поэтому имеет смысл сделать эту работу максимально гладкой и
комфортной. Владение инструментами не только позволяет тратить меньше времени на
попытки подчинить их своей воле, но и даёт возможность решать задачи, которые
раньше казались невозможно сложными.

Сегодня многие стороны разработки ПО к тому же меняются с появлением инструментов
и рабочих процессов на основе ИИ или дополненных ИИ. При уместном использовании и
понимании их недостатков они часто приносят специалистам по CS ощутимую пользу,
а значит, стоит выработать практические навыки работы с ними. Поскольку ИИ –
сквозная вспомогательная технология, отдельной лекции про ИИ нет; вместо этого мы
встроили использование новейших применимых ИИ-инструментов и приёмов прямо в
каждую лекцию.

Прочитайте о [мотивации создания этого курса]({{ site.baseurl }}/about/).

{% comment %}
# Registration

Sign up for the IAP 2026 class by filling out this [registration form](https://forms.gle/j2wMzi7qeiZmzEWy9).
{% endcomment %}

# Программа

{% comment %}
**Lecture**: [35-225](https://whereis.mit.edu/?go=35), 1:30--2:30pm (_exception_: 3--4pm on Friday 1/16)<br>
**Discussion**: [OSSU Discord](https://ossu.dev/#community) (use `#missing-semester-forum` like you would use Piazza, and `#missing-semester` to chat with the class/instructors)
{% endcomment %}

<ul>
{% assign lectures = site['2026'] | sort: 'date' %}
{% for lecture in lectures %}
    {% if lecture.phony != true %}
        <li>
        <strong>{{ lecture.date | date: '%-d.%-m.%y' }}</strong>:
        {% if lecture.ready %}
            <a href="{{ lecture.url | relative_url }}">{{ lecture.title }}</a>
        {% else %}
            {{ lecture.title }} {% if lecture.noclass %}[занятия нет]{% endif %}
        {% endif %}
        </li>
    {% endif %}
{% endfor %}
</ul>

## Специальные темы прошлых лет

Набор тем от года к году меняется. Для тех, кому интересен полный набор тем,
которые мы освещали за все годы, мы выделяем темы прошлых лет, не вошедшие в
программу 2026 года.

{% comment %} pop to remove default "posts" collection {% endcomment %}
{% assign sorted_collections = site.collections | sort: 'label' | pop | reverse %}
<ul>
{% for collection in sorted_collections %}
    {% assign grouped_lectures = site[collection.label] | group_by: 'date' | sort: 'name' %}
    {% for group in grouped_lectures %}
        {% assign sorted_lectures = group.items | sort: 'order' %}
        {% for lecture in sorted_lectures %}
            {% if lecture.special == true %}
                <li>
                    <strong>{{ lecture.date | date: '%-d.%-m.%y' }}</strong>:
                    <a href="{{ lecture.url | relative_url }}">{{ lecture.title }}</a>
                </li>
            {% endif %}
        {% endfor %}
    {% endfor %}
{% endfor %}
</ul>

{% comment %}
Lecture videos will be made available to MIT students immediately after lecture (via Panopto). The system has a limitation that only those with an MIT Kerberos can access the raw lecture videos. We are working on editing lecture videos and uploading them to YouTube. A couple have been uploaded already; we expect the rest to be uploaded by mid-February.

If you can't wait until January 2026, you can also take a look at the lectures
from the [previous offering of the course]({{ site.baseurl }}/2020/), which covers many of the
same topics.
{% endcomment %}

# Общая информация

**Преподаватели**: курс совместно ведут [Anish](https://anish.io/), [Jon](https://thesquareplanet.com/) и [Jose](https://josejg.com/).<br>
**Вопросы**: пишите нам на [missing-semester@mit.edu](mailto:missing-semester@mit.edu).<br>
**Обсуждение**: [Discord OSSU](https://ossu.dev/#community) (канал `#missing-semester-forum` используйте как Piazza, а `#missing-semester` – для общения с группой и преподавателями).

# За пределами MIT

Мы делимся этим курсом и за пределами MIT в надежде, что эти материалы пригодятся
и другим. Публикации и обсуждения можно найти на

 - Hacker News ([2026](https://news.ycombinator.com/item?id=47124171), [2020](https://news.ycombinator.com/item?id=22226380), [2019](https://news.ycombinator.com/item?id=19078281))
 - Lobsters ([2026](https://lobste.rs/s/q4ykw7/missing_semester_your_cs_education_2026), [2020](https://lobste.rs/s/ti1k98/missing_semester_your_cs_education_mit), [2019](https://lobste.rs/s/h6157x/mit_hacker_tools_lecture_series_on))
 - r/learnprogramming ([2026](https://www.reddit.com/r/learnprogramming/comments/1r93yk6/the_missing_semester_of_your_cs_education_2026/), [2020](https://www.reddit.com/r/learnprogramming/comments/eyagda/the_missing_semester_of_your_cs_education_mit/), [2019](https://www.reddit.com/r/learnprogramming/comments/an42uu/mit_hacker_tools_a_lecture_series_on_programmer/))
 - r/programming ([2020](https://www.reddit.com/r/programming/comments/eyagcd/the_missing_semester_of_your_cs_education_mit/), [2019](https://www.reddit.com/r/programming/comments/an3xki/mit_hacker_tools_a_lecture_series_on_programmer/))
 - X ([2026](https://x.com/anishathalye/status/2024521145777848588), [2020](https://twitter.com/jonhoo/status/1224383452591509507), [2019](https://x.com/jonhoo/status/1090323977766137858))
 - Bluesky ([2026](https://bsky.app/profile/jonhoo.eu/post/3mfa2bhyuj22i))
 - Mastodon ([2026](https://fosstodon.org/@jonhoo/116098318361854057))
 - LinkedIn ([2026](https://www.linkedin.com/posts/anishathalye_i-returned-to-mit-during-iap-january-term-activity-7430285026933522433-Ehr9))
 - YouTube ([2026](https://www.youtube.com/playlist?list=PLyzOVJj3bHQunmnnTXrNbZnBaCA-ieK4L), [2020](https://www.youtube.com/playlist?list=PLyzOVJj3bHQuloKGG59rS43e29ro7I57J), [2019](https://www.youtube.com/playlist?list=PLyzOVJj3bHQuiujH1lpn8cA9dsyulbYRv))

# Переводы

{% comment %} keep these in alphabetical order {% endcomment %}

- [Английский (оригинал)](https://missing.csail.mit.edu/)
- [Арабский](https://missing-semester-ar.github.io/)
- [Бенгальский](https://missing-semester-bn.github.io/)
- [Вьетнамский](https://missing-semester-vn.github.io/)
- [Испанский](https://missing-semester-esp.github.io/)
- [Итальянский](https://missing-semester-it.github.io/)
- [Каннада](https://missing-semester-kn.github.io/)
- [Китайский (упрощённый)](https://missing-semester-cn.github.io/)
- [Китайский (традиционный, Тайвань)](https://missing-semester-tw.github.io/)
- [Корейский](https://missing-semester-kr.github.io/)
- [Монгольский](https://missing-semester-mn.github.io)
- [Немецкий](https://missing-semester-de.github.io/)
- [Персидский](https://missing-semester-fa.github.io/)
- [Португальский](https://missing-semester-pt.github.io/)
- [Сербский](https://netboxify.com/missing-semester/)
- [Тайский](https://missing-semester-th.github.io/)
- [Турецкий](https://missing-semester-tr.github.io/)
- [Шведский](https://den-saknade-terminen.l10n.se/)
- [Японский](https://missing-semester-jp.github.io/)

Примечание: это внешние ссылки на переводы, сделанные сообществом. Авторы курса
их не проверяли. Этот сайт – русский перевод сообщества; оригинал находится по
адресу [missing.csail.mit.edu](https://missing.csail.mit.edu/).

Сделали перевод конспектов этого курса? Отправьте [pull request](https://github.com/missing-semester/missing-semester/pulls)
в оригинальный репозиторий, чтобы его добавили в список!

## Благодарности

{% comment %}
2026 acks; previous years' acks are on their respective pages
{% endcomment %}

Мы благодарим Elaine Mello и [MIT Open Learning](https://openlearning.mit.edu/) за возможность записать видео лекций. Мы благодарим Luis Turino / [SIPB](https://sipb.mit.edu/) за поддержку курса в рамках [SIPB IAP 2026](https://sipb.mit.edu/iap/).

---

<div class="small center">
<p><a href="https://github.com/missing-semester-rus/missing-semester-rus.github.io">Исходный код перевода</a> · <a href="https://github.com/missing-semester/missing-semester">исходный код оригинала</a>.</p>
<p>Лицензия CC BY-NC-SA.</p>
<p><a href="{{ site.baseurl }}/license/">Правила</a> участия и перевода.</p>
</div>
