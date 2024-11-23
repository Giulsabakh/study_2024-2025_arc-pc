---
## Front matter
title: "Лабораторная работа №8"
subtitle: "Команды безусловного и условного переходов в Nasm. Программирование ветвлений."
author: "Байрамова Гюльсабах Акифовна"

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

1) Я создала каталог lab8 и внутри создал файл lab8-1.asm

![Cоздание файла lab8-1.asm]![6 1](https://github.com/user-attachments/assets/ac135cf1-0e05-41eb-8528-657eab474142)
{ #fig:001 width=70% }

2) Я ввела в файл текст программы и запустила его.

![Текст в файле lab8-1.asm]![6 2](https://github.com/user-attachments/assets/3c2970db-c7ca-456b-a3b3-5ad64433358e)
{ #fig:002 width=70% }

3) Я создала исполняемый файл и запустила его. Результат соответствовал нужному.

![Запуск программы lab8-1]![6 3](https://github.com/user-attachments/assets/2d707164-0d3a-4360-a81f-c38d4e1e128a)

{ #fig:003 width=70% }

4)Я изменила текст программы чтобы выводился нужный ответ и создала исполняемый файл.

![Изменение текста]![6 4](https://github.com/user-attachments/assets/f1d733d2-cec0-4378-ba08-10eeeacc37c3)
{ #fig:004 width=70% }

![Проверка работы программы]![6 5](https://github.com/user-attachments/assets/debbe034-d4c6-4930-8afc-961f587b8833)
{ #fig:005 width=70% }

5)Я изменила текст программы чтобы сначала выводило сообщение 3,затем 2, затем 1.

![Изменение текста]![6 6](https://github.com/user-attachments/assets/e0788494-1a1f-409f-85af-f58e4692865c)
{ #fig:006 width=70% }

6) Запустила программу и проверила ее работу.

![Запуск программы]![6 7](https://github.com/user-attachments/assets/b3821856-4f11-4ed4-82c1-c38848dcbd68)
{ #fig:007 width=70% }

7) Я создала файл lab8-2.asm и написала текст программы.

![Текст программы для сравнения чисел]![6 8](https://github.com/user-attachments/assets/ead9a18a-d79f-4746-9717-21aff0e718b3)
{ #fig:008 width=70% }

8) Я ввела два разных числа чтобы проверить как работает программа. 

![Программа для сравнения чисел]![6 9](https://github.com/user-attachments/assets/cf7d2c27-f266-4b01-b0ea-079020540222)
{ #fig:09 width=70% }

9) Я создала файл листинга lab8-2.lst и открыла его.

![Файл листинга lab8-2.lst]![6 10](https://github.com/user-attachments/assets/64516b30-2c44-4b5d-8904-09e9826a8787)
{ #fig:010 width=70% }

10) Проанализировав файл, я поняла как он работает и какие значения выводит.

1) Эта строка находится на 24 месте, ее адрес "00000101", Машинный код - В8 [0A000000], а mov eax,B - исходный текст программы, означающий что в регистр eax мы вносим значения переменной B.

![Объяснения первой строки]![6 11](https://github.com/user-attachments/assets/39c83120-7d61-452a-bfdc-c53091ab429f)
{ #fig:011 width=70% }

2) Эта строка находится на 38 месте, ее адрес "00000134", Машинный код - E863FFFFFF, а call atoi - исходный текст программы, означающий что символ лежащий в строке выше переводится в число.

![Объяснения второй строки]![6 12](https://github.com/user-attachments/assets/aff864fb-ab88-4085-8dd3-822f77ee95f2)
{ #fig:012 width=70% }

3) Эта строка находится на 50 месте, ее адрес "00000162", Машинный код - A1[00000000], а mov eax,[max] - исходный текст программы, означающий что число хранившееся в переменной max записывается в регистр eax.

![Объяснения третьей строки]![6 13](https://github.com/user-attachments/assets/ece50551-336f-4e83-bdcb-1b29e11650fe)
{ #fig:013 width=70% }

11) В строке mov eax,max я убрала max и попробовала создать файл. Выдало ошибку, так как для программы нужно два операнда.
![Создание файла без одного операнда]![6 14](https://github.com/user-attachments/assets/8cca3bf9-f7ff-4d6f-b3db-73bd87bd6994)
{ #fig:014 width=70% }

12) В файле листинга показывает где именно ошибка и с чем она связана.

![Файл листинга без одного операнда]![6 15](https://github.com/user-attachments/assets/0efee3ae-5334-447b-a2de-86ce44b620f0)
{ #fig:015 width=70% }

# Самостоятельная работа.

1) Я написала программу для нахождения меньшего из трех чисел. Для большего удобства я сделал ввод чисел с клавиатуры.У меня 11 вариант поэтому числа были: 21, 28, 34. Программа вывела меньшее из этих чисел.

![Текст программы]![6 16](https://github.com/user-attachments/assets/13e74787-01ed-4745-99d3-f6847d1677b9)
{ #fig:016 width=70% }

2) Я написалf программу, чтобы она вычисляла выражение при введенных Х и А. Для большего удобства, выражение которое будет вычисляться я вывожу вначале работы программы. Так как у меня 11 вариант, то программа написана для 11 варианта.

![Текст программы]![6 18](https://github.com/user-attachments/assets/234ff09a-5c04-4059-b341-61b7099ccfef)
{ #fig:018 width=70% }

# Вывод

Я изучила команды условного и безусловного перехода. Приобрелф навыки написания программ с переходами.

::: {#refs}
:::
