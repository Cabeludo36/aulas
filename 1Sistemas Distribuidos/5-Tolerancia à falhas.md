1. Introdução
	- SDs São construidos por vários processadores independentes;
	- Diferencian de computadores paralelos pelo acoplamento fraco entre os nodos;
	- Tambem não tem acesso a um relogio global;
	- Elementos não homogêneos e assíncronos;
	- A área de tolerancia á falhas em sistemas distribuidos é vasta.
2. Motivações
	- Um SD deve operar sem interrupção, com pequena queda de desempenho, mesmo com qualquer tipo de falha;
	- SDs de tempo-real diferem dos sistemas convencionais por apresentarem restrições de tempo e situações criticas;
	- Qualquer tipo de falha, inclusivefalha temporal, pode causar consequencias irreparaveis.
3. Falhas em sistemas distribuidos
	- Modelos classicos de falhas para sistemas distribuidos;
	- Modelo de Chistian: Falhas chrash, omissão temporização, resposta e modelo de Schneider-Arbitraria;
	- Falhas que afetam as trocas de mensagem entre nodos;
4. Processadores Fail-stop e armazenamento estável
	- O sistema deve preservar seu estado global mesmo na presença de falhas;
	- Armazenamento estável;
	- Lembrando: falhas podem ocorrer inclusive no armazenamento secondario ou seja, disco magnetico ou ótico;
	- Armazenamento estável ideal é apenas uma abstração teórica;
	- Para toda e qualquer operação na presença de uma falha interna irrecuoperavel: Fail-Stop
5. Tratamento de falhas
	- Detecção de falhas - checksum;
	- Mascaramento de falhas - retransmissão;
	- Tolerar flhas - Não é pratico tratar todas;
	- Recuperação de falhas - rollback
	- Redundância

Notas:
- nodos não podem ter processadores diferentes, porem podem ter mais memoria;