# Шифрование методом Цезаря

## Цель

Изучить способ шифрования методом Цезаря. Реализовать программный интерфейс, реализующий данный метод. 

## Описание метода

Шифр Цезаря, также известный как шифр сдвига, код Цезаря или сдвиг Цезаря – один из самых простых и наиболее широко известных методов шифрования.

Шифр Цезаря – это вид шифра подстановки, в котором каждый символ в открытом тексте заменяется символом, находящимся на некотором постоянном числе позиций левее или правее него в алфавите. Например, в шифре со сдвигом вправо на 3, А была бы заменена на Г, Б станет Д, и так далее.

Шифр назван в честь римского императора Гая Юлия Цезаря, использовавшего его для секретной переписки со своими генералами.

Шаг шифрования, выполняемый шифром Цезаря, часто включается как часть более сложных схем, таких как шифр Виженера, и всё ещё имеет современное приложение в системе ROT13. Как и все моноалфавитные шифры, шифр Цезаря легко взламывается и не имеет почти никакого применения на практике.

## Исходные данные 

Текст

## Принцип работы метода

Если сопоставить каждому символу алфавита его порядковый номер (нумеруя с 0), то шифрование и дешифрование можно выразить формулами модульной арифметики:

**y = ( x + k ) mod n**
**x = ( y - k + n) mod n**,

где **x** – символ открытого текста, **y** – символ шифрованного текста, **n** – мощность алфавита, **k** – ключ.

С точки зрения математики шифр Цезаря является частным случаем аффинного шифра.

Шифрование с использованием ключа k = 3. Буква «Е» «сдвигается» на три буквы вперёд и становится буквой «З». Твёрдый знак, перемещенный на три буквы вперёд, становится буквой «Э», буква «Я», перемещенная на три буквы вперёд, становится буквой «В», и так далее.

Исходный алфавит:

**А Б В Г Д Е Ё Ж З И Й К Л М Н О П Р С Т У Ф Х Ц Ч Ш Щ Ъ Ы Ь Э Ю Я _**

Оригинальный текст:

**СЛУЧАЙНАЯ ПОСЛЕДОВАТЕЛЬНОСТЬ ЯВЛЯЕТСЯ СМУТНЫМ ПОНЯТИЕМ, ОЛИЦЕТВОРЯЮЩИМ ИДЕЮ ПОСЛЕДОВАТЕЛЬНОСТИ, В КОТОРОЙ КАЖДЫЙ ЧЛЕН ЯВЛЯЕТСЯ НЕПРЕДСКАЗУЕМЫМ ДЛЯ НЕПОСВЯЩЕННЫХ**

Шифрованный:

**ФОЦЬГРГБВТСФОИЗСЕГХИОЮРСФХЮВБЕОБИХФБВФПЦХРПВТСРБХМИПВСОМЩИХЕСУБАЭМПВМЗИАВТСФОИЗСЕГХИОЮРСФХМВЕВНСХСУСВНГКЗВЬОИРВБЕОБИХФБВРИТУИЗФНГЛЦИППВЗОБВРИТСФЕБЭИРРШ**

Шифрованный текст получается путём замены каждой буквы оригинального текста соответствующей буквой шифрованного алфавита.
