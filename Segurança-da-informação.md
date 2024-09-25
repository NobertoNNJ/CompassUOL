# Fundamentos de segurança da informação

## O que é segurança da informação?

De acordo com o NIST (National Institute of Standards and Technology) a segurança da Informação é a proteção de informações e sistemas de informação contra o acesso, o uso, a divulgação, a interrupção, a modificação ou a destruição não autorizados, a fim de fornecer confidencialidade, integridade e disponibilidade.

## Pilares de segurança da informação

- confidencialidade
- integridade
- disponibilidade

A triade dos pilares de segurança da informação é o conjunto de tecnologias, processos e politicas que tem como finalidade manter as infromações, integras e disponiveis.

A segurança da informação tem o papel de proteger os dados agregando valor e contribuindo para o sucesso do negócio, e você tem papel fundamental nessa missão.

## Mas o que significa confidencialidade, integridade e disponibilidade?

### Confidencialidade

Para proteger a informação de acessos não autorizados, evitando situações de ataques por acesso indevido.

O objetivo é controlar o acesso por múltiplos fatores autenticação e criptografias.

**É assim o dia a dia em autenticação!**

- Especificar requisitos mínimos para uma senha segura.
- Autentiação multifator.
- Verificação de senha fraca.
- Identificador e gerenciador de sessões.

### Integridade

Este é o pilar que devemos atender para manter as coisas caracteristicas originais dos dados, conforme sua criação.

A implementação de controles para impedir a alteração não autorizada devem ser pensados e implementados.

**Original e confiavel é a regra aqui**

- Validação de dados, como hashes.
- Verifiação de duplicidade.
- Tratamento de dados de entrada, como caracteres especiais e comandos.

### Disponibilidade

Queremos que os dados estejam disponiveis para o que for necessário, quando precisarmos. Isso demanda a estabilidade e acesso permanente ao ambiente a aos sistemas.

Pense aqui nos controles existentes para acessar e usar informações

**A qualquer hora que precisar!**

- Recursos de redundândia, como backup de dados e balanceamento de carga.
- Infraestrutura em nuvem.
- Gestão de vulnerabilidades.

## A segurança da informação é responsabilidade de todos

Você é quem faz nosso ambiente mais seguro e para isso precisa pelo menos conhecer quais são nossas políticas e as principais diretrizes de segurança da informação.

Aprofundaremos nas principais diretrizes nos próximos módulos.

### **Política de Segurança da Informação (PSI)**

Em nossa PSI você encontra as boas práticas a seguir para proteger as informações, tudo que estiver contrário a isso considere um incidente de segurança e deve ser reportado ao time InfoSex (Veremos nos modulos a seguir).

Nós, assim como todas as demais empresas do grupo seguimos atualmente as orientações da PSI publicada pelo grupo UOL que diz:

"A politica de segurança da informação e segurança cibernética pretende (i) descrever as melhores práticas de segurança da informação e segurança cibernética quantoaá confiabilidade, integridade e disponibilidade de informações; (ii) estabelecer diretrizes para todos os usuatios, e (iii) minimizar os riscos de Segurança da informação"

### **Política de Classificação da Informação**

Para definir o controle mais adequando é necessário conhecer o tipo de informação, a sua criticidade e o público.

O melhor guia é a politica de clissificação da informação.

"Esta politica descreve o processo de classificação da informação, caracterizado pela definição do nivel de sensibilidade e os grupos de acesso à informação, visando assegurar que esta receba um nivel adequado de proteção, conforme seu valor, sensibilidade e criticidade para a organização."

---

# Classificação da Informação

“A classificação da informação tem como obtivo definir níveis de proteção que cada informação deve receber”. 

Toda e qualquer informação deve ser classificada, seja fisica ou lógica, de acordo com sua sensibilidade, criticidade e valor. A classificação deve tratar as informações durante o seu cilco de vida, ou seja, sua criação, edição, compartilhamento, armazenamento e descarte.

**Por que classificar?**

Para aplicar a devida proteção das informações e reduzir a probabilidade de ocorrer incidentes.

O vazamento de informações, por exemplo, pode ocasionar impactos financeiros, regulatório e reputacional, trazendo sanções e prejuizos a Compass, seus clientes, parceiros e profissionais.

## Níveis de classificação

### **Confidencial**

São informações altamente sigilosas e que não podem ser divulgadas para evitar danos à empresa, terceiros, funcionarios e clientes.

Seu uso requer medidas de controle e proteção rigorosos contra acessos cópias, reproduções ou divulgações não autorizados.

Devido à sensibilidade dessas informações, várias restrições de uso são aplicados e o destinatario consegue apenas consultar o documento.

**ATENÇÃO:** sob esta classificação, um possivel vazamento de dados certamente causaria grandes danos à empresa.


### **Restrita**

São informações exclusivas de alguns profissionais e/ou determiadas áreas.
Siginifica que nem todos têm acesso à elas, pois os dados desta categoria são disponibilizados apenas aos destinatários nos quais você delega confiança para tratar do assunto.

**Exemplos:**

- E-mail com feedback;
- Divulgação de metas e resultados institucionais;
- Informações sobre produtos, serviços e projetos;
- Dados ou informações referentes às politicas comerciais.

**ATENÇÃO:** Sob esta classificação, um possivel vazamento de dados pode causar um impacto significativo à empresa, seus profissionais, seus parceiros ou seus clientes.

### **Interna**

São informações que competem aos profissionais, estagiários, prestadores de serviços da empresa e precisam de cuidados para evitar a divulgação ao público externo.

**Exemplos:**

- Comunicados;
- Politicas e normas corporativas;
- Procedimentos operacionais e técnicos;
- Relação de endereços de e-mail internos;
- Informações disponibilizadas no intranet.

### **Pública**

São informações que podem ser divulgadas sem restrição para o público em geral, incluindo clientes, fornecesores, imprensa, concorrentes, entre outros.

As informações públicas são aqueles dados que podem ser divulgados sem oferecer risco algum à empresa., seus colaboradores e clientes.

---

# Engenharia Social

## Tácticas de abordagem

As abordagens variam de acordo com a exposição do atacante, abaixo os mais comuns. Ele se aproveita da boa vontade das pessoas para convencer a vitima através da labia a passar informações sensiveis, isso funciona principalmente por a pessoa ser o elo mais fraco e facil de burlar em um sistema de segurança.

**Baiting:** uma isca fisica ou digital como um pendrive ou download de um filme, podem trazer um malware para o computador ao inserir o pendrive ou baixar e executar um arquivo, o malware oculto ganha acesso ao computador.

**Pishing:** O mais famoso, porém, também mais eficiente! O atacante cria conteudo enganoso muto próximo de algo legitimo e confiavel, afim de obter credendiais ou instalar um malware. É comum se utilizar do e-mail, mas é muito comum também por SMS(Smishing) ou ligações de voz (Vishing).

**Dumpster Diving:** é uma das abordagens menos óbvias, porém, caso as empresas não tenham cuidados com o descarte de informações o atacante pode encontrar relatórios inteiros, discos removiveis entre outros tipos de midia com informações de todos os niveis de classificação.

## Dicas de Prevenção

- Sempre desconfie!
- Não baixe arquivos e anexos em emails suspeitos;
- Não responda ou interaja com mensagens de desconhecidos;
- valide links e remetentes dos emails;
- Descarte corretamente documentos e equipamentos;

# Boas práticas e diretrizes

**Compartilhamento de acesso:** Não compartilhe acesso as suas credenciais a ninguem, qualquer ação realizada com elas é de sua total responsabilidade

**Armazenamento:** Guarde suas informações nos repositorios oficiais para maior segurnaça

**Softwares e malwares:** softwares maliciosos e malwares são muito comuns em arquivos baixados pela internet, tomar muito cuidados, sempre verificar se os softwares que deseja baixar são homologados.

**Senhas Seguras:** As senhas que concedem acessos aos nossos dados devem ser seguras.

- Evitar nome, sobrenome, apelidos, datas de aniversario, celular;
- Senhas diferentes para sistemas diferentes;
- Trocas frequentes de senhas;
- Usar aplicativos "cofres de senhas";
- Utilização de MFA sempre que possivel;
- Reportar ao infosec casos suspeitos que requisitem seus dados;
- sempre que possivel utilizar letras maiusculas, minusculas, numeros e simbolos;

**Uso da internet:** 

Quando precisar trafegar informação sensível, procure pelo "cadeadinho"!

Conteúdo ilícito? Uma lista pra você se lembrar, mas não limitada a esta.

Ataques, ameaças, violência, pornografia, spoofing, sniffer, defacement, disseminação de vírus, worms, trojans, spywares, spam, roubo de informação, espionagem, sabotagem, destruição, divulgação e alteração de informações não autorizadas, pirataria, engenharia reversa e/ou depuração de código não autorizado.

**Multi-factor Autenticator(MFA):** Controle de segurança que demanda 2 ou mais elementos de autenticação para identificar usuário.

*Tipos mais utilizados:*

- O que sei: Exigido algo como login, senha ou resposta a uma pergunta secreta.
- O que tenho: Necessário algo fisico como um token, cartão inteligente ou app para obter uma informação geralmente randomica.
- Quem sou: Utiliza caracteristicas fisicas como a impressão digital,reconhecimento facial ou leitura de retina.

Na compass utilizamos MS Autenticator.

**Atualização de software:** Sempre manter softwares atualizados para minimizar riscos.

**Incidentes de segurança:** É um evento ou conjunto deles, que podem impactar a disponibilidade, integridade, confidencialidade de um ativo de informação, assim como qualquer violação do PSI.

- Ferramentas não autorizadas instaladas;
- Vírus e outros códigos maliciosos;
- Tentativas não autorizadas de acesso;
- Compartilhamento de credenciais;

Caso descobrir algum incidente de segurança relatar ao time infosec.


**Rede Wi-fi:** Evitar acesso a redes Wi-fi publicas, pois alguem pode estar bisbilhotanto os pacotes que trafegam nessa rede.

- Evite acessar redes publicas.
- Utilize VPN confiavel.
- Desative opção de conexão automatica a redes publicas.
- Desabilitar compartilhamento de arquivos.
- Nao instalar apps que prometem quebrar senhas para se conectar a redes protegidas.

*Em sua rede domestica:*

- Configurar senha forte e realizar trocas frequentes.
- Manter firmware atualizado.
- Mudar os padrões de fabrica como os dados de administrador.
- Desabilitar acesso para manutenção remota.
- Ficar atento a sites que pedem dados sensiveis.

# Segurança em IA Generativa

Forma mais segura para utilizar as tecnologias de inteligência artificial generativas e proteger os dados pessoais e empresariais da organização, bem como evitar o compartilhamento indevido de códigos e informações confidenciais

Orientações para evitar riscos como exposição involuntária de informação de clientes ou da Compass, comprometimento da imagem ou dos negócios da empresa, atividades ilegais, danos financeiros por vazamento de informações pessoais.

**O que é IA generativa:** Subcampo da IA que se concentra na criação de novos conteúdos, dados ou informações de texto, imagens, vídeos, músicas ou código, a partir de um conjunto de entradas existente.

Essas IAs aprendem com esses dados de entrada e são capazes de gerar saídas semelhantes, mas não iguais, com base no que aprenderam no treinamento.

**Ambiente e utilização de ferramentas de IA:** Existem ferramentas pagas e gratuitas para isso, mas deve-se saber como os dados inseridos nela serão utilizados para conseguir garantir a segurança dessas informações, ou podemos acabar permitindo que terceiros utilizem esses dados.

**Como proteger os dados** 

- Remover dados pessoais, senhas ou tokens de consulta que enviar, independente se são de ambiente ou produção.
- Quando possivel utilizar mascaramento de rede.
- Não enviar nas consultas dados reais de clientes ou da empresa.

**Controles Mínimos de segurança** 

- Homologação para validar os controles técnicos.
- Análise de riscos.
- Utilizar o jira para solicitação de acessos às ferramentas de IA.
- Documentar no Sharepoint ou Confluence os manuais ou processos para utilização das ferramentas de IA.
- Realizar os treinamentos obrigatórios e participar das ações de capacitação e consientização sobre o tema.