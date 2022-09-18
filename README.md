1- Bir listeyi düzleştiren (flatten) fonksiyon yazın. Elemanları birden çok katmanlı listelerden ([[3],2] gibi) oluşabileceği gibi, non-scalar verilerden de oluşabilir.

Örnek olarak:

**input: [[1,'a',['cat'],2],[[[3]],'dog'],4,5]**

**output: [1,'a','cat',2,3,'dog',4,5]**


```python
flat_list = []
def flatten_list(x):
    for i in x:
        if type(i) == list:
            flatten_list(i)
        else:
            flat_list.append(i)
    return flat_list

liste = [[1,'a',['cat'],2],[[[3]],'dog'],4,5]

print('Orjinal Liste', liste)
print('Düzeltilmiş Liste', flatten_list(liste))
```

2- Verilen listenin içindeki elemanları tersine döndüren bir fonksiyon yazın. Eğer listenin içindeki elemanlar da liste içeriyorsa onların elemanlarını da tersine döndürün.

Örnek olarak:

**input: [[1, 2], [3, 4], [5, 6, 7]]**

**output: [[[7, 6, 5], [4, 3], [2, 1]]**
