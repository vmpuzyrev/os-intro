---
# РОССИЙСКИЙ УНИВЕРСИТЕТ ДРУЖБЫ НАРОДОВ
## Факультет физико-математических и естественных наук

lang: ru-RU
title: "Отчёт по лабораторной работе №9"
author: "Пузырев Владислав Максимович"

# Formatting
toc-title: "Содержание"
toc: true # Table of contents
toc_depth: 2
lof: true # List of figures
lot: true # List of tables
fontsize: 12pt
linestretch: 1.5
papersize: a4paper
documentclass: scrreprt
polyglossia-lang: russian
polyglossia-otherlangs: english
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase
indent: true
pdf-engine: lualatex
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

Познакомиться с операционной системой Linux, получить практические навыки работы с редактором vi, установленным по умолчанию практически во всех дистрибутивах.

# Задание

1. Ознакомился с теоретическим материалом.
2. Ознакомился с редактором vi.
3. Выполнил упражнения, используя команды vi.


# Выполнение лабораторной работы

**Задание 1. Создание нового файла с использованием vi.**

1. Создал каталог с именем ~/work/os/lab06.

2. Перешёл во вновь созданный каталог.

3. Вызвал vi и создал файл hello.sh

4. И сразу же исходя из задания обозначил уровень доступа.

![](image/3.png)

4. Нажал клавишу i и ввела следующий текст:

#!/bin/bash

HELL=Hello

function hello {

LOCAL HELLO=World

echo $HELLO

}

echo $HELLO

hello

![](image/1.png)

5. Нажал клавишу Esc для перехода в командный режим после завершения ввода

текста.

6. Нажал «:» для перехода в режим последней строки и внизу экрана появилось приглашение в виде двоеточия.

7. Нажал w (записать) и q (выйти), а затем нажал клавишу Enter для сохранения текста и завершения работы.

![](image/4.bmp)

**Задание 2. Редактирование существующего файла.**

1. Вызвал vi на редактирование файла.

2. Установил курсор в конец слова HELL второй строки.

![](image/5.bmp)

3. Перешёл в режим вставки и заменил на HELLO. Нажал Esc для возврата в
командный режим.

![](image/6.bmp)

4. Установил курсор на четвертую строку и стёр с1.Краткая характеристика режимов работы редактора vi:

– командный режим — предназначен для ввода команд редактирования и навигации по редактируемому файлу;

– режим вставки — предназначен для ввода содержания редактируемого файла;

– режим последней (или командной) строки — используется для записи изменений

в файл и выхода из редактора.

2. Выйти из редактора, не сохраняя произведённые изменения, можно используя клавиши «:q!» в командном режиме.

3. Краткую характеристика команд позиционирования:

– 0 (ноль) — переход в начало строки;

– $ — переход в конец строки;

– G — переход в конец файла;

– n G — переход на строку с номером n.

4. Для редактора vi словом является: пробел; буквы, находящиеся между двумя пробелами.

5. Из любого места редактируемого файла перейти в конец файла можно с помощью клавишы G и курсора вниз, а в начало – курсор вверх.

6. Краткая характеристика основных групп команд редактирования:

Вставка текста

– а — вставить текст после курсора;

– А — вставить текст в конец строки;

– i — вставить текст перед курсором;

– n i — вставить текст n раз;

– I — вставить текст в начало строки.

Вставка строки

– о — вставить строку под курсором;

– О — вставить строку над курсором. Удаление текста

– x — удалить один символ в буфер;

– d w — удалить одно слово в буфер;

– d $ — удалить в буфер текст от курсора до конца строки;

– d 0 — удалить в буфер текст от начала строки до позиции курсора;

– d d — удалить в буфер одну строку;

– n d d — удалить в буфер n строк. Отмена и повтор произведённых изменений

– u — отменить последнее изменение;

– . — повторить последнее изменение.

Копирование текста в буфер

– Y — скопировать строку в буфер;

– n Y — скопировать n строк в буфер;

– y w — скопировать слово в буфер.

Вставка текста из буфера

– p — вставить текст из буфера после курсора;

– P — вставить текст из буфера перед курсором. Замена текста

– c w — заменить слово;

– n c w — заменить n слов;

– c $ — заменить текст от курсора до конца строки;

– r — заменить слово;

– R — заменить текст.

Поиск текста

– / текст — произвести поиск вперёд по тексту указанной строки символов текст;

– ? текст — произвести поиск назад по тексту указанной строки символов текст. 7. Чтобы заполнить строку символами $ можно использовать клавиши ni(вставить текст n раз).

8. Отменить некорректное действие, связанное с процессом редактирования, можно с помощью клавиши «.».

9. Характеристика основных групп команд режима последней строки:

Копирование и перемещение текста

– : n,m d — удалить строки с n по m;

– : i,j m k — переместить строки с i по j, начиная со строки k;

– : i,j t k — копировать строки с i по j в строку k;

– : i,j w имя-файла — записать строки с i по j в файл с именем имя-файла.

Запись в файл и выход из редактора

– : w — записать изменённый текст в файл, не выходя из vi;

– : w имя-файла — записать изменённый текст в новый файл с именем имяфайла;

– : w ! имя-файла — записать изменённый текст в файл с именем имяфайла;

– : w q — записать изменения в файл и выйти из vi;

– : q — выйти из редактора vi;

– : q ! — выйти из редактора без записи;

– : e ! — вернуться в командный режим, отменив все изменения, произведённые со времени последней записи.

10. Определить, не перемещая курсора, позицию, в которой заканчивается строка, можно используя клавишу $ (переход в конец строки).

11. Опции редактора vi позволяют настроить рабочую среду. Для задания опций

используется команда set (в режиме последней строки):

– : set all — вывести полный список опций;

– : set nu — вывести номера строк;

– : set list — вывести невидимые символы;

– : set ic — не учитывать при поиске, является ли символ прописным или

строчным.

Если вы хотите отказаться от использования опции, то в команде set перед именем опции надо поставить no.

12. Определить режим работы редактора vi можно по последней командной строке.

13. Взаимосвязь режимов работы редактора vi:

«Командный режим» - «Режим вставки»

\ /

«Режим командной строкилово LOCAL.

![](image/7.bmp)

5. Перешёл в режим вставки и набрал следующий текст: local, нажал Esc для возврата в командный режим.

![](image/8.bmp)

6. Установил курсор на последней строке файла. Вставил после неё строку, содержащую следующий текст: echo $HELLO.

![](image/9.bmp)

7. Нажал Esc для перехода в командный режим.

8. Удалил последнюю строку.

![](image/10.bmp)

9. Ввёл команду отмены изменений u для отмены последней команды.

![](image/11.bmp)

10. Ввёл символ «:» для перехода в режим последней строки. Записал произведённые изменения и вышел из vi.


# Выводы

- Познакомилась с операционной системой Linux, получила практические навыки работы с редактором vi, установленным по умолчанию практически во всех дистрибутивах.

# Ответы на контрольные вопросы
1.Краткая характеристика режимов работы редактора vi:

– командный режим — предназначен для ввода команд редактирования и навигации по редактируемому файлу;

– режим вставки — предназначен для ввода содержания редактируемого файла;

– режим последней (или командной) строки — используется для записи изменений

в файл и выхода из редактора.

2. Выйти из редактора, не сохраняя произведённые изменения, можно используя клавиши «:q!» в командном режиме.

3. Краткую характеристика команд позиционирования:

– 0 (ноль) — переход в начало строки;

– $ — переход в конец строки;

– G — переход в конец файла;

– n G — переход на строку с номером n.

4. Для редактора vi словом является: пробел; буквы, находящиеся между двумя пробелами.

5. Из любого места редактируемого файла перейти в конец файла можно с помощью клавишы G и курсора вниз, а в начало – курсор вверх.

6. Краткая характеристика основных групп команд редактирования:

Вставка текста

– а — вставить текст после курсора;

– А — вставить текст в конец строки;

– i — вставить текст перед курсором;

– n i — вставить текст n раз;

– I — вставить текст в начало строки.

Вставка строки

– о — вставить строку под курсором;

– О — вставить строку над курсором. Удаление текста

– x — удалить один символ в буфер;

– d w — удалить одно слово в буфер;

– d $ — удалить в буфер текст от курсора до конца строки;

– d 0 — удалить в буфер текст от начала строки до позиции курсора;

– d d — удалить в буфер одну строку;

– n d d — удалить в буфер n строк. Отмена и повтор произведённых изменений

– u — отменить последнее изменение;

– . — повторить последнее изменение.

Копирование текста в буфер

– Y — скопировать строку в буфер;

– n Y — скопировать n строк в буфер;

– y w — скопировать слово в буфер.

Вставка текста из буфера

– p — вставить текст из буфера после курсора;

– P — вставить текст из буфера перед курсором. Замена текста

– c w — заменить слово;

– n c w — заменить n слов;

– c $ — заменить текст от курсора до конца строки;

– r — заменить слово;

– R — заменить текст.

Поиск текста

– / текст — произвести поиск вперёд по тексту указанной строки символов текст;

– ? текст — произвести поиск назад по тексту указанной строки символов текст. 7. Чтобы заполнить строку символами $ можно использовать клавиши ni(вставить текст n раз).

8. Отменить некорректное действие, связанное с процессом редактирования, можно с помощью клавиши «.».

9. Характеристика основных групп команд режима последней строки:

Копирование и перемещение текста

– : n,m d — удалить строки с n по m;

– : i,j m k — переместить строки с i по j, начиная со строки k;

– : i,j t k — копировать строки с i по j в строку k;

– : i,j w имя-файла — записать строки с i по j в файл с именем имя-файла.

Запись в файл и выход из редактора

– : w — записать изменённый текст в файл, не выходя из vi;

– : w имя-файла — записать изменённый текст в новый файл с именем имяфайла;

– : w ! имя-файла — записать изменённый текст в файл с именем имяфайла;

– : w q — записать изменения в файл и выйти из vi;

– : q — выйти из редактора vi;

– : q ! — выйти из редактора без записи;

– : e ! — вернуться в командный режим, отменив все изменения, произведённые со времени последней записи.

10. Определить, не перемещая курсора, позицию, в которой заканчивается строка, можно используя клавишу $ (переход в конец строки).

11. Опции редактора vi позволяют настроить рабочую среду. Для задания опций

используется команда set (в режиме последней строки):

– : set all — вывести полный список опций;

– : set nu — вывести номера строк;

– : set list — вывести невидимые символы;

– : set ic — не учитывать при поиске, является ли символ прописным или

строчным.

Если вы хотите отказаться от использования опции, то в команде set перед именем опции надо поставить no.

12. Определить режим работы редактора vi можно по последней командной строке.

13. Взаимосвязь режимов работы редактора vi:

«Командный режим» - «Режим вставки»

          \ /

«Режим командной строки