# Palindrome Chain Length

[Kata's Link](https://www.codewars.com/kata/525f039017c7cd0e1a000a26)

```python

def palindrome_chain_length(n):
    step = 0
    while True: #this is bad
        if str(n) == str(n)[::-1]:
            return step
        n = n + int(str(n)[::-1])
        step += 1

```
