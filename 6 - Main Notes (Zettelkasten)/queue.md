2024-11-02 10:42

### Status: #child

### Tags: #dsa #cs
# queue
First In, First Out (FIFO)

Queue é uma estrutura de dados utilizada para fazer buffering ou streaming de dados e utiliza [[Linked List]] para ser feita.

Se corretamente implementada, ela mantém uma ref de Head e Tail para adicionar e remover elementos para manter a lógica como O(1).

### Dequeue

```
from queue import Queue
from collections import deque

q = Queue()

q.put(1)
q.put(2)
q.put(3)

print(q.get())
print(q.get())

```

Esse código vai printar 1 e 2, respectivamente.

Em Python, uma queue é implementada via deque





# References









