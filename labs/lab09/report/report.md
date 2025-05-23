---
## Front matter
title: "Лабораторная работа 9"
subtitle: "Командная оболочка Midnight Commander"
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

Освоение основных возможностей командной оболочки Midnight Commander. Приобретение навыков практической работы по просмотру каталогов и файлов; манипуляций с ними.

# Задание

1. Изучите информацию о mc, вызвав в командной строке man mc. 
2. Запустите из командной строки mc, изучите его структуру и меню.
3. Выполните несколько операций в mc, используя управляющие клавиши (операции с панелями; выделение/отмена выделения файлов, копирование/перемещение файлов, получение информации о размере и правах доступа на файлы и/или каталоги и т.п.) 
4. Выполните основные команды меню левой (или правой) панели. Оцените степень подробности вывода информации о файлах. 
5. Используя возможности подменю Файл, выполните: 

– просмотр содержимого текстового файла; 

– редактирование содержимого текстового файла (без сохранения результатов редактирования); – создание каталога; 

– копирование в файлов в созданный каталог. 

6. С помощью соответствующих средств подменю Команда осуществите: 

– поиск в файловой системе файла с заданными условиями (например, файла с расширением .c или .cpp, содержащего строку main); 

– выбор и повторение одной из предыдущих команд; 

– переход в домашний каталог; 

– анализ файла меню и файла расширений. 

7. Вызовите подменю Настройки. Освойте операции, определяющие структуру экрана mc (Full screen, Double Width, Show Hidden Files и т.д.).

Задание по встроенному редактору mc

1. Создайте текстовой файл text.txt. 
2. Откройте этот файл с помощью встроенного в mc редактора. 
3. Вставьте в открытый файл небольшой фрагмент текста, скопированный из любого другого файла или Интернета. 
4. Проделайте с текстом следующие манипуляции, используя горячие клавиши: 

4.1. Удалите строку текста. 

4.2. Выделите фрагменттекста и скопируйте его на новую строку.

4.3. Выделите фрагменттекста и перенесите его на новую строку. 

4.4. Сохраните файл. 

4.5. Отмените последнее действие. 

4.6. Перейдите в конец файла (нажав комбинацию клавиш) и напишите некоторый текст. 

4.7. Перейдите в начало файла (нажав комбинацию клавиш) и напишите некоторый текст. 

4.8. Сохраните и закройте файл. 

5. Откройте файл с исходным текстом на некотором языке программирования (например C или Java) 
6. Используя меню редактора, включите подсветку синтаксиса, если она не включена, или выключите, если она включена.
7. Ответить на контрольные вопросы.


# Теоретическое введение

Командная оболочка — интерфейс взаимодействия пользователя с операционной системой и программным обеспечением посредством команд. Midnight Commander (или mc)—псевдографическая командная оболочкадля UNIX/Linux систем. Для запуска mc необходимо в командной строке набрать mc и нажать Enter . Рабочее пространство mc имеет две панели, отображающие по умолчанию списки файлов двух каталогов.
Над панелями располагается меню, доступ к которому осуществляется с помощью клавиши F9 . Под панелями внизу расположены управляющие экранные кнопки, ассоциированные с функциональными клавишами F1 – F10. .Над ними располагается командная строка, предназначенная для ввода команд.
Функциональные клавиши mc:

F1 Вызов контекстно-зависимой подсказки

F2 Вызов пользовательского меню с возможностью создания и/или дополнения дополнительных функций 

F3 Просмотр содержимого файла, на который указывает подсветка в активной панели (без возможности редактирования) 

F4 Вызов встроенного в mc редактора для изменения содержания файла, на который указывает подсветка в активной панели

F5 Копирование одного или нескольких файлов, отмеченных в первой (активной) панели, в каталог, отображаемый на второй панели 

F6 Перенос одного или нескольких файлов, отмеченных в первой (активной) панели, в каталог, отображаемый на второй панели 

F7 Создание подкаталога в каталоге, отображаемом в активной панели 

F8 Удаление одного или нескольких файлов (каталогов), отмеченных впервой (активной) панели файлов 

F9 Вызов меню mc

F10 Выход из mc

Более подробно об Linux см. в [1–7].

# Выполнение лабораторной работы

1. Изучили информацию о mc, вызвав в командной строке man mc (рис 4.1).

![man mc](image/1.JPG){#fig:001 width=70%}

2. Запустили из командной строки mc и изучили структуру (рис. 4.2).

![Структура mc](image/2.JPG){#fig:002 width=70%}

3.  Переместили и скопировали файлы с помощью управляющих клавиш. (рис. 4.3-4.4).

![Копирование файла](image/3.JPG){#fig:003 width=70%}

![Перемещение файла](image/4.JPG){#fig:004 width=70%}

4. Попробовали команды из левой панели (рис. 4.5-4.7).

![Информация о файлах](image/5.JPG){#fig:005 width=70%}

![Дерево каталогов](image/6.JPG){#fig:006 width=70%}

![Содержимое файлов](image/7.JPG){#fig:007 width=70%}

5. Использовали возможности меню “Файл” и выполнили следующие команды (рис. 4.8-4.11):

![Просмотр содержимого файла](image/8.JPG){#fig:008 width=70%}

![Редактирование файла](image/9.JPG){#fig:009 width=70%}

![Создание каталога 123](image/10.JPG){#fig:010 width=70%}

![Копирование файлов в созданный каталог](image/11.JPG){#fig:011 width=70%}

6. С помощью соответствующих средств подменю Команда осуществили необходимые действия (рис. 4.12-4.16).

![Поиск файлов с расширением .c](image/12.JPG){#fig:012 width=70%}

![Поиск с расширением .ccp](image/13.JPG){#fig:013 width=70%}

![Выбор одного из предыдущих действий](image/14.JPG){#fig:014 width=70%}

![Анализ меню](image/15.JPG){#fig:015 width=70%}

![Анализ расширения](image/16.JPG){#fig:016 width=70%}

7. Вызвали подменю Настройки. Освоили операции, определяющие структуру экрана mc (рис. 4.17).

![Подменю “Настройки”](image/17.JPG){#fig:017 width=70%}

8. Создали текстовой файл text.txt (рис. 4.18).

![Файл text.txt](image/18.JPG){#fig:018 width=70%}

9. Открыли этот файл с помощью встроенного в mc редактора (рис.4.19).

![Открытие файла](image/19.JPG){#fig:019 width=70%}

10. Вставили в открытый файл небольшой фрагмент текста. Я в качестве текста вставила список литературы из лабораторной работы (рис. 4.20).

![Текст файла](image/20.JPG){#fig:020 width=70%}

11. Удалили строку текста с помощью клавиши F8 (рис. 4.21).

![Удаление строки](image/21.JPG){#fig:021 width=70%}

12. Выделили фрагмент и скопировали с помощью клавиши F5 (рис. 4.22).

![Копирование строки](image/22.JPG){#fig:022 width=70%}

13. Выделили фрагмент и перенесли на новую строку с помощью клавиши enter (рис. 4.23).

![Перенос строки](image/23.JPG){#fig:023 width=70%}

14. Сохранили файл (рис. 4.24).

![Сохранение файла](image/24.JPG){#fig:024 width=70%}

15. Отменили последнее действие с помощью комбинации ctrl+u. Перешли в конец текста с помощью комбинации ctrl+end и написали свое имя (рис. 4.25).

![Добавление текста в конец файла](image/25.JPG){#fig:025 width=70%}

16. Перешли в начало файла с помощью комбинации ctrl+home и написали свою фамилию (рис. 4.26).

![Добавление текста в начало файла](image/26.JPG){#fig:026 width=70%}

17. Сохранили и закрыли файл (рис. 4.27).

![Сохранение файла](image/27.JPG){#fig:027 width=70%}

18. Использую меню редактора, отключили подстветку синтаксиса (рис.4.28).

![Подстветка синтаксиса](image/28.JPG){#fig:028 width=70%}

# Ответы на контрольные вопросы

1. Какие режимы работы есть в mc. Охарактеризуйте их.
mc - визуальная файловая оболочка для UNIX/Linux систем, аналог Far, Norton Commander, но оболочки в Linux несравненно богаче. На языке командной оболочки можно писать небольшие программы для выполнения ряда последовательных операций с файлами и содержащимися в них данными. Команда Переставить панели(Ctrl+U) меняет местами содержимое правой и левой панелей. Команде Отключить панели (Ctrl+O). По команде Сравнить каталоги (Ctrl-X,D) сравнивается содержимое каталогов, отображаемых на левой и правой панелях. Помимо того, что может задаваться формат вывода на панель списка файлов,любую панель можно перевести в один из следующих режимов:

Режим “Информация”. В этом режиме на панель выводится информация о подсвеченном в другой панели файле и о текущей файловой системе.

Режим“Дерево”.В режиме отображения дерева каталогов в одной из панелей выводится графическое изображение структуры дерева каталогов. Этот режим подобен тому, который вы увидите, выбрав команду Дерево каталогов из меню Команды, только в последнем случае изображение структуры каталогов выводится в отдельное окно. Левая Панель и Правая Панель меню (левой/правой панели) позволяют оперировать режимами отображения панелей. Меню Левая Панель и Правая Панель позволяют оперировать панелями. Формат списка бывает:

Стандартный – вывод списка файлов и каталогов по умолчанию;

Ускоренный – имена файла или каталогов;

Расширенный – атрибуты, владелец, группа и размер;

Определённый пользователем – имя, размер и атрибуты; 

Быстрый просмотр – выполняет быстрый просмотр содержимого панели. Информация – выдает всю имеющуюся информацию о файле или каталоге. Порядок сортировки – бывает: без сортировки, по имени, расширенный, время правки, время правки, время доступа, время изменение атрибута, размер, узел.

2. Какие операции с файлами можно выполнить как с помощью команд shell, так и с помощью меню (комбинаций клавиш) mc? Приведите несколько примеров.

Системная информация

Поиск

Копирование

3. Опишите структура меню левой (или правой) панели mc,дайте характеристику командам.

Список файлов показывает файлы в домашнем каталоге.

Быстрый просмотр позволяет выполнить быстрый просмотр содержимого панели.

Информация позволяет посмотреть информацию о файле или каталоге.

Командная оболочка Midnight Commander В меню каждой (левой или правой) панели можно выбрать Формат списка: стандартный,ускоренный,расширенный и определённый пользователем.

Порядок сортировки позволяет задать критерии сортировки при выводе списка файлов и каталогов: без сортировки, по имени, расширенный, время правки, время доступа, время изменения атрибута, размер, узел.

4. Опишите структура меню Файл mc, дайте характеристику командам.

Просмотр ( F3 ) позволяет посмотреть содержимое текущего файла без возможности редактирования.

Просмотр вывода команды ( М + ! ) функция запроса команды с параметрами.

Правка (F4) открывает текущий (или выделенный) файл для его редактирования.

Копирование (F5) осуществляеткопирование одного или нескольких файлов  или каталогов в указанное пользователем во всплывающем окне место.

Права доступа (Ctrl-x c) позволяет изменить права доступа к одному или нескольким файлам или каталогам.

Права доступа на файлы и каталоги

Жёсткая ссылка ( Ctrl-x l) позволяет создать жёсткую ссылку к текущему (или выделенному) файлу. 

Символическая ссылка ( Ctrl-x s) — позволяет создать символическую ссылку к текущему файлу .

Владелец группы ( Ctrl-x o ) позволяет задать владельца и имя группы для одного или нескольких файлов или каталогов.

Права (расширенные) позволяет изменить права доступа и владения для одного или нескольких файлов или каталогов.

Переименование ( F6) позволяет переименовать один или несколько файлов или каталогов.

Создание каталога ( F7) позволяет создать каталог.

Удалить ( F8 ) позволяет удалить один или несколько файлов или каталогов.

Выход ( F10 ) завершает работу mc.

5. Опишите структура меню Команда mc, дайте характеристику командам.

Дерево каталогов отображает структуру каталогов системы.

Поиск файла выполняет поиск файлов по заданным параметрам.

Переставить панели меняет местами левую и правую панели.

Сравнить каталоги ( Ctrl-x d ) сравнивает содержимое двух каталогов.

Размеры каталогов отображает размер и время изменения каталога (по умолчанию в mc размер каталога корректно не отображается).

История командной строки выводит на экран список ранее выполненных в оболочке команд.

Каталоги быстрого доступа ( Ctrl- ) при вызове выполняется быстрая смена текущего каталога на один из заданного списка.

Восстановление файлов позволяет восстановить файлы на файловых системах ext2 и ext3.

Редактировать файл расширений позволяет задать с помощью определённого синтаксиса действия при запуске файлов с определённым расширением (например, какое программного обеспечение запускать для открытия или редактирования файлов с расширением .c или .cpp).

Редактировать файл меню позволяет отредактировать контекстное меню пользователя, вызываемое по клавише F2 .

Редактировать файл расцветки имён позволяет подобрать оптимальную для пользователя расцветку имён файлов в зависимости от их типа.

6. Опишите структура меню Настройки mc,дайте характеристику командам.
Конфигурация позволяет скорректировать настройки работы с панелями.
Внешний вид и Настройки панелей определяет элементы,отображаемые при вызове mc, а также цветовое выделение.
Биты символов задаёт формат обработки информации локальным терминалом.
Подтверждение позволяет установить или убрать вывод окна с запросом подтверждения действий при операциях удаления и перезаписи файлов, а также при выходе из программы.
Распознание клавиш диалоговое окно используется для тестирования функциональных клавиш, клавиш управления курсором и прочее.
Виртуальные ФС настройки виртуальной файловой системы: тайм-аут, пароль и прочее.

7. Назовите и дайте характеристику встроенным командам mc.

F1 Вызов контекстно-зависимой подсказки.

F2 Вызов пользовательского меню с возможностью создания and/or.

F3 Просмотр содержимого файла, на который указывает подсветка в активной панели.

F4 Вызов встроенного в mc редактора для изменения содержания файла, на который указывает подсветка в активной панели.

F5 Копирование одного или нескольких файлов, отмеченных в первой (активной) панели, в каталог, отображаемый на второй панели.

F6 Перенос одного или нескольких файлов, отмеченных в первой панели, в каталог, отображаемый на второй панели. 

F7 Создание подкаталога в каталоге, отображаемом в активной панели.

F8 Удаление одного или нескольких файлов, отмеченных в первой панели файлов. 

F9 Вызов меню mc.

F10 Выход из mc.

8. Назовите и дайте характеристику командам встроенного редактора mc.

Ctrl+y удалить строку.

Ctrl+u отмена последней операции.

Ins вставка/замена.

F7 поиск.

Shift+F7 повтор последней операции поиска.

F4 замена файла.

F3 первое нажатие начало выделения, второе это окончание выделения.

F5 копировать выделенный фрагмент F6 переместить выделенный фрагмент.

F8 удалить выделенный фрагмент.

F2 записать изменения в файл.

F10 выйти из редактора.

9. Дайте характеристику средствам mc, которые позволяют создавать меню, определяемые пользователем.
Один из четырех форматов списка в Midnight Commander –пользовательский, определённый самим пользователем позволяет ему редактировать меню любого из двух списков. А меню пользователя – это меню, состоящее из команд, определенных пользователем. При вызове меню используется файл ~/.mc.menu. Если такого файла нет, то по умолчанию используется системный файл меню /usr/lib/mc/mc.menu. Все строки в этих файлах , начинающиеся с пробела или табуляции, являются командами, которые выполняются при выборе записи.

10. Дайте характеристику средствам mc, которые позволяют выполнять действия, определяемые пользователем, над текущим файлом.

Когда мы выделяем файл не являющегося исполняемым, Midnight Commander сравнивает расширение выбранного файла с расширениями, прописанными в«файле расширений» ~/ mc.ext. Если в файле расширений найдется подраздел, задающий процедуры обработки файлов с данным расширением,то обработка файла производится в соответствии с заданными в этом подразделе командами и файлами:

    • файл помощи для MC. /usr/lib/mc.hlp
    
    • файл расширений, используемый по умолчанию. /usr/lib/mc/mc.ext
    
    • файл расширений, конфигурации редактора. $HOME/.mc.ext
    
    • системный инициализационный файл. /usr/lib/mc/mc.ini
    
    • фаил который содержит основные установки. /usr/lib/mc/mc.lib
    
    • инициализационный файл пользователя. Если он существует,то системный файл mc.ini игнорируется. $HOME/.mc.ini
    
    • этот файл содержит подсказки, отображаемые в нижней части экрана.
    
    • /usr/lib/mc/mc.hint
    
    • системный файл меню MC,используемый по умолчанию./usr/lib/mc/mc.menu
    
    • файл меню пользователя. Если он существует, то системный файл меню
    
    • игнорируется. $HOME/.mc.menu
    
    • инициализационный файл пользователя. Если он существует,то системный
    
    • файл mc.ini игнорируется. $HOME/.mc.tree.

# Выводы

Я освоила основные возможности командной оболочки Midnight Commander. Приобрела навыкы практической работы по просмотру каталогов и файлов; манипуляций с ними.

# Список литературы{.unnumbered}

1. Dash, P. Getting Started with Oracle VM VirtualBox / P. Dash. – Packt Publishing Ltd, 2013. – 86 сс.
2. Colvin, H. VirtualBox: An Ultimate Guide Book on Virtualization with VirtualBox. VirtualBox / H. Colvin. – CreateSpace Independent Publishing Platform, 2015. – 70 сс.
3.  Vugt, S. van. Red Hat RHCSA/RHCE 7 cert guide : Red Hat Enterprise Linux 7 (EX200 and EX300) : Certification Guide. Red Hat RHCSA/RHCE 7 cert guide / S. van Vugt. – Pearson IT Certification, 2016. – 1008 сс.
4. Робачевский, А. Операционная система UNIX / А. Робачевский, С. Немнюгин, О. Стесик. – 2-е изд. – Санкт-Петербург : БХВ-Петербург, 2010. – 656 сс.
5. Немет, Э. Unix и Linux: руководство системного администратора. Unix и Linux / Э. Немет, Г. Снайдер, Т.Р. Хейн, Б. Уэйли. – 4-е изд. – Вильямс, 2014. – 1312 сс.
6. Колисниченко, Д.Н. Самоучитель системного администратора Linux : Системный администратор / Д.Н. Колисниченко. – Санкт-Петербург : БХВ-Петербург, 2011. – 544 сс.
7. Robbins, A. Bash Pocket Reference / A. Robbins. – O’Reilly Media, 2016. – 156 сс.


::: {#refs}
:::
