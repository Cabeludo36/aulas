Com a quantificação das etapas geradas pelo modelo RAM podemos comparar varios algoritimos uns com os outros e afirmar de maneira mais precisa qual é mais rápido, pois, independente da velocidade dos computadores nos quais são executados uma menor quantidade de etapas sempre apresentará um desempenho melhor para grandes volumes de dados processados.


Veremos o código de um programa simples para começar a explicar a tecnica analítica da contagem de etapas. 
Para realaizar este processo, basta contar, linha por linha, aquantidade de instruções realizadas por cada comando.
### Algoritimo
```java
Scanner sc = new Scannner(System.ini); // 1
int idade; // 1
System.out.println("Digite sua idade:"); // 1
idade = sc.nextInt(); // 2 leitura + atribuição

if (idade >= 18) // 1
	System.out.println("Maior de idade"); // ? 1
else
	System.out.println("Menorde de idade");
// T(n) = 7
// Complexidade constante
```
### Analise de algoritimos lineares
```java
public static void printArray(int[] A) {
	   //    1        n+1         n
	for(int i = 0; i < A.length; i++) {
		System.out.println(A[i]+"\n"); // n
	}
}
// T(n) = 3n + 2
// Complexidade linear
```
### Algoritimo quadratico
```c
matriz[n,m]
    //1     n+1    1
for(i = 0; i < n; i++) {
	//    1         n+1   n
	for(int j = 0; i < n; i++) {
		Scanf("%d", & matriz[i][j]); // n
	}
}
// (1+n+1+n) * (1+n+1+n) + n
// (2n+2)² + n
// T(n) = 4n² + /4n/ + 4 + /n/
// T(n) = 4n² + 5n + 4
// Complexidade quadratica
```
### Comparação entre algoritimos
| Algoritimo A         | Algotitimo B     |
| -------------------- | ---------------- |
| $T(n)=\frac{n^2}{2}$ | $T(n)=100n+1000$ |

**Qual o algoritimo mais eficiente?**

| $T(n)=\frac{n^2}{2}$ |                 | $T(n)=100n+1000$ |                 |
| -------------------- | --------------- | ---------------- | --------------- |
| **n**                    | **QTDE Instruções** | **n**                | **QTDE Instruções** |
| 208                  | 21632           | 208              |       21800          |
| 209                  | 21840,5         | 209              |       21900          |
| 210                  | 22050           | 210              |        22000         |
| 211                  | 22260,5         | 211              |        22100         |

| Representação | Nome               |
| ------------- | ------------------ |
| $n!$          | Fatorial           |
| $2^2$         | Exponencial        |
| $n^k$         | Polinomial         |
| $n^2$         | Quadratico         |
| $n\text{ } log_n$     | Linear Logaritmico |
| $N$           | linear             |
| $log_n$       | Logáritmico        |
| $1$              |     constante               |

