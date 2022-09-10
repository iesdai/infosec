---
# Front matter
title: "Отчет по лабораторной работе №2"
subtitle: "Задача о погоне"
author: "Исаханян Эдуард Тигранович"
group: NFIbd-01-19
institute: RUDN University, Moscow, Russian Federation
date: 2022 Feb 18th

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

Цель данной лабораторной работы построения математической модели для 
выбора правильной стратегии при решении задач поиска.

# Задание
В ходе работы мы должны:  
1. Записать уравнение, описывающее движение катера, с начальными
условиями для двух случаев (в зависимости от расположения катера
относительно лодки в начальный момент времени).  
2. Построить траекторию движения катера и лодки для двух случаев.  
3. Найти точку пересечения траектории катера и лодки.  

# Теоретическое введение  
Задача о погоне - это семейство задач в математике и информатике, в которых одна группа пытается поймать членов другой группы в определённой среде.     

***Постановка задачи***  

На море в тумане катер береговой охраны преследует лодку браконьеров.
Через определенный промежуток времени туман рассеивается, и лодка
обнаруживается на расстоянии 6,5 км от катера. Затем лодка снова скрывается в
тумане и уходит прямолинейно в неизвестном направлении. Известно, что скорость
катера в 2,6 раза больше скорости браконьерской лодки.  

***Решение исходной задачи сводится к решению системы из двух
дифференциальных уравнений.***  

$$ \left\{
\begin{array}{c}
\frac{dt}{dt} = v \\
r\frac{d\theta}{dt} = \sqrt(5.76)v \\
\end{array}
\right.$$
с начальными условиями  
$$ \left\{
\begin{array}{c}
\theta = 0 \\
r = \frac{k}{3.6} \\
\end{array}
\right.$$ 
или  
$$ \left\{
\begin{array}{c}
\theta = -\pi \\
r = \frac{k}{1.6} \\
\end{array}
\right.$$ 

# Выполнение лабораторной работы
***Решение***  
1. Принимем за $t_0 = 0$, $x_л0 = 0$ - место нахождения лодки браконьеров в
момент обнаружения, $x_к0 = k$ - место нахождения катера береговой охраны
относительно лодки браконьеров в момент обнаружения лодки.  
2. Введем полярные координаты. Считаем, что полюс - это точка обнаружения
   лодки браконьеров x_л0 ($\theta = x_л0 = 0$), а полярная ось
   r проходит через точку нахождения катера береговой охраны.  
    ![Положение катера и лодки в начальный момент времени](images/image12.png)  
3. Чтобы найти расстояние x (расстояние после которого катер начнет
   двигаться вокруг полюса), необходимо составить простое уравнение. Пусть
   через время t катер и лодка окажутся на одном расстоянии x
   от полюса. За это время лодка пройдет x, а катер k-x (или
   k+x, в зависимости от начального положения катера относительно полюса). Время, за которое они
   пройдут это расстояние, вычисляется как $\frac{x}{v}$
   или $\frac{k-x}{2.6v}$ (во втором случае $\frac{k+x}{2.6v}$). Так как время одно и то же, то эти величины одинаковы.
   Тогда неизвестное расстояние x можно найти из следующего уравнения:
   $\frac{x}{v} = \frac{k-x}{2.6v}$ в первом случае или $\frac{x}{v} = \frac{k+x}{2.6v}$ во втором.  
   Отсюда мы найдем два значения $x_1 = \frac{k}{3.6}$ и $x_2 = \frac{k}{1.6}$, задачу будем решать для
   двух случаев.  
   ![Расчеты для 1 и 2 случая](images/image10.png)  
4. После того, как катер береговой охраны окажется на одном расстоянии от
   полюса, что и лодка, он должен сменить прямолинейную траекторию и
   начать двигаться вокруг полюса удаляясь от него со скоростью лодки v.  
   Для этого скорость катера раскладываем на две составляющие: v~r~ -
   радиальная скорость и $v_\tau$ - тангенциальная скорость. Радиальная скорость - это скорость, с которой катер удаляется от полюса,
   $v_r = \frac{dr}{dt}$. Нам нужно, чтобы эта скорость была равна скорости лодки, поэтому полагаем
   $\frac{dr}{dt} = v$.  
   Тангенциальная скорость – это линейная скорость вращения катера
   относительно полюса. Она равна произведению угловой скорости
   $\frac{d\theta}{dt}$ на радиус r, $v_\tau = r\frac{d\theta}{dt}$.  
   ![Разложение скорости катера на тангенциальную и радиальную составляющие](images/image13.png)  
   ![Расчет тангенциальной скорости](images/image11.png)  

***Написание программы***  

1. Для начала мы напишем функции для движения катера и лодки.  
   ![Функция для движения катера](images/image1.png)  
   ![Функция для движения лодки](images/image2.png)  
2. Далее напишем общие начальные данные.  
   ![Начальные данные](images/image3.png)  
3. Теперь напишем данные для 1 случая, создадим графическое окно и нарисуем график.
    Движение катера нарисуем зеленной линией, а движение лодки красным.   
   ![Данные для 1 случая](images/image4.png)  
   ![Создание графического окна и нарисование графика](images/image5.png)  
4. Далее тоже самое сделаем для 2 случая.  
   ![Данные для 2 случая](images/image6.png)  
   ![Создание графического окна и нарисование графика](images/image7.png)  
5. Посмотрим на результат 1 случая и для 2 случая.  
   ![График 1 случая](images/image8.png)  
   ![График 2 случая](images/image9.png)  
    Из графиков видно, что для 1 случая катер и лодка встречаются в точке 1.77,а для 2 случая в точке 14.75.  

# Выводы  
Входе работы, мы научились строить математическую модель для выбора правильной стратегии при решении задач поиска.  


# Список литературы{.unnumbered}
1. Методические материалы к лабораторной работе, представленные на сайте "ТУИС РУДН" https://esystem.rudn.ru/  
::: {#refs}
:::