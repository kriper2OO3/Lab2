# Сортировка выбором

Сортировка выбором заключается в поиске на необработанном срезе массива или списка минимального значения и в дальнейшем обмене этого значения с первым элементом необработанного среза.

![image](https://github.com/kriper2OO3/Lab2/blob/main/Selection-Sort-Animation.gif)

### Алгоритм сортировки:

```py
def sort_select(lst):
    for i in range(len(lst), 1, -1):
        min = -999999999
        for j in range(i):
           if lst[j] >= min:
                min, t = lst[j], j
        lst[i - 1], lst[t] = lst[t], lst[i - 1]
    return(lst)
```
### Описание алгоритма.

На вход подаётся рандомно сгенерированный неотсортированный список элементов. Функция состоит из 2 циклов "for". Внешний цикл "for" перебирает номера элементов массива c шагом в -1. Перед вложенным циклом устанавливается наименьшее значение в переменну ***min***. Вложенный цикл 

### Таблица с данными роста времени в зависимости от количества элементов:

> |Количество элементов(ед.)|Сортировка выбором(сек.)|Сортировка вставками(сек.)|Пузырьковая сортировка(сек.)|Пузырьковая улучшенная сортировка(сек.)|
> |-------------|----------|---|----|----|         
> |-------------|----------|---|----|----|
> |-------------|----------|---|----|----|
> |                     1000|                    0.05|                      0.06|                         0.1|                                   0.11|
> |                    10000|                    4.32|                      5.04|                       10.45|                                  11.04|
