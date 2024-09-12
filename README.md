# DIO | Desenvolvendo e Registrando os Aprendizados com o Git

## Resumo

O repositório tem como objetivo anotar e descrever todos os códigos essenciais do Git, seja para uso futuro ou para ajudar os desenvolvedores que necessitam de uma solução rápida aos seus problemas ou relembrar códigos esquecidos.

Através do curso DIO Claro Bootcamp, estou desenvolvendo melhor as minhas habilidades com o Apliticativo de Versionamento de Código GIT, para ter uma bagagem completa das habilidades necessárias a se inserir no mercado de desenvolvimento de software e análise de dados.

## Listando Códigos para Configuração Completa do Git 

- Listar todas as configurações GIT

``git config --list``

- Configurar o email e nome que aparecerão nos commits

``git config --global user.name [NOME]``

``git config --global user.email [EMAIL]``


- Alterar a Branch padrão Master OR Main

``git config --global init.defaultBranch [BRANCH]``

### Criando sua Autenticação pelo Token

***Obs:*** o Token deve ser criado no seu Github através do [Github Tokens](https://github.com/settings/tokens) depois de criar seu token deve ser realizado um ``git clone`` **de um repositório privado** para assim utilizar a opção token

- Salvar Token permanentemente (após utiliza-lo)

``git config --global credential.helper store``

- Ver a localização do ".gitconfig" através do credential.helper

``git config --global --show-origin credential.helper``

### Criando sua chave SSH no Git

- Comando para listar se existem chaves SSH cadastradas

``ls -al ~/.ssh``

- Gerar uma nova chave SSH

`` ssh-keygen -t ed25519 -C "EMAIL"``

- Cria o agente da chave SSH

``eval "$(ssh-agent -s)"``

- Adicionando a chave SSH ao agente através do diretório ".ssh" criado anteriormente

``ssh-add /c/Users/gusta/.ssh/id_ed25519``

- Pegando os dados da sua chave SSH publica

``cd /c/Users/gusta/.ssh`` > ir até o diretório e abra o arquivo id_ed25519.pub com o CAT

``cat id_ed25519.pub`` > agora é só copiar a sua chave SSH e colocar no GitHub [clicando aqui](https://github.com/settings/keys)

## Explicando alguns documentos GIT
> .gitignore : o git ignore tem a capacidade de ignorar arquivos que você julgue desnecessário mostrar para aqueles que irão visualizar ou clonar o seu repositório

> .gitkeep : o Git keep é geralmente utilizado para quando existirem pastas vazias no seu repositório e deseja inseri-las no commit

## Códigos Essenciais para os Commits

- Inicializando um repositório Git na pasta atual

``git init``

- Ver a situação atual do seu repositório, ou seja, documentos a serem adicionados no commit

``git status``

- Adicionando documentos Untracked, ou seja, novos documentos ou documentos editados para mesa de Commits

``git add [DOCUMENTO]`` ( ou use "*" para adicionar todos)

- Restaurando documentos deletados

``git restore [DOCUMENTO]``

- Realizando o commit

``git commit -m "[DESCRIÇÃO DO COMMIT]"``

- Vendo  o registro completo de commits

``git log``

- Alterando a mensagem do commit

``git commit --amend -m "[NOVA MENSAGEM]"``


### Manipulando Commits anteriores

**Obs:** o Hash dos commits pode ser coletado utilizando o ``git log`` 

*  ``git reset --soft [HASH DO COMMIT ANTERIOR] ``

o Soft tem a função de retornar até o commit desejado, mas ainda mantém os arquivos atuais e ainda os deixa na mesa de commit, ou seja, os arquivos já passaram pelo ***git add***

* ``git reset --mixed [HASH DO COMMIT ANTERIOR] ``

o Mixed também retorna até o commit desejado mantendo os arquivos atuais, porém dessa vez deixa os arquivos como Untraked, ou seja, incapazes de serem adicionados a mesa de commits

* ``git reset --hard [HASH DO COMMIT ANTERIOR]`` 

 O Hard já não pe muito indicado, pois retorna até o commit deseja, mas deletando todos os registros anteriores

- Vendo o histórico de alteração nos commits

``git reflog``


## Enviando e Baixando Alterações com o Repositório Remoto








