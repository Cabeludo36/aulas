$f(n) = O(g(n))$

"Lê-se $f(n)$ é Big O de $g$ de $n$"

Se existirem constantes posicionadas $c$ e $n_0$ tais que $f(n)<= c \text{ x } g(n)$ para todos os $n>=n_0$ 
### Notação Big Omega(Ω)
A notação Ω nos fornece uma simbologia simplificada para representar um limite inferior de desempenho para um algoritimo. Isto é, um limite minimo de tempo que um algoritimo leva para ser executado
### Exemplos para função linear
**Quando dizemos:**
$4n-3$ é $Ω(n)$ ("lê-se" é ômega de n") estamos afirmando que o comportamento assimtótico de uma função linear é igual ou inferior ao dela.

Significa dizer que a função $4n-3$ nunca terá um comportamento de crescimento inferior ao de uma função com o comportamento linear.

Assim $Ω(n)$ apresenta-se como um limite inferior a $f(n)$

![](../diagramas/GraficoOmegaLinear.svg)

Da mesma forma $4n-3$ é $Ω(1)$ pois $f(n)$ funciona apresentará um comportamento de crescimento que seja ultrapassado por comportamento constante

![](../diagramas/BigOmegaConstante.svg)

#### Outro exemplo:
$4n-3$ não é $Ω(2^2)$ pois $f(n)$ nunca crescera a ponto de ultrapassar o comportamentp quadratico.

![](../diagramas/BigOmegaQuadratico.svg)

obs.: Não tera limite inferior por ter $n^2$ que passa da função $4n - 3$, por tanto não é $Ω$
### Definição matemática formal
$f(n)=Ω(g(n))$ ("lê-se $f(n)$ é $Ω(g(n))$") se existirem constantes positivas $c$ e $n_0$, tais que:

$f(n)>=c \times g(n)$ para todos os $n>=n_0$
### Exercicios:
Demonstrar que $4n+1$

$c=4$
| N   | $4n+1$ | >=  | $c \times n$ |
| --- | ------ | --- | ------------ |
| 1   | 5      | >   | 4            |
| 2   | 9      | >   | 8            |
| 3   | 13     | >   | 12           |
| 4   | 17     | >   | 16           |
| 5   | 21     | >    | 20           |

### Notação Big O
A notação O nos fornece uma simbologia para representar um limite exato de tempo que um algoritimo leva para ser executado, ou seja, a notação O representa o ponto de encontro entre as notação Ω (limite inferior) e Big O(limite superior)
#### Definição matemática formal
Dada duas definições de complexidade de tempo: $f(n)$ e $g(n)$ a deninição estabelece que:

$f(n) = O(g(n))$ ("lê-se $f(n)$ é $O(g(n))$")

Se existissem duas constantes positivas $c_1$ e $c_2$ e um valor $n_0$, tais que:

$c_1 \times g(n) <= f(n) <= c_2 \times g(n)$ 

para todos os $n>=n_0$ 

Provar que $4n+1$ é $O(n)$

$c_1=4$

$c_2=5$

| n   | $4n$ | $4n+1$ |     | 5n  |
| --- | ---- | ------ | --- | --- |
| 1   | 4    | 5      |     | 5   |
| 2   | 8    | 9      |     | 10  |
| 3   | 12   | 13     |     | 15  |
| 4   | 16   | 17     |     | 20  |
| 5   | 20   | 21     |     | 25    |
