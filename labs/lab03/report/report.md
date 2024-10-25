---
## Front matter
title: "Отчёт по лабораторной работе №3"
subtitle: "*Дисциплина: Архитектура компьютера*"
author: "Байрамова Гюльсабах Акифовна НММбд-01-24"

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

Целью работы является освоение процедуры оформления отчетов с помощью легковесного
языка разметки Markdown.

# Задание

1) Техническое обеспечение
	1) Установка необходимого ПО
2) Заполнение и компиляция отчёта по лабораторной работе №3
3) Задание для самостоятельной работы

# Теоретическое введение

Здесь описываются теоретические аспекты, связанные с выполнением работы.

Например, в табл. [-@tbl:std-dir] приведено краткое описание стандартных каталогов Unix.

: Описание некоторых каталогов файловой системы GNU Linux {#tbl:std-dir}

| Имя каталога | Описание каталога                                                                                                          |
|--------------|----------------------------------------------------------------------------------------------------------------------------|
| `/`          | Корневая директория, содержащая всю файловую                                                                               |
| `/bin `      | Основные системные утилиты, необходимые как в однопользовательском режиме, так и при обычной работе всем пользователям     |
| `/etc`       | Общесистемные конфигурационные файлы и файлы конфигурации установленных программ                                           |
| `/home`      | Содержит домашние директории пользователей, которые, в свою очередь, содержат персональные настройки и данные пользователя |
| `/media`     | Точки монтирования для сменных носителей                                                                                   |
| `/root`      | Домашняя директория пользователя  `root`                                                                                   |
| `/tmp`       | Временные файлы                                                                                                            |
| `/usr`       | Вторичная иерархия для данных пользователя                                                                                 |

Более подробно про Unix см. в [@tanenbaum_book_modern-os_ru; @robbins_book_bash_en; @zarrelli_book_mastering-bash_en; @newham_book_learning-bash_en].

# Выполнение лабораторной работы

Для начала откроем терминал и перейдём в каталог курса сформированный при выполнении лабораторной работы №2 (рис. [-@fig:001]).

![Переход в каталог курса сформированный при выполнении лабораторной работы №2]![1 1](https://github.com/user-attachments/assets/2b1bb17d-aa37-410d-a787-9497ee6de3d1)
{#fig:001 width=70%}

Далее обновим локальный репозиторий, скачав изменения из удаленного репозитория с помощью команды git pull (рис. [-@fig:002]).

![Обновление репозитория]![1 2](https://github.com/user-attachments/assets/35903943-8b58-40d1-9bd3-6422d574d5a5)
{#fig:002 width=70%}

Перейдём в каталог с шаблоном отчета по лабораторной работе № 3 (рис. [-@fig:003]).

![Переход в каталог с шаблоном отчёта]![1 3](https://github.com/user-attachments/assets/5eebcaa0-3468-45f7-a111-bf5db273a605)
{#fig:003 width=70%}

Проведём компиляцию шаблона с использованием Makefile. Для этого введём команду make (рис. [-@fig:004]).

![Команда make]![1 4](https://github.com/user-attachments/assets/f8d795bc-53bd-48cd-b2d4-230633d182ae)
{#fig:004 width=70%}

Удалим полученный файлы с использованием Makefile. Для этого введём команду make clean (рис. [-@fig:005]).

![Команда make clean]![1 5](https://github.com/user-attachments/assets/3fc17c7c-58f6-4501-932a-9536eaae8d1b)
{#fig:005 width=70%}

Откроем файл report.md c помощью любого текстового редактора, например gedit (рис. [-@fig:006]).

![Редактор gedit]![1 6](https://github.com/user-attachments/assets/c10a3ab6-8078-44e1-9e6b-9b85ab4f9662)
{#fig:006 width=70%}

Заполним и скомпилируем отчет с использованием Makefile. Проверим корректность полученных файлов (рис. [-@fig:007]).

![Проверка]![1 11](https://github.com/user-attachments/assets/6a168186-4610-46de-8d3f-22de3453684d)
{#fig:007 width=70%}

Загрузим файлы на Github (рис. [-@fig:008]).

![Загрузка на Github]![1 7](https://github.com/user-attachments/assets/76aac2df-7f8e-4255-9779-da765fc1f517)
{#fig:008 width=70%}

Приступим к выполнению задания для самостоятельной работы. В соответствующем каталоге сделаем отчёт по лабораторной работе № 2 в формате Markdown (рис. [-@fig:010]).

![Отчёт по лабораторной работе №2]![1 10](https://github.com/user-attachments/assets/e0b34a00-a4bb-4897-83fb-3bed7ad8f1d6)
{#fig:010 width=70%}

Загрузим файлы на Github (рис. [-@fig:011]).

![Загрузка на Github]![1 9](https://github.com/user-attachments/assets/97a9c761-a8a1-434a-966b-a5a404afb388)
{#fig:011 width=70%}

# Выводы

В ходе выполнения этой лабораторной работы я освоил процедуры оформления отчетов с помощью легковесного
языка разметки Markdown.

# Список литературы{.unnumbered}

::: {#refs}
:::