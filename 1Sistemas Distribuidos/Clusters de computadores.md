- Cluster ( ou clustering);
- Sistema que relaciona dois ou mais computadores;
- formado por nós (ou nodos)
- Não há limite teórico maximo de nós;
- comportamento "transporte" de um sistema distribuido;
- Pode usar computadores simples(PCs)
1. Tipos de clusters
	- Cluster de alto desempenho
	- Cluster de alta disponibilidade;
	- Cluster de balanceamento de carga;
	- é possivel combinações de tipos de clusters.
2. Funcionamento Basico
	- Hardware: equipamentos usados como nós
	- Podem ser nós dedicados ou não;
	- Sistema operacional homogênio;
	- Hetereogenidade pode levar a sistemas mais complexos;
	- middleware (exemplo: MPI);
	- nó controlador (mestre).
3. Algumas soluções de clusters
	- MOSIX (Multicomputer Operating System for Unix): Balanciamento de carga e alto desempenho;
		- Usa CPus e GPUs;
		- nó não dedicados;
		- Não é gratuito(OpenMosix).
	- OpenSSI (Single System Image): Focado em ambientes linux.
		- Alto desempenho e alta disponibilidade;
	- Kerrighed: Solução aberta para linux
		- Conceito de distributed shered Memory (DSM)
4. Vantagens e desvantagens
	- Resoltados tão bons ou até superior a super computadores
	- não é necessario depender de um unico fornecedor
	- A configuração de um cluster não custuma ser trvial;
	- Escala horizontal;
	- Software livre;
	- Facilidade de customização 
	- não oferece velocidade de transferência de dados
	- distancia geografica