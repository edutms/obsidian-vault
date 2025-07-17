2024-11-02 09:49

### Status:  #child

### Tags: [[software-engineering]]

# Big O Notation

O(1) --> Constant time:
- independente do input o tempo para pegar o elemento será sempre o mesmo
```
def get_first_element(arr): 
	return arr[0]
```
Seja o array de tamanho 2 ou 10ˆ3 o tempo será o mesmo


O(log n) --> logarithmic time:
- o input cresce muito mais rápido que o tempo de execução, o que é de certa forma ótimo
	- log2(10) = 3.321
	- log2(20) = 4.321
	- log2(40) = 5.321
- Isso é o que acontece numa binary search:
	- Quebrando a array pela metade em cada caso de "falso", você aumenta o tempo de execução em uma proporção logarítmica frente ao tamanho do input
	- ![[Pasted image 20241102100835.png]]

O(n) - linear time:
- tempo linear, conforme o input aumenta o tempo de execução aumenta proporcionalmente

O(n log n) - linearithmic time:
- Junção de O(log n ) e O(n), uma parte do algoritmo escalando com certa parte
- Olhar `MergeSort`

O (nˆ2) - Quadratic time:
- conforme o input aumenta, o aumento do tempo de execução tem um aumento quadrático
- nestar For Loops é um exemplo 

O(2ˆn) - exponential time:

O(n!) - factorial time:
- 

# References









