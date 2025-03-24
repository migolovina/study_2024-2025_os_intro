---
## Front matter
title: "По внешнему курсу «Введение в Linux»"
subtitle: "Операционные системы"
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

Познакомятся с операционной системой Linux и её базовыми возможностями. 


# Задание


1. Продвинутые темы
2. Текстовый редактор vim
3. Скрипты на bash: основы
4. Скрипты на bash: ветвления и циклы
5. Скрипты на bash: разное
6. Продвинутый поиск и редактирование
7. Строим графики в gnuplot
8. Разное

# Теоретическое введение


Здесь описываются теоретические аспекты, связанные с выполнением работы.
Например, в табл. 3.1 приведено краткое описание стандартных каталогов Linux.

В табл. [-@tbl:std-dir] приведено краткое описание стандартных каталогов Linux.

: Описание некоторых каталогов файловой системы GNU Linux {#tbl:std-dir}

| Имя каталога | Описание каталога                                                                                                          |
|--------------|----------------------------------------------------------------------------------------------------------------------------|
| `/`          | Корневая директория, содержащая всю файловую                                                                               |
| `bin`        | Основные системные утилиты, необходимые как в однопользовательском режиме, так и при обычной работе всем пользователям     |
| `/etc`       | Общесистемные конфигурационные файлы и файлы конфигурации установленных программ                                           |
| `/ home`     | Содержит домашние директории пользователей, которые, в свою очередь, содержат персональные настройки и данные пользователя |
| `/ root`     | Домашняя директория пользователя root                                                                                      |
|`/tmp`        | временные файлы                                                                                                            |

Более подробно об Linux см. в [1–6].

# Выполнение лабораторной работы

1. Познакомились Текстовым редактор vim и отвечаем на несколько тестовых вопросов (рис. 4.1-4.5).

![Задание 3.1.5](image/54.JPG){#fig:001 width=70%}

![Задание 3.1.7](image/55.JPG){#fig:002 width=70%}

![Задание 3.1.8](image/56.JPG){#fig:003 width=70%}

![Задание 3.1.10](image/57.JPG){#fig:004 width=70%}

![Задание 3.1.11](image/58.JPG){#fig:005 width=70%}

2. Познакомились с основами скриптов на bash и отвечаем на несколько тестовых вопросов (рис. 4.6-4.9).

![Задание 3.2.3](image/59.JPG){#fig:006 width=70%}

![Задание 3.2.5](image/60.JPG){#fig:007 width=70%}

![Задание 3.2.7](image/61.JPG){#fig:008 width=70%}

![Задание 3.2.10](image/62.JPG){#fig:009 width=70%}


3. Изучили  скрипты на bash: ветвления и циклы и отвечаем на несколько тестовых вопросов (рис. 4.10-4.14).

![Задание 3.3.3](image/63.JPG){#fig:010 width=70%}

![Задание 3.3.5](image/64.JPG){#fig:011 width=70%}

![Задание 3.3.6](image/65.JPG){#fig:012 width=70%}

![Задание 3.3.8](image/66.JPG){#fig:013 width=70%}

![Задание 3.3.9](image/67.JPG){#fig:014 width=70%}

4. Изучили  скрипты на bash: разное и отвечаем на несколько тестовых вопросов (рис. 4.15-4.20)

![Задание 3.4.3](image/68.JPG){#fig:015 width=70%}

![Задание 3.4.5](image/69.JPG){#fig:016 width=70%}

![Задание 3.4.6](image/70.JPG){#fig:017 width=70%}

![Задание 3.4.8](image/71.JPG){#fig:018 width=70%}

![Задание 3.4.9](image/72.JPG){#fig:019 width=70%}

![Задание 3.4.10](image/73.JPG){#fig:020 width=70%}

5. Изучили  продвинутый поиск и редактирование и отвечаем на несколько тестовых вопросов (рис. 4.21-4.27)

![Задание 3.5.3](image/74.JPG){#fig:021 width=70%}

![Задание 3.5.4](image/75.JPG){#fig:022 width=70%}

![Задание 3.5.5](image/76.JPG){#fig:023 width=70%}

![Задание 3.5.7](image/77.JPG){#fig:024 width=70%}

![Задание 3.5.9](image/78.JPG){#fig:025 width=70%}

![Задание 3.5.11](image/79.JPG){#fig:026 width=70%}

![Задание 3.5.12](image/80.JPG){#fig:027 width=70%}

6. Изучили построение графиков в gnuplot и отвечаем на несколько тестовых вопросов (рис. 4.28-4.31)

![Задание 3.6.3](image/81.JPG){#fig:028 width=70%}

![Задание 3.6.5](image/82.JPG){#fig:029 width=70%}

![Задание 3.6.7](image/83.JPG){#fig:030 width=70%}

![Задание 3.6.10](image/84.JPG){#fig:031 width=70%}

7. Изучили  пункт Разное и отвечаем на несколько тестовых вопросов (рис. 4.32-4.37)

![Задание 3.7.4](image/85.JPG){#fig:032 width=70%}

![Задание 3.7.5](image/86.JPG){#fig:033 width=70%}

![Задание 3.7.7](image/87.JPG){#fig:034 width=70%}

![Задание 3.7.8](image/88.JPG){#fig:035 width=70%}

![Задание 3.7.10](image/89.JPG){#fig:036 width=70%}

![Итог](image/90.JPG){#fig:037 width=70%}

# Выводы

Познакомились с операционной системой Linux и её базовыми возможностями. 

# Список литературы{.unnumbered}

1. http://rus-linux.net/  -- виртуальная энциклопедия ﻿Linux ﻿
2. ﻿http://www.f-notes.info/linux:linux_command -- довольно обширный список полезных команд терминала.
3. ﻿http://ru.najomi.org/_nix -- полезные примеры использования команд терминала
4. ﻿http://forum.ubuntu.ru/ -- форум русскоязычного сообщества Ubuntu.
5. http://ru.najomi.org/vim -- команды vim
6. ﻿http://lib.ru/LINUXGUIDE/torvalds_jast_for_fun.txt -- книга создателя Linux Линуса Торвальдса "Just for fun".

::: {#refs}
:::
