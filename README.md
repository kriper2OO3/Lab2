# Сортировка выбором

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
