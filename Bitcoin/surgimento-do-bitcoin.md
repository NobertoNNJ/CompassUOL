# Parte 1

# Crise de 2008

o surgimento inicial do bitcoin foi durante a crise de 2008.

# Bitcoin

- É uma moeda virtual criptografada
- Unidade de troca
- Internamente ja possui um sistema de pagamento
- Funciona como reserva de valor
- Numero maximo que podem existir é 21 milhões

Criador é o pseudonimo "Satoshi Nakamoto"

bitcoin funciona devido uma conbinação entre

- Criptografia
- Blockchain
- Redes descentralizadas
- "Engenharia de incentivo"(caso siga as regras do bitcoin você ganha dinheiro, caso não é provavel que perca dinheiro.)

Em 2009 foi criado primeiro bloco de bitcoin(Genesis block)

---

# **Blockchain:** 

É uma cadeia de blocos, cada bloco possui uma serie de dados, que pode ser de qualquer tipo, cada bloco contém também informações a respeito do bloco anterior(algo como uma lista encadeada, ou como seu nome sugere uma corrente de blocos), caso um dado seja alterado em um bloco toda a blockchain apartir dele é alterada, isso ocorre devido a função hash.

**Funções Hash:**

- Tranforma um input em um output de tamanho fixo
- O input pode possuir qualquer tamanho
- O output sempre possui o mesmo tamanho

ex:

Fox -> Hash function -> DFJFF85DS5
The red cat -> Hash function -> GFSJUG86SR9

**Funções Hash Criptográficas:**

- Fácil de computar
- Livre de colisão: Extremamente improvável dois inputs com o mesmo output.
- Unidirecional: Extremamente improvável descobrir o input dado pelo seu hash
- "Puzzle Friendly"(uma pequena mudança no input gera uma grande mudança no output)

**Cada bloco possui**

- hash do bloco
- hash anterior
- dados

Pegando os dados e o hash do bloco anterior e geramos um novo hash que seria o hash do bloco, esse hash do bloco funciona como o "nome" do bloco, assim o porximo bloco terá o hash do bloco anterior e o seu proprio para apartir dele conseguirmos ir para o bloco anterior através do seu hash.

Supondo algum hacker modifique os dados de algum bloco da blockchain, mas caso ele faça isso os outros blocos perceberam, pois o hash é gerado através dos dados e do hash anteior, com a mudança nos dados do bloco vai existir uma incosistencia no hash, para isso o hacker vai precisar gerar um novo hash para esse bloco, mas isso vai quebrar a cadeia dos blocos , pois o caminho do proximo bloco iria apontar para um bloco que não existe mais, assim caso o hacker realmente deseje realizar essa invasão ele teria que ir modificando o hash de todos os blocos subsequente, para isso seria necessario um poder computacional muito grande.

# **Assinaturas Digitais**

Está ligada a garantia de transferencias seguras no bitcoin, algo como o sistema de segurança em um banco para amenizar fraudes, ela garante a segurança nas transações com bitcoin, todas as transferencias realizadas necessitam a "assinatura" de quem está realizando ela.

- Só você pode assinar
- Qualquer um pode verificar sua assinatura
- Assinatura atrelada ao documento

Isso funciona através de um sistema criptografico  denominado, criptografia de chave publica. Possuimos então uma chave publica e uma secreta, ao assinarmos um documento com a chave secreta é gerada uma assinatura especifica para aquele documento através de uma conta matematica, para verificar que foi realmente assinado por quem deveria é realizada um outro calculo em cima dessa assinatura do documento, mas dessa vez com a chave publica de quem assinou.