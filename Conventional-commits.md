# **Conventional Commits:**

Convenção para utilizar mensagens de commits. Ela define as regras a serem usadas para criar um histórico de commit explicito. Essa convenção se encaixa com o SemVer, descrevendo os recursos, correções e modificações que quebram a compatibilidade nas mensagens de commit.

**Deve ser feito da seguinte forma:**

Tipo[escopo opcional]: Descrição

[Corpo opcional]

[rodapé(s) Opcional(is)]

**exemplo:**

fix: corrigindo bug xxx que faz com que xxx ocorra.

**Tipos:**

*Fix:* um commit do tipo fix soluciona um problema no código (isso se correlaciona com PATCH do versionamento semântico).

*Feat:* um commit do tipo feat inclui um novo recurso no código (isso se correlaciona com MINOR do versionamento semântico).

*BREAKING CHANGE:* um commit que contém no rodapé o texto BREAKING CHANGE:, ou contém o símbolo ! depois do tipo/escopo, introduz uma modificação que quebra a compatibilidade da API (isso se correlaciona com MAJOR do versionamento semântico). Uma BREAKING CHANGE pode fazer parte de commits de qualquer tipo.

---

Outros tipos adicionais são permitidos além de fix: e feat:, por exemplo recomenda-se build:, chore:, ci:, docs:, style:, refactor:, perf:, test:, entre outros.

Outros rodapés diferentes de BREAKING CHANGE: <descrição> podem ser providos e seguem uma convenção similar ao git trailer format.

Esses tipos adicionais não são exigidos pela especificação do Conventional Commits e não têm efeito implícito no versionamento semântico (a menos que incluam uma BREAKING CHANGE). 

Um escopo pode ser fornecido ao tipo do commit, para fornecer informações contextuais adicionais e está contido entre parênteses, por exemplo feat(parser): adiciona capacidade de interpretar arrays.

**Exemplos:**

Mensagem de commit com descrição e modificação que quebra a compatibilidade no rodapé

- feat: permitir que o objeto de configuração fornecido estenda outras configurações

- BREAKING CHANGE: a chave `extends`, no arquivo de configuração, agora é utilizada para estender outro arquivo de configuração.


Mensagem de commit com ! e BREAKING CHANGE no rodapé

- chore!: remove suporte para Node 6

- BREAKING CHANGE: refatorar para usar recursos do JavaScript não disponíveis no Node 6

Mensagem de commit sem corpo

- docs: ortografia correta de CHANGELOG

Mensagem de commit com escopo

- fear(lang): adiciona tradução para português brasileiro

Mensagem de commit de uma correção utilizando número de ticket (opcional)

- fix: corrige pequenos erros de digitação no código

- veja o ticket para detalhes sobre os erros de digitação corrigidos

- Revisado por: Noberto Nunes
- Refs #133

---

A mensagem de commit DEVE ser prefixado com um tipo, que consiste em um substantivo, feat, fix, etc., seguido por um escopo OPCIONAL, símbolo OPCIONAL !, e OBRIGATÓRIO terminar com dois-pontos e um espaço.

O tipo feat DEVE ser usado quando um commit adiciona um novo recurso ao seu aplicativo ou biblioteca.

O tipo fix DEVE ser usado quando um commit representa a correção de um problema em seu aplicativo ou biblioteca.

Um escopo PODE ser fornecido após um tipo. Um escopo DEVE consistir em um substantivo que descreve uma seção da base de código entre parênteses, por exemplo, fix(parser): .

Uma descrição DEVE existir depois do espaço após o prefixo tipo/escopo. A descrição é um breve resumo das alterações de código, por exemplo, fix: problema na interpretação do array quando uma string tem vários espaços.

Um corpo de mensagem de commit mais longo PODE ser fornecido após a descrição curta, fornecendo informações contextuais adicionais sobre as alterações no código. O corpo DEVE começar depois de uma linha em branco após a descrição.

Um corpo de mensagem de commit é livre e PODE consistir em infinitos parágrafos separados por uma nova linha.

PODE(M) ser fornecidos um ou mais rodapés, uma linha em branco após o corpo. Cada rodapé DEVE consistir em um token de palavra, seguido por um separador :<espaço> ou <espaço>#, seguido por um valor de uma string (isso é inspirado pelo git trailer convention).

Um token de rodapé DEVE usar - no lugar de espaços em branco, por exemplo, Acked-by (isso ajuda a diferenciar a seção de rodapé de um corpo de vários parágrafos). Uma exceção é feita para BREAKING CHANGE, que PODE também ser usado como um token.

O valor de um rodapé PODE conter espaços e novas linhas, e a análise (parsing) DEVE terminar quando o próximo token/separador de rodapé válido for encontrado.

BREAKING CHANGES DEVEM ser indicadas após o tipo/escopo de uma mensagem de commit, ou como uma entrada no rodapé.

Se incluída como um rodapé, uma alteração de quebra DEVE consistir no texto em maiúsculas QUEBRAR ALTERAÇÃO, seguido por dois pontos, espaço e descrição, por exemplo, BREAKING CHANGE: as variáveis de ambiente agora têm precedência sobre os arquivos de configuração.

Se incluído no prefixo de tipo/escopo, as BREAKING CHANGES DEVEM ser indicadas por um ! imediatamente antes de :. Se o símbolo ! for usado, BREAKING CHANGE: PODE ser omitido da seção de rodapé, e a descrição da mensagem de commit DEVE ser usada para descrever a BREAKING CHANGE.

Tipos diferentes de feat e fix PODEM ser usados em suas mensagens de commit, por exemplo, docs: documentos de referência atualizados
As unidades de informação que compõem o Conventional Commits NÃO DEVEM ser tratadas com distinção entre maiúsculas e minúsculas pelos implementadores, com exceção de BREAKING CHANGE que DEVE ser maiúscula.

BREAKING-CHANGE DEVE ser sinônimo de BREAKING CHANGE, quando usado como um token em um rodapé.


---

**Porque utilizar conventional commits**

- Criação automatizada de CHANGELOGs 
- Determinar automaticamente alterações no versionamento semântico(com base nos tipos de commits)
- Comunicar a natureza das mudanças para colegas de equipe, o público e outras partes interessadas
- Disparar processos de build e deploy
- Facilitar a contribuição de outras pessoas em seus projetos, permitindo que eles explorem um histórico de commits melhor estruturado


# **Versionamento semantico**


**Versões:**

- *versão Maior(MAJOR):* quando fizer mudanças incompatíveis na API;
- *versão Menor(MINOR):* quando adicionar funcionalidades mantendo compatibilidade; 
- *versão de Correção(PATCH):* quando corrigir falhas mantendo compatibilidade. 

Rótulos adicionais para pré-lançamento(pre-release) e metadados de construção(build) estão disponíveis como extensão ao formato MAJOR.MINOR.PATCH.

---

Software usando Versionamento Semântico DEVE declarar uma API pública. Esta API poderá ser declarada no próprio código ou existir estritamente na documentação, desde que seja precisa e compreensiva.

Um número de versão normal DEVE ter o formato de X.Y.Z, onde X, Y, e Z são inteiros não negativos, e NÃO DEVE conter zeros à esquerda. X é a versão Maior, Y é a versão Menor, e Z é a versão de Correção. Cada elemento DEVE aumentar numericamente. Por exemplo: 1.9.0 -> 1.10.0 -> 1.11.0.

Uma vez que um pacote versionado foi lançado(released), o conteúdo desta versão NÃO DEVE ser modificado. Qualquer modificação DEVE ser lançado como uma nova versão.

No início do desenvolvimento, a versão Maior DEVE ser zero (0.y.z). Qualquer coisa PODE mudar a qualquer momento. A API pública NÃO DEVE ser considerada estável.

Versão 1.0.0 define a API como pública. A maneira como o número de versão é incrementado após este lançamento é dependente da API pública e como ela muda.

Versão de Correção Z (x.y.Z | x > 0) DEVE ser incrementado apenas se mantiver compatibilidade e introduzir correção de bugs. Uma correção de bug é definida como uma mudança interna que corrige um comportamento incorreto.

Versão Menor Y (x.Y.z | x > 0) DEVE ser incrementada se uma funcionalidade nova e compatível for introduzida na API pública. DEVE ser incrementada se qualquer funcionalidade da API pública for definida como descontinuada. PODE ser incrementada se uma nova funcionalidade ou melhoria substancial for introduzida dentro do código privado. PODE incluir mudanças a nível de correção. A versão de Correção DEVE ser redefinida para 0(zero) quando a versão Menor for incrementada.

Versão Maior X (X.y.z | X > 0) DEVE ser incrementada se forem introduzidas mudanças incompatíveis na API pública. PODE incluir alterações a nível de versão Menor e de versão de Correção. Versão de Correção e Versão Menor DEVEM ser redefinidas para 0(zero) quando a versão Maior for incrementada.

Uma versão de Pré-Lançamento (pre-release) PODE ser identificada adicionando um hífen (dash) e uma série de identificadores separados por ponto (dot) imediatamente após a versão de Correção. Identificador DEVE incluir apenas caracteres alfanuméricos e hífen [0-9A-Za-z-]. Identificador NÃO DEVE ser vazio. Indicador numérico NÃO DEVE incluir zeros à esquerda. Versão de Pré-Lançamento tem precedência inferior à versão normal a que está associada. Uma versão de Pré-Lançamento (pre-release) indica que a versão é instável e pode não satisfazer os requisitos de compatibilidade pretendidos, como indicado por sua versão normal associada. Exemplos: 1.0.0-alpha, 1.0.0-alpha.1, 1.0.0-0.3.7, 1.0.0-x.7.z.92.

Metadados de construção(Build) PODE ser identificada por adicionar um sinal de adição (+) e uma série de identificadores separados por ponto imediatamente após a Correção ou Pré-Lançamento. Identificador DEVE ser composto apenas por caracteres alfanuméricos e hífen [0-9A-Za-z-]. Identificador NÃO DEVE ser vazio. Metadados de construção PODEM ser ignorados quando se determina a versão de precedência. Assim, duas versões que diferem apenas nos metadados de construção, têm a mesma precedência. Exemplos: 1.0.0-alpha+001, 1.0.0+20130313144700, 1.0.0-beta+exp.sha.5114f85.

A precedência refere como as versões são comparadas uma com a outra quando solicitado.

A precedência DEVE ser calculada separando identificadores de versão em Maior, Menor, Correção e Pré-lançamento, nesta ordem. (Metadados de construção não faz parte da precedência).

A precedência é determinada pela primeira diferença quando se compara cada identificador da esquerda para direita, como se segue: Versões Maior, Menor e Correção são sempre comparadas numericamente.

Exemplo: 1.0.0 < 2.0.0 < 2.1.0 < 2.1.1.

Quando Maior, Menor e Correção são iguais, a versão de Pré-Lançamento tem precedência menor que a versão normal.

Exemplo: 1.0.0-alpha < 1.0.0.

A precedência entre duas versões de Pré-lançamento com mesma versão Maior, Menor e Correção DEVE ser determinada comparando cada identificador separado por ponto da esquerda para direita até que seja encontrada diferença da seguinte forma:

Identificadores consistindo apenas dígitos são comparados numericamente.

Identificadores com letras ou hífen são comparados lexicalmente na ordem de classificação ASCII.

Identificadores numéricos sempre têm menor precedência do que os não numéricos.

Um conjunto maior de campos de pré-lançamento tem uma precedência maior do que um conjunto menor, se todos os identificadores anteriores são iguais.

Exemplo: 1.0.0-alpha < 1.0.0-alpha.1 < 1.0.0-alpha.beta < 1.0.0-beta < 1.0.0-beta.2 < 1.0.0-beta.11 < 1.0.0-rc.1 < 1.0.0.

---

**Por que usar Versionamento Semântico?**

Sem a aderência a algum tipo de especificação formal, os números de versão são essencialmente inúteis para gerenciamento de dependências. Dando um nome e definições claras às ideias acima, fica fácil comunicar suas intenções aos usuários de seu software. Uma vez que estas intenções estão claras, especificações de dependências flexíveis (mas não tão flexíveis) finalmente podem ser feitas.
