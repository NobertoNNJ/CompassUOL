# Parte 2

# Accounts and States

Ethereum é uma maquina de estados, cada conta vai ter um estado.

- Externally Owned Accounts (EOA): Controladas por usuários detentores de uma chave secreta
- Contract Accounts (Smart Contracts): São ativadas por EOAs, mas controladas por sua programação interna.


**O que significava ter bitcoins?**

Significa ter varias transações que alguem fez direionadas a minha chave publica, e a soma de todas essas transações que eu não gastei é o meu saldo.


**No Ethereum é diferente:**

É mais similar a uma conta em um banco, o usuário possui algo parecido com conta em que no State aparece a sua quantidade de Ethereum, alem de outras coisas, a cada novo bloco com novas transações esse State é atualizado, apenas caso tenha alguma transação no bloco com uma relação com o do usuário.

Os States de  todas as Accounts ficam armazenados fora da blockchain, em uma estrutura de dados chamada State tree, na blockchain ficam as transações que modificam esses states, assim quem possui um no do blockchain Ethereum também possui um State tree que fica constantemente sendo atualizado.


**Por que States?**

- Simplicidade
- Eficiência

---

# Ethereum Virtual Machine (EVM):

Blocos diferentes

No caso do Ethereum as transações não são apenas a respeito de moedas destruidas e criadas, no Ethereum as transações contem um código de computador, o Ethereum é turing completo, o que significa que ele pode executar qualquer programa de computador, desde que tenha tempo e recursos suficientes.

Todos os nós da rede Ethereum executam todo o código em todos os blocos, assim eles sempre ficam com os States de todas as accounts atualizados.

Isso pode ser um problema, pois todos tem que rodar esso codigo independente de onde, isso pode gerar um problema, algo como tentar rodar um jogo do NES no SNES ou mega drive, isso não funciona, assim o código dos blocos do Ethereum são feitos para rodar no EVM, isso possibilita eles rodarem nas mesmas condições.

obs: Esse EVM seria similar a um Container no Docker. 

**Ethereum Virtual Machine:**

- Todos os nós da rede Ethereum possuem a EVM
- A EVM permite que linguagens de alto nível sejam usadas para criar algoritimos executáveis em qualque máquina com um nó Ehtereum.
- Solidity

---

# GAS:

**Problemas de todo nó precisar executar os codigos do bloco:**

- Custo de processamento
- Denial of service attacks(DoS)
- Algoritimos com problemas
- Loops infinitos

**GAS:**

- Qualquer transação tem um custo em GAS.
- Mais complexo -> Mais caro.
- Toda operação será executada até:
  - Finalizar normalmente.
  - Atigir o GAS Limit.
  - Usar todo o GAS enviado na transação
-  Para uma mesma operação, o custo em GAS é sempre o mesmo.
-  O preço do GAS varia em função da demanda.
- Impede o DoS(pois o ataque vai custar caro).
- Evita loops infinitos.
- Incentiva eficiência.
- Facilita a precificação.