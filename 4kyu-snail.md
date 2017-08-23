# Snail 

[Kata's Link](https://www.codewars.com/kata/521c2db8ddc89b9b7a0000c1)

```python

def snail(array):
    snail = []
    rotation = 3
    while array:
        if rotation is 0:
            snail.extend([a[len(array)] for a in array])
            array = [ a[:len(array)] for a in array]
            rotation = 1
        elif rotation == 1:
            snail.extend(array[len(array)-1][::-1])
            array = array[:len(array)-1]
            rotation = 2
        elif rotation == 2:
            snail.extend([a[0] for a in array][::-1])
            array = [ a[1:] for a in array]
            rotation = 3
        else:
            snail.extend(array[0])
            array = array[1:]
            rotation = 0

    return snail

```
