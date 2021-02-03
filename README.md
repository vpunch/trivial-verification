# trivial-verification

## Учись

[Математические методы верификации схем и программ](
https://mk.cs.msu.ru/index.php/%D0%9C%D0%B0%D1%82%D0%B5%D0%BC%D0%B0%D1%82%D0%B8%D1%87%D0%B5%D1%81%D0%BA%D0%B8%D0%B5_%D0%BC%D0%B5%D1%82%D0%BE%D0%B4%D1%8B_%D0%B2%D0%B5%D1%80%D0%B8%D1%84%D0%B8%D0%BA%D0%B0%D1%86%D0%B8%D0%B8_%D1%81%D1%85%D0%B5%D0%BC_%D0%B8_%D0%BF%D1%80%D0%BE%D0%B3%D1%80%D0%B0%D0%BC%D0%BC)

[Чья-то лаба](https://github.com/arkuzmin/verification)

[Лекции по модальной логике](
https://www.youtube.com/playlist?list=PL6ZCZFyULOwfPPGgNQcRB7IEzgJM13y-C)

[Лекции по верификации](
https://www.youtube.com/watch?v=EnWNYAyQqxo&list=PL-_cKNuVAYAUw3pNeradNr8zwOXKQ1IZA)

[Лекции по верификации от Савенкова](
https://www.youtube.com/user/ksavenkov/playlists)

## Spin

[Документация](http://spinroot.com/spin/Man/promela.html)

[Краткий гайд](http://spinroot.com/spin/Man/Quick.html)

[Гайд](http://spinroot.com/spin/Man/Manual.html)

[Адекватная подсветка синтаксиса для Vim](
https://github.com/blyoa/vim-promela-syntax)

[Синтаксис LTL](http://spinroot.com/spin/Man/ltl.html)

Модель описывается на языке Promela (PROcess MEta LAnguage). Для верификации
Spin генерирует программу на C.

Получить все контрпримеры (error trails) не получится, только один.

Отрицание свойства называется *never claim*.

Верифицировать:

```
spin -run main.pml
```

Если модель не соответствует спецификации, то контрпример будет записан в файл
с расширением `.trail`. Чтобы выполнить на нем симуляцию с выводом
диаграммы последовательности:

```
spin -t -M main.pml
```

Функции для генерации случайных значений нет. Ее наличие бы значительно
усложнило верификацию, так как проверяются все варианты работы системы.

## NuSMV


