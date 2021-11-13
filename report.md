---
# Front matter
title: "Отчёт по лабараторной работе №5"
author: "Кучен Ирзилей Сайын"

# Generic otions
lang: ru-RU
toc-title: "Содержание"

# Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

# Pdf output format
toc: true # Table of contents
toc_depth: 2
lof: true # List of figures
lot: true # List of tables
fontsize: 12pt
linestretch: 1.5
papersize: a4
documentclass: scrreprt
## I18n
polyglossia-lang:
  name: russian
  options:
	- spelling=modern
	- babelshorthands=true
polyglossia-otherlangs:
  name: english
### Fonts
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase,Scale=0.9
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
## Misc options
indent: true
header-includes:
  - \linepenalty=10 # the penalty added to the badness of each line within a paragraph (no associated penalty node) Increasing the value makes tex try to have fewer lines in the paragraph.
  - \interlinepenalty=0 # value of the penalty (node) added after each line of a paragraph.
  - \hyphenpenalty=50 # the penalty for line breaking at an automatically inserted hyphen
  - \exhyphenpenalty=50 # the penalty for line breaking at an explicit hyphen
  - \binoppenalty=700 # the penalty for breaking a line at a binary operator
  - \relpenalty=500 # the penalty for breaking a line at a relation
  - \clubpenalty=150 # extra penalty for breaking after first line of a paragraph
  - \widowpenalty=150 # extra penalty for breaking before last line of a paragraph
  - \displaywidowpenalty=50 # extra penalty for breaking before last line before a display math
  - \brokenpenalty=100 # extra penalty for page breaking after a hyphenated line
  - \predisplaypenalty=10000 # penalty for breaking before a display
  - \postdisplaypenalty=0 # penalty for breaking after a display
  - \floatingpenalty = 20000 # penalty for splitting an insertion (can only be split footnote in standard LaTeX)
  - \raggedbottom # or \flushbottom
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Изучение механизмов изменения идентификаторов, применения
SetUID- и Sticky-битов. Получение практических навыков работы в консоли с дополнительными атрибутами. Рассмотрение работы механизма
смены идентификатора процессов пользователей, а также влияние бита
Sticky на запись и удаление файлов.

# Задание

Выполнить все пункты, занося ваши ответы на поставленные вопросы и замечания в отчёт.

# Выполнение лабораторной работы

1. Войдите в систему от имени пользователя guest.

![Вход](image/1.jpg){ #fig:001 width=70% }

2. Создайте программу simpleid.c:

![Создание программы](image/2.jpg){ #fig:001 width=70% }

3. Скомплилируйте программу и убедитесь, что файл программы создан:

![Компилирование](image/3.jpg){ #fig:001 width=70% }

4. Выполните программу simpleid:

![Выполнение](image/4.jpg){ #fig:001 width=70% }

5. Выполните системную программу id: id и сравните полученный вами результат с данными предыдущего пункта задания.

![Выполнение id](image/5.jpg){ #fig:001 width=70% }

6. Усложните программу, добавив вывод действительных идентификаторов:

![Усложнение](image/6.jpg){ #fig:001 width=70% }

7. Скомпилируйте и запустите simpleid2.c:

![Компиляция](image/7.jpg){ #fig:001 width=70% }

8. От имени суперпользователя выполните команды:

![Выполнение команд](image/8.jpg){ #fig:001 width=70% }

9. Используйте sudo или повысьте временно свои права с помощью su.
Поясните, что делают эти команды.

![Повышение прав](image/9.jpg){ #fig:001 width=70% }

10. Выполните проверку правильности установки новых атрибутов и смены
владельца файла simpleid2:

![Проверка](image/10.jpg){ #fig:001 width=70% }

11. Запустите simpleid2 и id:

![Запуск](image/11.jpg){ #fig:001 width=70% }

# Выводы

В результате выполнения работы мы изучили механизмы изменения идентификаторов, применения
SetUID- и Sticky-битов. Полученили практические навыки работы в консоли с дополнительными атрибутами. Рассмотрели работы механизма
смены идентификатора процессов пользователей, а также влияние бита
Sticky на запись и удаление файлов.
