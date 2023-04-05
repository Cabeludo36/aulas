A notação Big "O" nos permite descrever a complexidade do nosso coódigo algebricamente de uma maneira que podemos estimar quão rapido ou lento nosso código funcionara quando colocado sob pressão de grandes quantidades de dados.

O Big O não vai fornecer uma resposta exata sobre quanto tempo um pedaçõ de código levará para ser executado, mas nos permite discutir nosso código algebricamente para ter uma noção da rapidez com a pressão de grandes conjuntos de dados

Sempre esfatizamos o pior caso, pois, queremos determinar a quantidade maxima de tempo que um processo pode levar para entender os limites do código analisado a fim de evitar soluções ruimns, isso garante que uma soluição não demorara mais do que se espera e garante que o algoritimo não terá problemas de tempo no futuro

- Como um tempo de execução O(n) se compara a outros tempos de execução?
- Quais tempos de execução podemos esperar para diferentes tipos de soluções?
- Cada algoritimo terá seu tempo próprio de execução, mas podemos esperar ver sendo executado com bastante frequência o o seguinte: 
  | Sim                | Nome |
  | ------------------ | ---- |
  | $O(log_n)$         | n    |
  | $O(n)$             | n    |
  | $O(n\text{ }log_n)$ | n    |
  | $O(n^2)$           | n    |
  | $O(n!)$            | n    |
  
  A lista acima está ordenada por eficiencia, algoritmos que rodam em $O(logn)$ rodam muito mais rapido do que algoritimos que rodam em $O(n!)$
  
  ![](../diagramas/GraficoAlg1.svg)
  
### Definição matemática formal
Dada duas funções de complexidade de tempo de algorítimos:

$f(n)\text{ e }g(n)$

A definição matemática estabelece que:

$f(n)=O(g(n))$

Se, existirem constantes positivas $c\text{ e }n_0$ para todos os $n>=n_0$

## Exemplos
#### 1 -
$4n+1=O(n)$
(Ẽ-se "$4n+1$" é $O(n)$)
Pela definição precisamos demonstrar que existe uma constante $c$ e um valor positivo $n_o$ de forma que, para todos os valores de $n$ maiores ou igual á $n_0$, $4n+1$ sempre seja menor ou igual a $c \text{ x } n$. 
Resumindo:
$4n+1=<c\text{ x }n$ 