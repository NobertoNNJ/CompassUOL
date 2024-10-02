# Parte 4

# Evitando O Gasto Duplo

Graças a  existencia do proof of work que não existe o gasto duplo.

*Gasto duplo:* Basicamente gastar o mesmo dinheiro duas vezes, usar os mesmo 5 bitcoins para pagar duas pessoas diferentes.

É possivel que dois blocos sejam encontrados basicamente no mesmo momento, os minerados que acharam os blocos vão espalhar essa noticia que acharam um bloco e isso vai causar uma certa divisão em que alguns acreditam que um bloco A é o certo e outros acreditam que o bloco B é o correto.

Com isso os mineradores divididos vão minerar naqueles que acreditam ser correto, ai que entra a regra que os mineradores sempre extendem o bloco mais longo da cadeia, com isso quando em um desses dois novos blocos for encontrado um novo bloco AA ele vai se tornar o mais longo e os mineradores que estavam no bloco B vão começar a minerar nesse novo bloco AA, apenas as transações que ocorreram nesse bloco B serão contabilizadas para esse novo bloco AA, o bloco B não vai entrar na blockchain nem o dinheiro do minerador que acho esse bloco B vai ser contabilizado.


Para garantir que uma transação com bitcoin seja validada o que está recebendo deve aguardar um certo numero de confirmações, quem está rececebendo deve aguardar que um novo bloco seja minerado em cima desse bloco que confirma que ele recebeu, normalmente são aguardado 6 confirmações, ou seja o bloco com minha transação e mais 5 outros blocos em cima desse bloco da transação, então caso alguem queira realizar esse gasto duplo seria necessario que ele conseguisse 51% do poder computacional de mineração de bitcoin algo muito dificil de acontecer.

**Funciona porque funciona:**

- Não existe nada que force os mineradores a se comportar corretamente
- Basicamente, seguindo o protocolo estabelecido, os mineradores são remunerados e mantêm a segurança do sistema.
- Seria praticamente impossível um minerador agir de forma maliciosa e lucrar:
  - É necessário um poder computacional muito grande
  - Destruiria a confiança no sistema

Os hackers tentam roubar a chave secreta associada a uma chave publica para conseguir os bitcoins, não atacam diretamente o sistema de bitcoins, pois se algum ataque realmente conseguir fraudar o bitcoin ele vai perder a confiaça e consequentemente se torna algo sem valor.