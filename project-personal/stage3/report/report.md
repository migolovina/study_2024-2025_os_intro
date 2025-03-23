---
## Front matter
title: "Отчёт по индивидуальному проекту. Этап 3"
subtitle: "Добавить к сайту достижения"
author: "Головина Мария Игоревна"

## Generic otions
lang: ru-RU
toc-title: "Содержание"

## Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

## Pdf output format
toc: true # Table of contents
toc-depth: 2
lof: true # List of figures
lot: true # List of tables
fontsize: 12pt
linestretch: 1.5
papersize: a4
documentclass: scrreprt
## I18n polyglossia
polyglossia-lang:
  name: russian
  options:
	- spelling=modern
	- babelshorthands=true
polyglossia-otherlangs:
  name: english
## I18n babel
babel-lang: russian
babel-otherlangs: english
## Fonts
mainfont: IBM Plex Serif
romanfont: IBM Plex Serif
sansfont: IBM Plex Sans
monofont: IBM Plex Mono
mathfont: STIX Two Math
mainfontoptions: Ligatures=Common,Ligatures=TeX,Scale=0.94
romanfontoptions: Ligatures=Common,Ligatures=TeX,Scale=0.94
sansfontoptions: Ligatures=Common,Ligatures=TeX,Scale=MatchLowercase,Scale=0.94
monofontoptions: Scale=MatchLowercase,Scale=0.94,FakeStretch=0.9
mathfontoptions:
## Biblatex
biblatex: true
biblio-style: "gost-numeric"
biblatexoptions:
  - parentracker=true
  - backend=biber
  - hyperref=auto
  - language=auto
  - autolang=other*
  - citestyle=gost-numeric
## Pandoc-crossref LaTeX customization
figureTitle: "Рис."
tableTitle: "Таблица"
listingTitle: "Листинг"
lofTitle: "Список иллюстраций"
lotTitle: "Список таблиц"
lolTitle: "Листинги"
## Misc options
indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Создать свой сайт (Добавить к сайту достижения.).


# Задание

1. Добавить информацию о навыках (Skills).
2. Добавить информацию об опыте (Experience).
3. Добавить информацию о достижениях (Accomplishments).
4. Сделать пост по прошедшей неделе.
5. Сделать пост по языку разметки Markdown.

# Теоретическое введение

Примеры использования git:

1. Система контроля версий Git представляет собой набор программ командной строки. 
Доступ к ним можно получить из терминала посредством ввода команды git с различными опциями.

2. Благодаря тому, что Git является распределённой системой контроля версий, резервную копию локального хранилища можно сделать простым копированием или архивацией.
Основные команды git:

Например, в табл. @tbl:std-dir приведено краткое описание основных команд Git.

: Описание некоторых команд системы контроля версий Git {#tbl:std-dir}

| Команда | Описание команды                                                                  |
|--------------|-----------------------------------------------------------------------------------|
| git init     | Создание основного дерева репозитория  |
| git pull     | Получение обновлений(изменений текущего дерева из центрального репозитория |
| git push     | Отправка всех произведённых изменений локального дерева в центральный репозиторий |
| git status   | Просмотр списка изменённых файлов в текущей директории |
| git diff     | Просмотр текущих изменений  |
| git add .    | Добавление все изменённые и/или созданные файлы и/или каталоги |
| git rm имена_файлов | Удаление файлов и/или каталогов из индекса репозитория |
| git commit -am 'Описание коммита'| Сохранение всех добавленных изменений и всех изменённых файлов |
| git commit   | Сохранение добавленный изменений с внесением комментария через встроенный редактор |
| git checkout -b имя_ветки | Создание новой ветки, базирующейся на текущей | 
| git branch -d имя_ветки | Удаление локальной уже слитой с основным деревом ветки |
| git branch -D имя_ветки | Принудительное удаление локальной ветки |


Полный список команд можно посмотреть на официальном сайте: [Github.com](https://docs.github.com/en/get-started/using-github/github-command-palette)


# Выполнение индивидуального проекта

1. Перехожу в /work/blog/content/authors/admin и заполняю графу Experience (рис. 4.1).

![Заполнила графу Experience](image/1.png){#fig:001 width=70%}

2. Перехожу на свой сайт и проверяю графу Experience (рис. 4.2).

![Вид графы Experience на сайте](image/2.png){#fig:002 width=70%}

3. Перехожу в /work/blog/content/authors/admin и заполняю графу Skills, Hobbies (рис. 4.3).

![Заполнила графу Skills, Hobbies](image/3.png){#fig:003 width=70%}

4. Перехожу на свой сайт и проверяю графу Skills, Hobbies (рис. 4.4).

![Вид графы Skills, Hobbies на сайте](image/4.png){#fig:004 width=70%}

5. Перехожу в /work/blog/content/authors/admin и заполняю графу Accomplishments (рис. 4.5).

![Заполнила графу Accomplishments](image/5.png){#fig:005 width=70%}

6. Перехожу на свой сайт и проверяю графу Accomplishments (рис. 4.6).

![Вид графы Accomplishments на сайте](image/6.png){#fig:006 width=70%}

7. Теперь я перехожу в /work/blog/content/post/last-week-8 и загружаю туда свою фотографию с прошедшей недели, а также буду изменять информацию в index.md (рис. 4.7).

![Размещение фотографии с прошедшей недели](image/7.png){#fig:007 width=70%}

8. Добавила в файл index.md название поста, дату, краткое описание, автора, тэги, информацию откуда я взяла фотографию и основное содержание поста (рис. 4.8).

![Изменение index.md](image/8.png){#fig:008 width=70%}

9. Перехожу на свой сайт и проверяю свой пост (рис. 4.9)

![Пост по прошедшей недели](image/9.png){#fig:009 width=70%}

10. Теперь я перехожу в /work/blog/content/post/markdown и загружаю туда фотографию, подходящую к этому посту, а также буду изменять информацию в index.md (рис. 4.10).

![Размещение фотографии, подходящей к этому посту](image/10.png){#fig:010 width=70%}

11. Добавила в файл index.md название поста, дату, краткое описание, автора, тэги, информацию откуда я взяла фотографию и основное содержание поста (рис. 4.11-4.12).

![Изменение index.md](image/11.png){#fig:011 width=70%}

![Изменение index.md](image/12.png){#fig:012 width=70%}

12. Перехожу на свой сайт и проверяю свой пост (рис. 4.13)

![Пост по язык разметки Markdown](image/13.png){#fig:013 width=70%}

# Выводы

В ходе данной работы я создала шаблон своего сайта, который в будущем буду дорабатывать, а также закрепила навыки работы с системой контроля версий Git.

# Список литературы{.unnumbered}

1. [Этапы реализации проекта](https://esystem.rudn.ru/mod/page/view.php?id=970806&forceview=1)

2. [Техническая реализация проекта](https://esystem.rudn.ru/mod/page/view.php?id=970807&forceview=1)

3. [Руководство по выполнению первого этапа индивидуального проекта](https://esystem.rudn.ru/mod/url/view.php?id=980904&forceview=1)

4. [Инструменты Git - Подмодули](https://git-scm.com/book/ru/v2/%D0%98%D0%BD%D1%81%D1%82%D1%80%D1%83%D0%BC%D0%B5%D0%BD%D1%82%D1%8B-Git-%D0%9F%D0%BE%D0%B4%D0%BC%D0%BE%D0%B4%D1%83%D0%BB%D0%B8)

::: {#refs}
:::
