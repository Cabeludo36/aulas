<style>
	tab {
		tab-size: 2;
	}
</style>
Existem tipos de plataformas de R.V. fundamentada em projeções: Tela panorâmica, mesa digital e cavernas digitais.<br>
Permitem a manipulação de imagens de tamanho real e, favorece trabalhos colaborativos com participação simultânea de varias pessoas.
## Dispositivos Somaticos
- **Data Gloves**:<br>
	Uma forma de comunicar as ações do usuário ao ambiente virtual e usar gestos capturados por luvas, podendo até "simular" formas geometricas que possam ser interagidas.
- **Sistemas de Interfaces não-convencionais**:<br>
	A exploração do ambiente virtual é feito usando-se interfaces não-convencionais, implemantando a imersão total a partir de processamentos cíclicos de informações tipicas de sistemas de R.V., podendo ser representada como: 
	
	![](../diagramas/DiagramaNaoConvencional.svg)

	Para não causar desconforto e garantir a condição de presença do usuário, o tempo de latência deve ser baixo (menor que 20ms).
	Nunca zero, pois o computadir precisa de tempo para rastrear movimentos e renderizar novas imagens.
	Para alcançar um tempo de latência, algumas abordagens são utilizadas, como:
	- Utilizar tecnicas de timewarp/reprojection;
	- Diminuir o tempo de atualização de todos os pixels;
	- Otimização do buffer da GPU;
	- Previsão do movimento da cabeça do usuário.
- **Coordenadas, transformações e projeções**
	Os modelos (topologia) dos objetos não mudam numa cena virtual, mas sua representação dos objetos mudam constantemente em respostaaos movimentos e ações do usuário
	Tais mudanças podem ser implementadas por uma série de operações matematicas denominadas transformações geomátricas de coordenadas
	- Coordenada:<br>
		Sistema cartesiano de coordenadas é empregado na descrição das transformações de coordenadas.
	- Transformações:<br>
		Modelo de transformações, escalonamento, cisalhamento, reflexão, rotação.
- **Projeção Geometrica**
	Conversão genérica de entidades de uma dada dimensão para outra de menor ordem. A finalidade da projeção na C.G. é converter os modelos tridimencionais em imagens bidimencionais.
	Para sua representação em um plano bidirecional, devem ser considerados os elementos basicos:
	- Plano de projeção:<br>&emsp;
		Superficie onde será projetado o objeto.
	- Raios de projeção(ou projetoras):<br>&emsp;
		São retas que passam pelos pontos dos objetos e pelo centro de projeção.
	- Centro de projeção:<br>&emsp;
		Ponto fixo onde os raios de projeção partem.
