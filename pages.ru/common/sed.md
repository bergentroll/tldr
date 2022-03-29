# sed

> Редактировать текст в стиле сценариев.
> Смотрите также: `awk`, `ed`.
> Больше информации: <https://www.gnu.org/software/sed/manual/sed.html>.

- Выполнить указанное выражение:

`{{команда}} | sed '{{s/apple/mango/g}}'`

- Выполнить указанный скрипт:

`{{команда}} | sed --file={{путь/к/скрипту.sed}}`

- Выполнить указанный скрипт с включенными расширенными регулярными вырежениями:

`{{команда}} | sed --regexp-extended '{{s/(apple)/\U\1/g}}'`

- Выполнить указанное выражение без автоматического вывода буфера:

`{{команда}} | sed --quiet '{{1p}}'`

- Выполнить указанное выражение и заменить файл его выводом:

`sed --in-place '{{s/apple/mango/g}}' {{путь/к/файлу}}`

- Заменить строку указанной на всех строках (команда `[s]ubstitute`):

`{{команда}} | sed 's/{{регулярное_выражение}}/{{замена}}/g'`

- Вывести только первую строку (команда `[p]rint`):

`{{команда}} | sed --quiet '{{1}}p'`