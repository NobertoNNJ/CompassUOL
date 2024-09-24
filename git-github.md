# **Git e GitHub**

## **Git:**

- Sistema de controle de versão distribuído, gratuito e de código aberto;
- Software;
- Não necessariamente versionamento e programação, pode ser também para doc, xls;


Versão 1.0.0 -> versão 1.1.0 -> versão 1.1.1

Importante para reverter ações, evitando que grandes erros possam comprometer a aplicação sem possibilidade de volta. Realizamos o commit para enviar novas atualizações para versões.

## **GitHub:**

É um serviço de hospedagem cloud, para projetos que utilizam o git, garanti que caso eu perca arquivo local eu o possua no repositories com sync no github, também muito util para colaboração em projetos.


**Branch:** seria uma filia, um ramo do projeto principal main.

**Arquivos untracked:** são aqueles que foram adicionados ao diretório de trabalho, mas ainda não foram adicionados ao controle de versão do Git. Se esses arquivos forem alterados, o Git não fará uma cópia deles em um novo snapshot (commit).

**Arquivos tracked:** são aqueles que já foram adicionados ao controle de versão e possuem um snapshot (commit) associado. Quando um arquivo rastreado é alterado, o Git registra essa alteração no próximo commit, mantendo um histórico das versões desse arquivo.

**Arquivo pode estar em 3 estagio**

*working:* quando é feito a modificação de algum arquivo

*staging:* quando foi preparado para o commit git add .

*commit:* quando ja esta na versão final

É possível realizar o commit sem o git add ., porém evitar isso e so fazer caso possa garantir que não tem nada errado.

---
branch é uma filia/ramo

Main é a branch principal

Normalmente não se edita a main, deve-se criar uma branch onde será feita as suas modificações antes de manda-las para a main. Após garantir que a branch está completa é feito o merge para a main. Caso outros possuam branch da versão anterior da main quando fizerem o merge haverá algum conflito.

---

**Comandos:**

*git add .* transforma arquivo untracked em tracked

*git rm --cached* retorna arquivo para untracked

*git commit -m "mensagem"* é feito um snapshot e o arquivo se torna o arquivo versão final, e com isso torna-se possível voltar para versões anteriores.

*git diff* é possível ver o que foi modificado no commit

*git log* para ver todas as versões com data, comentário, versão, quem modificou.

*git log --oneline* vemos os dados de versão resumido.

*git rm "nome arquivo"* é realizada a remoção de algum arquivo

*git restore --staged "nome arquivo"* restaurar arquivo deletado da parte staged

*git restore "nome arquivo"* para restaurar realmente para a pasta 

modificar nome de arquivos

file -> file1

*git mv file file1*

*git commit -m "mensagem" --amend* alterar mensagem do ultimo commit

*git log -p* me traz o histórico de mudanças realizadas detalhadamente

*git reset* para retornar a algum commit anterior

ele basicamente muda o status atual main para algum anterior

**existem 3 tipos de git reset soft/mixed/hard**

*git reset --hard id* retorna ao commit escolhido apagando o atual

*git reset --mixed id* retorna ao commit escolhido e deixa o atual esperando aprovar add . para ficar pronto para commit

*git reset --soft id* retorna ao commit escolhido e deixa o atual pronto para ser commitado.

**git alias (atalho), serve para modificar os comandos do git**

*git config alias.log1 "log --oneline"* quando usar log1 será na verdade log --oneline

*git config --global alias.log1 "log --oneline"* quando usar log1 será na verdade log --oneline, com o global qualquer um que usar o git nesse repositório vai ter essa configuração.

*git branch nome* para criar uma branch

*git switch nome* para mudar para uma branch

*git switch -c nome* para criar e mudar para uma nova branch

*git merge -m "Merge da branch nome para a main" nome* para mergear uma branch para a main

*git branch -d nome* apagar a branch que não é mais util

*git init* inicializa um novo repositório Git no diretório atual.

*git add arquivo.txt*
Este comando adiciona o arquivo à área de stage, preparando-o para o próximo commit.

*git branch -m main* Este comando renomeia a branch atual para main.

*git remote add origin link*
Este comando adiciona um repositório remoto chamado origin, que é o endereço do repositório no GitHub.

*git push -u origin main* Este comando envia os commits da branch main para o repositório remoto. A opção -u (ou --set-upstream) associa a branch local à branch remota, facilitando o uso de git push e git pull posteriormente.

*git pull* Este comando atualiza o repositório local com as alterações feitas no repositório remoto.



---

Issues: problemas

criamos um "ticket" no GitHub para saber os problemas que surgiram e devemos resolver

assignees: designado a resolver o problema