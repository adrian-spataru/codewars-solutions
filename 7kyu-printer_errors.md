# Printers Error 

[Kata's Link](https://www.codewars.com/kata/56541980fa08ab47a0000040)

```python

def printer_error(s):
    return "".join(str(len(s.translate(str.maketrans(dict.fromkeys('abcdefghijklm')))))+"/"+str(len(s)))
```
