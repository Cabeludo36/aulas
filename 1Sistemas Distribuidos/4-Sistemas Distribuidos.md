![](../diagramas/Arquitetura9.svg)
### Processos e threads
- Movimentar processos entre máquinas diferentes em SD;
- Migração de processos, ou migração de código, ajuda a aumentar a escalabilidade
- Tambem pode ajudar a configurar dinamicamente clientes e servidores;
- Formam a base para a cominicação entre maquinas diferentes;
- São organizados internamente e suportam ou não varias threds de continuidade;
- Threads são úteis para continuar usando a CPU quando é realizada uma operação bloqueada de E/S
### Threads
- A granularidade sob a forma de multiplos threds de controle por processo facilita a construção de aplicações distribuidas e a obtenção de melhor desenpenho
- O contexto de thread consiste um contexto de CPU, junto com algumas informações para gerenciamento de threads;
- Elas proporcionam um meio conveniente de permitir chamadas bloqueadas de sistemas sem bloquear o processo interno.
### Comunicação
1. **Forma de comunicação**
   - Direta:

      send: Há indicação do processo receptor
         
      Exemplo: 

	      `send(process, msg)`
     receive: Há indicação do emissor
      Exemplo: 

	      `receive(process, msg)`
   - Indireta:

     send: Envio para uma porta ou mailbox como reconhecimento de qual será o receptor.

     Exemplo: 

	     `send(mailbox, msg)`
     receive: Obtenção da msg guardada no mailbox, possivelmente desconhecendo a origem.

     Exemplo: 
     
	     `receve(mailbox, msg)`
2. **Troca de mensagens**
   - As mensagens são objetos de dados cuja estrutura e aplicação são definidas pelas aplicações que o usarão
   - Feitas através de primitivas de comunicação `send` e `receve`
3. **Forma de sincronização**
   - Síncrono ou bloqueante
   - Assíncrono ou não-bloqueante
   **Endereçamento**
	   1. Um identificador único de processo na mesma maquina;
	   2. Endereçamento indicando o processo e a máquina;
	   3. Processos escolhem endereções que são detectados por brodcast;
	   4. Uso de um servidor de nomes.
4. **Primitivas confiaveis e não-confiaveis de comunicação**
   - Se as mensagens envolvidas na comunicação cliente/servidor for assumida como não-confiaveis , recairá ao usuario a tarefa de controlar possiveis perdas de mensagens. Isso não é desejavel;
   - O Kernel do S.O. deve se preocupar em verificar se as mensagens foram corretamente recebidas garantindo comunicação confiável.
5. **RCP - Remote Procedure Call**
   - Permite que programas invoquem procedimentos localizados em outras máquinas como se ele estivesse localmente definido.
   - Chamador e chamado executam em espaços de endereçamento diferentes;
   - Possibilidades de falhas.
   **Operação básica**
	   1. Oprocedimento chama o stub cliente como se fosse um procedimento local qualquer;
	   2. O stub cliente constrói a mensagem e passa ao kernel;
	   3. O kernel remoto envia a msg ao stub servidor;
	   4. O kernel remoto entrga a msg ao stub servidor;
	   5. O stub servidor desempacota os parametros e chama o servidor;
	   6. O servidor realiza o trbalho e envia o resultado ao stub servidor;
	   7. O stub servidor empacorta o resultado em uma msg e passa para o kernel;
	   8. O kernel remoto envia a msg ao kernel cliente;
	   9. O kernel cliente entrega a msg ao stub cliente.
	   10. Ostub desenpacota o resultado e retorna ao cliente.
	- Stubs são gerados automaticamente pelo compilador e são a parte da aplicação que se conecta com a rede.
6. **Sêmantica RPC na presença de falhas**
   - Existem cinco classes diferentes de falhas possiveis
   1. O cliente não consegue encontrar o servidor
   2. Mensagem de requisição perdida
   3. Mensagem de resposta perdida
   4. Servidor cai após receber a requisição
   5. O cliente falha após a requisição