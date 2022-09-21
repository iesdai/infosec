---
# Front matter
lang: ru-RU
title: Защита лабораторной работы №6 Мандатное разграничение прав в Linux
author: "Исаханян Эдуард Тигранович"
group: NFIbd-01-19
institute: RUDN University, Moscow, Russian Federation
date: 2022 Sep 21th

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

# Защита лабораторной работы №6  

# Цель

Развить навыки администрирования ОС Linux. Получить первое практическое знакомство с технологией SELinux1. Проверить работу SELinx на практике совместно с веб-сервером Apache.

# Подготовка лабораторного стенда

## Параметр ServerName

![Параметр ServerName](images/1.png){ #fig:001 width=70% }

## Отключение фильтра

![Отключение фильтра](images/2.png){ #fig:002 width=70% height=70% }

## Отключение фильтра

![Отключение фильтра](images/3.png){ #fig:003 width=70% height=70% }

# Выполнение лабораторной работы

## Проверка режима и политики

![Проверка режима и политики](images/4.png){ #fig:004 width=70% height=70% }

## Проверка через браузер

![Проверка через браузер](images/5.png){ #fig:005 width=70% height=70% }

## Проверка через браузер

![Проверка статуса](images/6.png){ #fig:006 width=70% height=70% }

## веб-сервер Apache

![веб-сервер Apache](images/7.png){ #fig:007 width=70% height=70% }

## Просмотр переключателей SELinux для Apache

![Просмотр переключателей SELinux для Apache](images/8.png){ #fig:008 width=70% height=70% }

## Статистика

![Статистика](images/9.png){ #fig:009 width=70% height=70% }

## Определение типов файлов и круг пользователей

![Определение типов файлов и круг пользователей](images/10.png){ #fig:010 width=70% height=70% }

## Создание файла

![Создание файла](images/11.png){ #fig:011 width=70% height=70% }

## Проверка

![Проверка](images/12.png){ #fig:012 width=70% height=70% }

## Получение доступа к файлу через браузер

![Получение доступа к файлу через браузер](images/13.png){ #fig:013 width=50% height=50% }

## Изменение контекста, проверка

![Изменение контекста, проверка](images/14.png){ #fig:014 width=50% height=50% }

## Получение доступа к файлу через браузер

![Получение доступа к файлу через браузер](images/15.png){ #fig:015 width=50% height=50% }

## Анализ ситуации

![Анализ ситуации](images/16.png){ #fig:016 width=50% height=50% }

## Изменеие порта 80 на 81

![Изменеие порта 80 на 81](images/17.png){ #fig:017 width=50% height=50% }

## Анализ и просмотр лог-файлов

![Анализ и просмотр лог-файлов](images/18.png){ #fig:018 width=50% height=50% }

## Выполнение и проверка

![Выполнение и проверка](images/19.png){ #fig:019 width=50% height=50% }

## Возвращение контекста

![Возвращение контекста](images/20.png){ #fig:020 width=50% height=50% }

## Получение доступа к файлу через браузер

![Получение доступа к файлу через браузер](images/21.png){ #fig:021 width=50% height=50% }

## Исправленный файл apache

![Исправленный файл apache](images/23.png){ #fig:022 width=50% height=50% }

## Удаление привязки к 81 порту и удаление файла

![Удаление привязки к 81 порту и удаление файла](images/22.png){ #fig:023 width=50% height=50% }

# Вывод   

Входе работы, мы развили навыки администрирования ОС Linux. Получили первое практическое знакомство
с технологией SELinux. Проверили работу SELinx на практике совместно с
веб-сервером Apache.



