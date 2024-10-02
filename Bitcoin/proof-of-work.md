# Parte 3

# Proof of work

- hash bloco
- hash anterior
- nonce
- TXs

O minerador que tem o direito de adcionar o proximo bloco, é o primeiro que encontrar um bloco  cujo hash possuo um determinado numero de zeros no começo, esse numero de zeros é chamada de dificuldade e é constantemente atualizada, um bloco novo deve surgir a cada 10 min aproximadamente, quando um minerador encontrar, ele avisa a todos os outros e esse bloco entra na blockchain, assim todos começam a minerar apartir desse novo bloco.

Uma das formas pelos quais os mineradores rebcebem é através das tarifas de transções, ao realizar uma transação sempre existe um pequeno excedente do valor da transação que fica para os mineradores, mas atualmente a principal forma de remuneração dos mineradores é através da coin base transection, o minerador que encontra o proximo bloco da blockchain possui o direito de realizar essa transação em que cria um determinado numero de bitcoins novos que pode enviar para quem ele desejar, normalmente ele mesmo, quando o numero maximo de bitcoins existir(21 milhões) ele so vai receber através do excedente das transações.

A quantidade que o minerador pode gerar em uma coin base transection é bem definida, e a cada 4 anos ela cai pela metade, no inicio do bitcoin cada coin base transection criava 50 novos bitcoins, todos os bitcoins foram criados através da coin base transection, todo o dinheiro dos bitcoins foi devido os mineradores.

**Dificuldade na mineração:**

- Um computador convencional demoraria muito tempo para minerar algum novo bloco.
- Minerar bitcoin é um negócio com investimento consideráveis em hardware específico(ASICs).

**Mining Pools:**

Possui algo como um coordenador, varios mineradores se jutam com esse coordenador para minerar um novo bloco no bloco dele, caso algum ache um novo bloco ele envia ele para o coordenador, ele então divide a recompensa por achar um novo bloco entre todos os mineradores proporcionalmente ao trabalho realizado por cada um deles. Com isso eles reduzem o risco da mineração, pois assim eles recebem um fluxo mais constante, ao inves de ariscar a possibilidade de achar ou não algo, eles também selecionam a moeda que está dando mais lucro no momento para selecionar qual vai ser minerada no momento.