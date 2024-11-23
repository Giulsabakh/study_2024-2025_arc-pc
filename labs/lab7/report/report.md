---
## Front matter
title: "Лабораторная работа №8"
subtitle: "Команды безусловного и условного переходов в Nasm. Программирование ветвлений."
author: "Лушин Артем Андреевич"

## Generic otions
lang: ru-RU
toc-title: "Содержание"

## Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

## Pdf output format
toc: true # Table of contents
toc-depth: 2
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
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase,Scale=0.9
## Biblatex
biblatex: false
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

Изучение команд условного и безусловного переходов. Приобретение навыков написания программ с использованием переходов. Знакомство с назначением и структурой файла листинга.

# Выполнение лабораторной работы

1) Я создал каталог lab8 и внутри создал файл lab8-1.asm

![Cоздание файла lab8-1.asm](image/1.png){ #fig:001 width=70% }

2) Я ввел в файл текст программы и запустил его.

![Текст в файле lab8-1.asm](image/2.png){ #fig:002 width=70% }

3) Я создал исполняемый файл и запустил его. Результат соответствовал нужному.

![Запуск программы lab8-1](image/3.png){ #fig:003 width=70% }

4)Я изменил текст программы чтобы выводился нужный ответ и создал исполняемый файл.

![Изменение текста](image/4.png){ #fig:004 width=70% }

![Проверка работы программы](image/5.png){ #fig:005 width=70% }

5)Я изменил текст программы чтобы сначала выводило сообщение 3,затем 2, затем 1.

![Изменение текста](image/6.png){ #fig:006 width=70% }

6) Запустил программу и проверил ее работу.

![Запуск программы](image/7.png){ #fig:007 width=70% }

7) Я создал файл lab8-2.asm и написал текст программы.

![Текст программы для сравнения чисел](image/8.png){ #fig:008 width=70% }

8) Я ввел два разных числа чтобы проверить как работает программа. 

![Программа для сравнения чисел](image/9.png){ #fig:09 width=70% }

9) Я создал файл листинга lab8-2.lst и открыл его.

![Файл листинга lab8-2.lst](image/10.png){ #fig:010 width=70% }

10) Проанализировав файл, я понял как он работает и какие значения выводит.

1) Эта строка находится на 24 месте, ее адрес "00000101", Машинный код - В8 [0A000000], а mov eax,B - исходный текст программы, означающий что в регистр eax мы вносим значения переменной B.

![Объяснения первой строки](image/11.png){ #fig:011 width=70% }

2) Эта строка находится на 38 месте, ее адрес "00000134", Машинный код - E863FFFFFF, а call atoi - исходный текст программы, означающий что символ лежащий в строке выше переводится в число.

![Объяснения второй строки](image/12.png){ #fig:012 width=70% }

3) Эта строка находится на 50 месте, ее адрес "00000162", Машинный код - A1[00000000], а mov eax,[max] - исходный текст программы, означающий что число хранившееся в переменной max записывается в регистр eax.

![Объяснения третьей строки](image/13.png){ #fig:013 width=70% }

11) В строке mov eax,max я убрал max и попробовал создать файл. Выдало ошибку, так как для программы нужно два операнда.

![Создание файла без одного операнда](image/14.png){ #fig:014 width=70% }

12) В файле листинга показывает где именно ошибка и с чем она связана.

![Файл листинга без одного операнда](image/15.png){ #fig:015 width=70% }

# Самостоятельная работа.

1) Я написал программу для нахождения меньшего из трех чисел. Для большего удобства я сделал ввод чисел с клавиатуры.У меня первый вариант поэтому числа были :17,23,45. Программа вывела меньшее из этих чисел.

![Текст программы](image/16.png){ #fig:016 width=70% }

![Результат работы программы](image/17.png){ #fig:017 width=70% }

2) Я написал программу, чтобы она вычисляла выражение при введенных Х и А. Для большего удобства, выражение которое будет вычисляться я вывожу вначале работы программы. Так как у меня 1 вариант, то программа написана для 1 варианта.

![Текст программы](image/18.png){ #fig:018 width=70% }

![Проверка работы программы](image/19.png){ #fig:019 width=70% }

# Вывод

Я изучил команды условного и безусловного перехода. Приобрел навыки написания программ с переходами.

::: {#refs}
:::
