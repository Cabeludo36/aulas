O metodo analitico é uma maneira mais assertiva de realizar a analize de algoritimos. Ele não tem o objetivo de calcular o tempo de execução em segundos, minutos ou alguma outra apresentação de tempo. 
Ele visa emcontrar uma expressão matemática para tradizir o desemprenho do algoritimo em quantidade de etapas. 
Desta forma, consegue-se medir o desenpenho do algoritimo da maneira totalmente independente de linguagens de programação, de compiladores e de outros fatores fisicos que possam invalidar a anilise.

## Modelo RAM
O modelo RAM (Random Acesses Machine) é a estratégia utilizada para média o desempenho de forma analitica. Ele realiza a contagem das etaás que um algoritimo executa e ignora todos os aspectos de velocidade de processamento ou qualquer tipo de otimização de hardware.
Neste modelo, cada operação (tais como: atribuições, comparações e inicializações, etc) consome um custo computacional e constante e único
### Exemplos de Operações computacionais com mesmo custo
| atribuições                      | custo |
| -------------------------------- | ----- |
| `int valor = 0;`                 | 1     |
| `float sal = 2005.15;`           | 1     |

| Incremento/Decrecimento de valor | Custo |
| -------------------------------- | ----- |
| `valor++;`                       | 1     |
| `valor++;`                       | 1      |

| Operações matemáticas Complexas | Custo |
| ------------------------------- | ----- |
| `valor*(4/Math.sqrt(9));`       | 1     | 

| Acesso à elementos de arranjos | Custo |
| ------------------------------ | ----- |
| `lista[i];`                     | 1     | 

| Operações logicas | custo |
| ----------------- | ----- |
| `if(valor > 10)`  | 1     |
| `if(valor==3 or valor==2)`      |  1     |

| operações de escrita/leitura       | custo |
| ---------------------------------- | ----- |
| `System.out.println("Olá Mundo");` | 1     |
| `scanner.nextInt();`                  | 1

É obvio que estas operações possuem diferenças significativas de desempenho. Umas são mais rápidas de serem executadas doque outras, contudo estamos interessados em analisar o desempenho do algorítimo com base na quantidade de etapas, o Modelo RAM ignora tais diferenças.
### Exemplo:
```java
Scanner sc = new Scanner(System.int); // 1
int idade; // 1
System out println("Digite sua idade:"); // 1
idade = sc.nextInt(); // 2 (conversão e atribuição)
if (idade >= 18) // 1
	System.out.println("Maior de idade"); // 1 ? pode não ser executado
else
	System.out.println("Menor de idade"); // 1 ?
// Formula da Complexidade
// T(n) = 7
```

## Analise de algoritimos lineares
A analise anterior foi bem foi fácil e serve apenas para aprendizado basico. Vamos ver um exemplo um pouco mais complexo.
Um algoritimo que, dada um arranjo $A[]$ de $n$ valores, imprime todos os valores desse arranjo:
```java
public static void printArray(int[] A) {
	//       1         n+1          n
	for(int i = 0; i < A.length; i++) {
		System.out.println(A[i]+"\n"); // n
	}
}
// T(n) = 3n + 2
```

Este exercicio será corrigido na proxima aula
```java
public static void calcularMax(int[] A) {
	int maior = A[0]; // 1
	//       1       n          n-1
	for(int i = 1; i < A.length; i++) {
		if(maior < A[i]) { // n-1
			maior = A[i]; // n-1
		}
	}
	return maior; // 1
}
// T(n) = 4n
```
