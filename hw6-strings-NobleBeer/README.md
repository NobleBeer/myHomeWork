# ДЗ 6. Strings

## Дедлайн
**Мягкий дедлайн** - 6 ноября в 12-00

**Жесткий дедлайн** - 11 ноября в 23-59

## Как сдать
Реализуйте нужные классы. Запустите у себя на компьютере тесты. Для этого откройте консоль и выполните команду
```bash
./gradlew test
```

Если тесты прошли успешно - вы увидите надпись `BUILD SUCCESSFUL` , если же вы увидите надпись `BUILD FAILED`, то найдите в сообщении в терминале название теста и посмотрите этот тест в директории `src/test/groovy/`

После этого отправьте свое решение в ветку **main**. Призовите меня (ivanetc) в комментариях, где, **пожалуйста**, **напишите** "Cдаю задачи 1, 2, 3 ... n".
Убедитесь, что тесты проходят локально.

## Операции со строками и другими последовательностями
1. **isLowerCase** - Проверьте, что строка состоит только из строчных букв
2. **isUpperCase** - Проверьте, что cтрока состоит только из заглавных букв 
3. **isCamelCase** - Строка начинается с заглавной буквы, а все остальные строчные 
4. **isMixedCase** - Проверьте, что в строке чередуются буквы, т.е. первая заглавная, вторая строчная, 
третья заглавная и т.д. Или наоборот, первая строчная, вторая заглавная, третья строчная и т.д. 
Используйте конструкцию Character.isUpperCase(‘z’), чтобы определить, верно ли, что символ является заглавной буквой. (аналогично Character.isLowerCase())
5. **isPalindrome** Дана строка, проверьте, является ли она палиндромом. Т.е. верно ли, что если ее 
прочитать с конца в начало, то получится та же строка. Пробельные символы игнорируйте.
6. **isStrictPalindrome** Аналогично функции палиндрома, но функция имеет второй логический параметр 
strict, если он false, то при проверке нужно игнорировать регистр букв и пробелы.
7. **isAllCharactersPaired** Дана строка, проверьте, верно ли, что в ней все символы идут парами одинаковых. 
Например, для строки `aaBBccDD55**` нужно вернуть `True`, а для строки `aaBBcC**hF` нужно вернуть `False`.
8. **replaceBinaryNumbers** Напишите функцию, которой дается строка. Она должна поменять местами все 
использования 0 на 1, а все использования 1 на 0. Например,
`abc01xyz000111` должно превратиться в `abc10xyz111000`.
9. **replace** Добавьте в функцию _replaceBinaryNumbers_ два параметра: символы для замены. Т.е. заменять можно не только 0 на 1 и наоборот, а любой символ на любой. На самом деле, решить нужно эту задачу. А вариант с 0 и 1 нужен только для тренировки.
    * Чтобы решить задачу, попробуйте разобраться либо в методе `replace` для строк. Либо в паре методов `translate` и `maketrans`. Второй вариант предпочтительней, но чуть сложнее, чтобы разобраться.
10. **makeDragonCurve** Кривая дракона. В функцию передается один аргумент, целое число n>=0. Если передан 0, нужно вернуть строку `R`. Иначе нужно повторить n раз следующую операцию: допустим, на предыдущем шаге мы получили строку S. Нужно к ней приписать букву `R`, а потом приписать снова S, но, во-первых, прочитанную с конца, а, во-вторых, в которой буквы `R` заменены на буквы `L` и наоборот. Например, при n=1 получается `RRL` как `R` + `R` + `L`, при n=2 получается `RRLRRLL` = `RRL` + `R` + `RLL` и т.д.
11. **makeGrayCode** Коды Грея, часть 1. Создайте функцию, в которую передается один аргумент, целое число n>=0. Если передан 0, нужно вернуть строку `0`. Иначе нужно повторить n раз следующую операцию: приписать список из предыдущего шага к самому себе, вставив в середине число с номером шага. На примере это выглядит так:
```
n = 0     "0"
n = 1     "0 1 0"
n = 2     "0 1 0 2 0 1 0"
n = 3     "0 1 0 2 0 1 0 3 0 1 0 2 0 1 0"
...
```