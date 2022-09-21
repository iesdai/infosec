---
# Front matter
lang: ru-RU
title: Защита лабораторной работы №5 Дискреционное разграничение прав в Linux. Исследование влияния дополнительных атрибутов
author: "Исаханян Эдуард Тигранович"
group: NFIbd-01-19
institute: RUDN University, Moscow, Russian Federation
date: 2022 Sep 17th

# Formatting
toc: false
slide_level: 2
theme: metropolis
header-includes: 
 - \metroset{progressbar=frametitle,sectionpage=progressbar,numbering=fraction}
 - '\makeatletter'
 - '\beamer@ignorenonframefalse'
 - '\makeatother'
aspectratio: 43
section-titles: true

---

# Защита лабораторной работы №5  

# Цель

Изучение механизмов изменения идентификаторов, применения SetUID- и Sticky-битов.
Получение практических навыков работы в консоли с дополнительными атрибутами.
Рассмотрение работы механизма смены идентификатора процессов пользователей, а также влияние бита Sticky на запись и удаление файлов.

# Выполнение лабораторной работы

## Программа simpleid.c

![Программа simpleid.c](images/1.png){ #fig:001 width=70% }

## Компиляция и выполнение программы simpleid

![Компиляция и выполнение программы simpleid](images/2.png){ #fig:002 width=70% }

## Программа simpleid2.c

![Программа simpleid2.c](images/3.png){ #fig:003 width=70% }

## Компиляция и выполнение программы simpleid2

![Компиляция и выполнение программы simpleid2](images/4.png){ #fig:004 width=70% }

## Смена пользователя. Установка SetUID-бита. Выполнение программы simpleid2

![Смена пользователя. Установка SetUID-бита. Выполнение программы simpleid2](images/5.png){ #fig:005 width=70% }

## Установка SetGID-бита. Выполнение программы simpleid2

![Установка SetGID-бита. Выполнение программы simpleid2](images/6.png){ #fig:006 width=70% }

## Программа readfile.c

![Программа readfile.c](images/7.png){ #fig:007 width=70% }

## Работа с программой readfile.c

![Работа с программой readfile.c](images/8.png){ #fig:008 width=70% }

## Установка SetUID-бита на программу readfile

![Установка SetUID-бита на программу readfile](images/9.png){ #fig:009 width=70% }

## Программа readfile читает readfile.c

![Программа readfile читает readfile.c](images/10.png){ #fig:010 width=70% }

## Программа readfile читает /etc/shadow

![Программа readfile читает /etc/shadow](images/11.png){ #fig:011 width=70% }

# Исследование Sticky-бита

## Исследование Sticky-бита от имени guest

![Исследование Sticky-бита от имени guest](images/12.png){ #fig:012 width=70% }

## Работа с file01.txt от имени guest2 при наличии Sticky-бита

![Работа с file01.txt от имени guest2 при наличии Sticky-бита](images/13.png){ #fig:013 width=70% }

## Снятие Sticky-бита с /tmp

![Снятие Sticky-бита с /tmp](images/14.png){ #fig:014 width=70% }

## Работа с file01.txt от имени guest2 без Sticky-бита

![Работа с file01.txt от имени guest2 без Sticky-бита](images/15.png){ #fig:015 width=70% }

## Возвращение Sticky-бита на /tmp

![Возвращение Sticky-бита на /tmp](images/16.png){ #fig:016 width=70% }


# Вывод   

Входе работы, мы изучили механизмы изменения идентификаторов, применения SetUID- и Sticky-битов.
Получили практические навыки работы в консоли с дополнительными
атрибутами. Рассмотрели работу механизма смены идентификатора процессов
пользователей, а также влияние бита Sticky на запись и удаление файлов.



