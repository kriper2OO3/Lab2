# Сортировка выбором


def my_sort(lst):
    for i in range(len(lst), 1, -1):
        min = -999999999
        for j in range(i):
           if lst[j] >= min:
                min, t = lst[j], j
        lst[i - 1], lst[t] = lst[t], lst[i - 1]
    return(lst)
