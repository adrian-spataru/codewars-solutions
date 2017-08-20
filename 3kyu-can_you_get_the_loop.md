# Can you get the loop?

[Kata's Link](https://www.codewars.com/kata/52a89c2ea8ddc5547a000863)

```python

def loop_size(node):
    a = {}
    while True:
        if a.has_key(node):
            leader = node
            count = 1
            while node.next !=  leader:
                node = node.next
                count +=1
            return count
        a[node] = 0
        node = node.next
            

```
