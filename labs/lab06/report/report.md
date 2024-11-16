---
## Front matter
title: "Лабораторная работа №7"
subtitle: "Арифметические операции в NASM."
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

Освоение арифметических инструкций языка ассемблера NASM.



# Выполнение лабораторной работы

1) Я создала каталог lab07 и внутри создал файл lab7-1.asm.

![Создание файла lab7-1.asm]![2 1](https://github.com/user-attachments/assets/bd6e4618-0abe-4a79-b589-26aa7b2d9d4b)
{ #fig:001 width=70% }

2) В файл lab7-1.asm я ввела нужный текст, создал файл и проверила его. Программа вывела j.

![Текст в файле lab7-1.asm]![2 2](https://github.com/user-attachments/assets/e06d284d-3c68-4ee2-88a9-7b8cc158640b)
{ #fig:002 width=70% }

![Создание файла и проверка работы]![2 3](https://github.com/user-attachments/assets/aff2c96f-a8d8-4440-baa2-4a0b260b7f40)
{ #fig:003 width=70% }

3) Я изменила  текст программы. Когда я сделала программу и запустила ее, она вывела невидимый символ, как и должна была.

![Изменения программы lab7-1.asm]![2 4](https://github.com/user-attachments/assets/df0838fc-6144-410e-85d5-3dccefd82a2a)
 #fig:004 width=70% }

![Проверка программы]![2 5](https://github.com/user-attachments/assets/5f333124-8f52-4b35-a2aa-e6686d2fd49f)
{ #fig:005 width=70% }

4) Я создала файл lab7-2.asm и ввела в него текст программы.

![Создание файла lab7-2.asm]![2 6](https://github.com/user-attachments/assets/6146f8cd-1421-4890-900c-7dac2e55d2a8)
{ #fig:006 width=70% }

5) Cоздалф исполняемый файл и запустил его. Как и предполагалось, он вывел число 106.

![Запуск программы lab7-2.asm]![2 7](https://github.com/user-attachments/assets/6a08ed72-f558-4cdb-934e-07d939c55687)
{ #fig:007 width=70% }

6) Я изменилф текст программы lab7-2 и запустилф ее. Она вывела число 10, как и должна была.

![Изменения в программе lab7-2.asm]![2 8](https://github.com/user-attachments/assets/a8249860-3e23-4d61-a50d-333bdb9d4832)
{ #fig:008 width=70% }

![Проверка программы]![2 9](https://github.com/user-attachments/assets/3bc952bb-465e-4a1f-9a00-98742dfee412)
{ #fig:009 width=70% }

7)Я заменила функцию iprintLF на iprint. Проверила файл и результат отличался в выводе данных. Когда используется команда iprintLF мы начинаем вводить команду на следующей строке, а при использовании команды iprint мы вводим следующие данные на той же строке.

![Замена iprintLF на iprint]![2 10](https://github.com/user-attachments/assets/159bd104-9e69-415a-9815-86231066880e)
{ #fig:010 width=70% }

![Запуск программы с изменениями]![2 11](https://github.com/user-attachments/assets/e22d4d7c-8713-4efa-86bc-ed7cd68ec0b7)
{ #fig:011 width=70% }

8) Я создала файл lab7-3.asm и ввела текст программы. Запустила и проверила ее работу.

![Текст в программе lab7-3.asm]![2 13](https://github.com/user-attachments/assets/ab044789-866d-41d9-bcbb-de3e670c628d)
{ #fig:012 width=70% }

![Запуск программы lab7-3]![2 13](https://github.com/user-attachments/assets/22735fc9-5ce5-414a-9b79-5fb5e5e27bc0)
{ #fig:013 width=70% }

9) Я изменила программу для примера F(x) = (4*6+2)/5. Запустила ее и проверил

![Изменения в программе lab7-3]![2 14](https://github.com/user-attachments/assets/e84f018b-4511-45b0-8769-e8bb4151c027)
{ #fig:015 width=70% }

![Запуск программы]![2 15](https://github.com/user-attachments/assets/f2362980-99e7-47a4-ac6a-ac60b50b3bdc)
{ #fig:016 width=70% }

10) Я создала файл variant.asm и ввела туда нужный текст.

![Текст программы в файле variant.asm]![2 16](https://github.com/user-attachments/assets/bdd5d927-ac0e-4195-8d27-ac494893bf4c)
{ #fig:017 width=70% }

11) Я ввела в эту программу свой студенческий билет "1132226520" Он вывел ответ 1, я проверила это аналитически, ответ совпал.

![Запуск программы variant]![2 17](https://github.com/user-attachments/assets/91c0f0e1-8239-4322-a6fb-d0db32833c3e)
{ #fig:018 width=70% }

# Вопросы:

1)Какие строки листинга 7.4 отвечают за вывод на экран сообщения ‘Ваш вариант:’? 

mov eax,msg
call sprintLF

2) Для чего используется следующие инструкции? nasm mov ecx, x
mov edx, 80 call sread

Эти инструкции используются для ввода переменной Х с клавиатуры и сохранения введенных данных.

3) Для чего используется инструкция “call atoi”?

Эта инструкция используется для преобразования Кода переменной ASCII в число.

4) Какие строки листинга 7.4 отвечают за вычисления варианта?

mov ebx,20
div ebx
inc edx

5)В какой регистр записывается остаток от деления при выполнении инструкции “div ebx”?

В регистре ebx.

6) Для чего используется инструкция “inc edx”?

Для увеличения значения edx на 1.

7)Какие строки листинга 7.4 отвечают за вывод на экран результата вычислений?

mov eax,edx
call iprintLF

# Самостоятельная работа

Открываю созданный файл для редактирования, ввожу в него текст программы для вычисления значения выражения (11 + x) * 2 - 6 (рис. [-@fig:024]). Это выражение было под вариантом 8.

![Программа для вычесления записанная в файле 1.asm]![4 1](https://github.com/user-attachments/assets/b9c2945d-b7bf-4295-91b6-9431c4bba4a8)
{ #fig:019 width=70% }

![Результаты работы этой программы]![4 2](https://github.com/user-attachments/assets/999457c0-a981-4a4a-8bd0-290fe40c53f2)
{ #fig:020 width=70% }

# Вывод

Я освоила арифметические инструкции языка ассемблер NASM.

::: {#refs}
:::
