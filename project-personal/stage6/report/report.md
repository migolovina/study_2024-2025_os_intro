---
## Front matter
title: "Отчёт по индивидуальному проекту. Этап 6"
subtitle: "Размещение двуязычного сайта на Github"
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

Разместить двуязычный сайт на Github.


# Задание

1. Сделать поддержку английского и русского языков.
2. Разместить элементы сайта на обоих языках.
3. Разместить контент на обоих языках.
4. Сделать пост по прошедшей неделе.
5. Добавить пост на тему по выбору (на двух языках).


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

1. Перехожу в /work/blog/config/_default и внесла изменения в файл languages.yaml, чтобы сделать сайт на двух языках (английский и русский) (рис. 4.1).

![Изменение languages.yaml](image/1.png){#fig:001 width=70%}

2. Перехожу в /work/blog/config/_default и внесла изменения в файл hugo.yaml, чтобы сделать сайт на двух языках (английский и русский) (рис. 4.2).

![Изменение hugo.yaml](image/2.png){#fig:002 width=70%}

3. Проверила сайт на русском языке (рис. 4.3).

![Проверка](image/3.png){#fig:003 width=70%}

4. Проверила сайт на английском языке (рис. 4.4).

![Проверка](image/4.png){#fig:004 width=70%}

5. Разместила контент на английском языке (рис. 4.5).

![Посты](image/5.png){#fig:005 width=70%}

6. Разместила контент на русском языке (рис. 4.6).

![Посты](image/6.png){#fig:006 width=70%}

7. Написала пост на тему Искусственный интеллект в повседневной жизни: возможности и риски (тема по моему выбору) на русском языке (рис. 4.7).

![Изменение index.md](image/7.png){#fig:007 width=70%}

8. Написала пост на тему Искусственный интеллект в повседневной жизни: возможности и риски (тема по моему выбору) на английском языке (рис. 4.8).

![Изменение index.md](image/8.png){#fig:008 width=70%}

9. Проверила сайт на русском языке (рис. 4.9).

![Проверка](image/9.png){#fig:009 width=70%}

10. Проверила сайт на английском языке (рис. 4.10).

![Проверка](image/10.png){#fig:010 width=70%}

11. Написала пост на тему Моя прошедшая неделя на русском языке (рис. 4.11).

![Изменение index.md](image/11.png){#fig:011 width=70%}

12. Написала пост на тему Моя прошедшая неделя на английском языке (рис. 4.12).

![Изменение index.md](image/12.png){#fig:012 width=70%}

13. Проверила сайт на русском языке (рис. 4.13).

![Проверка](image/13.png){#fig:013 width=70%}

14. Проверила сайт на английском языке (рис. 4.14).

![Проверка](image/14.png){#fig:014 width=70%}

# Выводы

В ходе данной работы я создала шаблон своего сайта, а также закрепила навыки работы с системой контроля версий Git.

# Список литературы{.unnumbered}

1. [Этапы реализации проекта](https://esystem.rudn.ru/mod/page/view.php?id=970806&forceview=1)

2. [Техническая реализация проекта](https://esystem.rudn.ru/mod/page/view.php?id=970807&forceview=1)

3. [Руководство по выполнению первого этапа индивидуального проекта](https://esystem.rudn.ru/mod/url/view.php?id=980904&forceview=1)

4. [Инструменты Git - Подмодули](https://git-scm.com/book/ru/v2/%D0%98%D0%BD%D1%81%D1%82%D1%80%D1%83%D0%BC%D0%B5%D0%BD%D1%82%D1%8B-Git-%D0%9F%D0%BE%D0%B4%D0%BC%D0%BE%D0%B4%D1%83%D0%BB%D0%B8)

::: {#refs}
:::
