# Задача по созданию модульного теста функции factorize

Дана функция `factorize(x)` со следующим контрактом:

    def factorize(x):
        """ Factorize positive integer and return its factors.
            :type x: int,>=0
            :rtype: tuple[N],N>0
        """
        pass

Написать комплект тестов:

1. `test_wrong_types_raise_exception`
2. `test_negative`
3. `test_zero_and_one_cases`
4. `test_simple_numbers`
5. `test_two_simple_multipliers`
6. `test_many_multipliers`

Проверить в них соответственно:

1. Что типы `float` и `str` (значения `string`, `1.5`) вызывают исключение `TypeError`.
2. Что для отрицательных чисел `-1`, `-10` и `-100` вызывается исключение `ValueError`.
3. Что для числа `0` возвращается кортеж `(0,)`, а для числа `1` кортеж `(1,)``
4. Что для простых чисел `3`, `13`, `29` возвращается кортеж, содержащий одно данное число.
5. Что для чисел `6`, `26`, `121` возвращаются соответственно кортежи `(2, 3)`, `(2, 13)` и `(11, 11)`.
6. Что для чисел `1001` и `9699690` возвращаются соответственно кортежи `(7, 11, 13)` и `(2, 3, 5, 7, 11, 13, 17, 19)`.

При этом несколько различных проверок в рамках одного теста должны быть обработаны как подслучаи с указанием `x: subTest(x=...)`.

**Решение**