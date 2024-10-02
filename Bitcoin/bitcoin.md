# Parte 2

# Bitcoin

## A Rede Bitcoin

- Distribuida
- Sem hierarquia
- Protocolo de consenso

No bitcoin, todos os computadores precisam entrar em um acordo, mesmo que alguns computadores sejam maliciosos a segurança da rede deve ser mantida.

- Qualquer computador conectado à rede blockchain é um nó desta rede.
- Full nodes:
  - Validam todas as transações emitidas pela rede
  - Mantêm a consistência da blockchain
- Lite nodes:
  - Não armazenam toda a blockchain
  - Necessitam de infromação de outros nós

Mineradores: funcionam meio que como os full nodes do bitcoin.

Carteiras: podem ser lite nodes ou full nodes

**Transação Bitcoin:**

- Assinatura noberto
- moedas criadas
  - chave do destinatario
- moedas cosumidas

Envia a transação para um node da rede bitcoin, ele explica para um computador da rede a transferencia realizada, esse node que recebem a transação verifica se está tudo correto na transação, caso esteja ele espalha a noticia para todos os nodes da rede bitcoin, isso acontece através do protocolo de fofoca.

**Mineradores:**

- Validam as transações recebidas e criam novos blocos.
- Competem entre si pelo direito de adcionar o próximo bloco blockchain.
- Verificam blocos obtidos por outros mineradores e adcionam a blockchain quando válidos.
- Sempre extemdem o ramo mais longo da blockchian

