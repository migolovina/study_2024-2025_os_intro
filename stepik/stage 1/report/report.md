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


1. Введение
2. Общая информация о курсе
3. Как установить Linux
4. Осваиваем Linux
5. Terminal: основы
6. Запуск исполняемых файлов
7. Ввод / вывод
8. Скачивание файлов из интернета
9. Работа с архивами
10. Поиск файлов и слов в файлах

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

1. Рассматриваем общую информацию о курсе и отвечаем на несколько тестовых вопросов (рис. 4.1-4.2).

![Задание 1.1.3](image/1.JPG){#fig:001 width=70%}

![Задание 1.1.5](image/2.JPG){#fig:002 width=70%}


2. Рассматриваем способы установки Linux и отвечаем на несколько тестовых вопросов (рис. 4.3-4.5). 


![Задание 1.2.6](image/3.JPG){#fig:003 width=70%}

![Задание 1.2.8](image/4.JPG){#fig:004 width=70%}

![Задание 1.2.10](image/5.JPG){#fig:005 width=70%}


3. Осваиваем Linux и отвечаем на несколько тестовых вопросов (рис. 4.6-4.9). 

![Задание 1.3.4](image/6.JPG){#fig:006 width=70%}

![Задание 1.3.6](image/7.JPG){#fig:007 width=70%}

![Задание 1.3.8](image/8.JPG){#fig:008 width=70%}

![Задание 1.3.10](image/9.JPG){#fig:009 width=70%}

4. Запускаем Terminal, а также изучаем несколько базовых команд для работы в нём и отвечаем на несколько тестовых вопросов (рис. 4.10-4.14).

![Задание 1.4.3](image/10.JPG){#fig:010 width=70%}

![Задание 1.4.5](image/11.JPG){#fig:011 width=70%}

![Задание 1.4.7](image/12.JPG){#fig:012 width=70%}

![Задание 1.4.10](image/13.JPG){#fig:013 width=70%}

![Задание 1.4.12](image/14.JPG){#fig:014 width=70%}

5. Рассмотрели запуск исполняемых файлов и отвечаем на несколько тестовых вопросов (рис. 4.15-4.17).

![Задание 1.5.3](image/15.JPG){#fig:015 width=70%}

![Задание 1.5.6](image/16.JPG){#fig:016 width=70%}

![Задание 1.5.7](image/17.JPG){#fig:017 width=70%}

6. Рассмотрели ввод/вывод и отвечаем на несколько тестовых вопросов (рис. 4.18-4.20).

![Задание 1.6.4](image/18.JPG){#fig:018 width=70%}

![Задание 1.6.5](image/19.JPG){#fig:019 width=70%}

![Задание 1.6.8](image/20.JPG){#fig:020 width=70%}

7. Рассмотрели скачивание файлов из интернета и отвечаем на несколько тестовых вопросов (рис. 4.21-4.23).

![Задание 1.7.3](image/21.JPG){#fig:021 width=70%}

![Задание 1.7.5](image/22.JPG){#fig:022 width=70%}

![Задание 1.7.7](image/23.JPG){#fig:023 width=70%}

8. Рассмотрели работу с архивами и отвечаем на несколько тестовых вопросов (рис. 4.24-4.26).

![Задание 1.8.3](image/24.JPG){#fig:024 width=70%}

![Задание 1.8.5](image/25.JPG){#fig:025 width=70%}

![Задание 1.8.7](image/26.JPG){#fig:026 width=70%}

9. Рассмотрели способы поиска файлов и слов и отвечаем на несколько тестовых вопросов (рис. 4.27-4.29).

![Задание 1.9.3](image/27.JPG){#fig:027 width=70%}

![Задание 1.9.5](image/28.JPG){#fig:028 width=70%}

![Задание 1.9.6](image/29.JPG){#fig:029 width=70%}


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
