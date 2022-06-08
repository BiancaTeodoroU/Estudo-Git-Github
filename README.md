# Estudo sobre Git e Github

![enter image description here](https://github.com/BiancaTeodoroU/Estudo-Git-Github/blob/main/image/GIT%20VS%20GITHUB.png?raw=true)

##  Antigamente as pessoas faziam cópias e mais cópias de um mesmo projeto, e outras acabavam sem querer apagando algum arquivo importante e não conseguindo recuperá-los, E a partir dai surgiu o controle de versão.

### o que é o controle de versão?

É um sistema com a finalidade de gerenciar diferentes versões de um documento, ele vai ser o sistema responsável por pegar as diferentes modificações ocorridas no seu projeto, e criar versões desses documentos facilitando com que você consiga avançar versões ou voltar versões sem ter tantas dificuldades.
### Nesse caso será abordado somente sobre o Git, mas existem outros.

## Mas afinal quem inventou o Git? qual é a história dele? 

### História do Git
Existia uma empresa chamada BitKeeper que guardava todo o código do kernel do linux, então todo o linux era versionado nesse sistema, só que houve uma quebra entre a linux e a BitKeeper, fazendo com que a linux não fosse mais isenta de pagar pelo uso da ferramenta, com isso o linux teria que começar a pagar para usar.
      O criador do linux, Linus Torvalds decidiu então criar sua própria ferramenta, e criou uma ainda melhor que a da BitKeeper, E fez um sistema de versionamento que tem melhorias comparado as deficiências que ele via na ferramenta da BitKeeper, e assim surgiu o Git.

### Quais as melhorias o Git tem comparada a ferramente da BitKeeper?

#### Melhorias: 
- Velocidade.
- Design Simples.
- Suporte robusto a desenvolvimento não linear (Milhares de branches paralelos).
- Totalmente distribuído.
- Capaz de lidar eficientemente com grandes projetos como o kernel do linux.

## O que é Git?

É o sistema de controle de versão.

## O que é GitHub ?

É um serviço de web compartilhado para projetos que utilizam o Git para versionamento.
Atualmente se tornou como se fosse uma rede social onde você disponibiliza seu código para todo mundo, mas dentro a possibilidade de deixar de maneira privada também.

### ATENÇÃO O GIT NÃO É IGUAL AO GITHUB, eles são diferentes.

- O Git são seus arquivos no seu local, é o controle de versão.
- O GitHub são seus arquivos na web, é só o seu repositório remoto.

# Comandos Git - Terminal

## Como configurar o Git 
### Comando para definir seu nome de usúario, que vai passar para todos os seus repositórios ( config de usúario (Global))

    git config --global user.name "Seu nome"

### Comando para configurar o e-mail

    git config --global user.email "Seu E-mail"

### Como configurar qual é o editor principal do Git
    git config --global core.editor

(passar aqui o comando do seu editor, por exemplo se usa sublime será subl ou vscode)

#### Se você não definir ele vai usar o vim por padrão.
## Para saber qual é o valor daquele dado que você digitou
### Exemplo: Qual seu user name

    git config user.name

### Qual seu e-mail ?

    git config user.email

### Caso queira saber tudo é só utilizar o comando, e vai mostrar todas as informações do seu Git
    git config --list


### Comando para criar uma pasta 
    mkdir (nome da pasta)

### Para entrar dentro da pasta 
    cd (nome da pasta)

### Responsável por inicializar o repositório e ficar enxergando todas as mudanças nesse projeto.
    git init

### Ele vai mostrar todos os diretórios
    ls -la

### Para voltar no diretório anterior 
    cd ..

### Editar o nome do arquivo 
vim(ou outro que você estiver usando) (nome do arquivo)
ficaria : 
    vim Readme.md

Assim que executado o comando Apertar a tecla i
Depois de escrever tudo que você preferir apertar a tecla ESQ, e apertar :  ( que indica que você vai iniciar algum comando ), apertar o w ( que significa que você quer escrever, salvar), e apertar o q ( que significa que você quer sair).

### Serve para reportar como está o repositório 
    git status

### Adicionar o arquivo ao Git
    git add ( Nome do arquivo )
ou 
    git add . ( Para adicionar todos os arquivos )

### O que é um commit? 
O commit é o momento em que você irá avisar o git, olha pegue todos esses arquivos do meu repositório e crie uma versão dele.

### Uma boa prática colocar sempre nos seus comentários, o que você de fato fez de modificação, se você fez uma nova funcionalidade etc..

### Para commitar : 
    git commit -m "Escrever aqui seu commit dentro das aspas dupla"

### Mostra os commits ja feitos, e quais arquivos mudaram
    git log 

### Mostra algumas informações, por exemplo mudou de branch para outra, que tags foram geradas.
    git log --decorate 

## Pode se filtrar pelo autor (Nome) 
### Exemplo usando meu Nome, mas deve se colocar o seu que foi criado
    git log --author="Bianca" 

### Ele mostra em ordem alfabetica, quais foram os autores, quantos commits eles deram, e quais eles foram.
    git shortlog

### Se quiser ver só a quantidade de commits e a pessoa
    git shortlog --sn 

### Mostra em forma gráfica o que está acontecendo com as brachs e as versões
    git log --graph

### Dentro do git log existe uma hash, pela hash da pra se identificar o que aconteceu nesse commit, o que foi modificado etc...
Para descobrir quais modificações foram feitas, copie o hash ( o hash é o que está grifado de vermelho ).
E use o comando git show ( e a numeração da hash ) então ficaria:

    git show 345019c00ad7df85074d8aaaa7e34d9dbee48a74 

![enter image description here](https://github.com/BiancaTeodoroU/Estudo-Git-Github/blob/main/image/rash.png?raw=true)

### Mostra as mudanças antes de commitar 
    git diff

### Mostrar somente o nome do arquivo que foi modificado
    git diff --name-only

### Para resetar o arquivo, fazendo isso ele vai retornar o arquivo antes da edição
    git checkout

### Quer dizer que você quer pegar o arquivo e tirar da fila do state
git reset HEAD (Nome do arquivo)
exemplo:

    git reset HEAD readme.md

### Para adicionar todos os meus arquivos modificados + a minha mensagem 
    git commit -am "Digite aqui dentro das aspas dupla"

### Esta opção ignora os ganchos dos commits anteriores e os ganchos das mensagens de commit, tambem possivel utilizar o --no-verify no git push.

    git commit -m "mensagem" --no-verify
### Como fazer para voltar, depois de ja ter dado o commit? existem 3 tipos de git reset ( Tomar cuidado porque ele altera o histórico do commit )

- --soft: ele vai pegar as minhas modificações e vai só voltar o commit, deletar aquele commit que ja foi feito, mas o arquivo ja vai estar em state com a modificação pronta pra ser commitado novamente.

- --mixed: ele vai deletar aquele commit, só que ele vai voltar os arquivos antes do state.

- --hard: ele vai deletar tudo que foi feito do commit, quando der o git log após utiliza-lo aquele histórico daquele commit que você deletou vai ter sumido, é recomendado usa-lo somente se você ainda não tiver subido aquele commit para um repositório remoto.

### A gente sempre escolhe não o commit que deseja retornar, a gente escolhe um commit antes. Para ficar mais fácil de entender aqui vai um exemplo:

#### O que está grifado de vermelho é o commit que eu quero deletar, e em azul é o commit que quero que não seja deletado, se eu quero apagar o 1 nesse caso ( em vermelho ) então eu tenho que usar o comando git usando uma hash antes do commit que eu quero deletar, ( o que está grifado de azul, o 2 commit) Ou seja sempre que eu for deletar determinado commit eu sempre uso a hash antes dele, para conseguir apagar.

![enter image description here](https://github.com/BiancaTeodoroU/Estudo-Git-Github/blob/main/image/git%20reset.png?raw=true)

então ficaria: 

    git reset --soft e482c78f1167a673cc1e04e70498fe89befab5a9 

( Nesse caso estou usando o --soft mas poderia ser tambem o --mixed ou o --hard, isso vai de sua escolha )

### Criando repositório remoto 
    git remote add origin ( E a url do seu repositório do git )

### Envia todos os arquivos, e modificações para o repositório que você determinar 
    git push -u origin master 

## O que é SSH? 
### SSH é um protocolo que serve pra autenticar um usúario remoto a um servidor, ou seja ele é baseado em chaves onde existe uma chave pública e uma chave privada, onde a chave privada consegue abrir a chave pública. Ou seja a gente envia a chave publica pro servidor (Github) e com a nossa chave privada dentro da nossa maquina a gente é capaz de abrir a chave publica do servidor e é capaz de subir o nosso código.

#### Para criar 

- abrir o terminal 
#### copiar o comando :

    $ ssh-keygen -t rsa -b 4096 -C "Aqui dentro das aspas dupla, você irá colocar exatamente o mesmo e-mail que você criou seu github"
#### Assim que der ENTER irá aparecer essa mensagem 
    Generating public/private rsa key pair
#### Aqui irá mostrar o local onde você irá salvar a chave e se você deseja alterar o nome ( em geral se deixa assim mesmo o nome padrão id_rsa)

    Enter a file in which to save the key (/users/you/.ssh/id_rsa): [Press enter]

- Neste etapa ele irá pedir para você apertar enter novamente (2x) e assim a sua chave será criada.

### Como ver minhas chaves? 
#### Esse é o diretório onde ficam as chaves ssh
    cd ~/.ssh/

#### Se digitar:
    ls

#### Será pega a chave pub, para pegar essa chave é preciso usar o comando 
    cat id_rsa.pub ou more id_rsa.pub

### Agora você irá entrar dentro do seu Github 
#### Clique na opção Settings

![enter image description here](https://github.com/BiancaTeodoroU/Estudo-Git-Github/blob/main/image/Onde%20colocar%20a%20chave%20SSH%20.png?raw=true)

#### Clique em SSH and GPG keys

![enter image description here](https://github.com/BiancaTeodoroU/Estudo-Git-Github/blob/main/image/local%20git%20chave%20ssh.png?raw=true)

#### Clique em New SSH key

![enter image description here](https://github.com/BiancaTeodoroU/Estudo-Git-Github/blob/main/image/onde%20criar%20a%20nova%20chave%20ssh%20no%20github.png?raw=true)

#### No campo escrito Key será onde você vai colar a chave SSH e em title geralmente se coloca o nome da maquina para ficar mais fácil depois de se identificar de onde é essa chave.Feito isso é só clicar em Add SSH key, e ai você irá poder utilizar o git push, sem ter problemas de permissão e para subir seu código.


![enter image description here](https://github.com/BiancaTeodoroU/Estudo-Git-Github/blob/main/image/add%20ssh%20key.png?raw=true)

#### Feito isso é só clicar em Add SSH key, e ai você irá poder utilizar o git push, sem ter problemas de permissão e para subir seu código.

### Para clonar algum repositório 

    git clone git@github.com:biancateodoro/github-course.git github-course-clone

#### Após clonar entrar dentro do repositório criado 

    cd github-course-clone/

#### Se der o comando, será possivel ver todas as informações clonadas do outro repositório

    more nome do arquivo

### O que é um branch? 
É um ponteiro móvel que leva a um commit 
### Porque usar? Quais são as vantagens?
- Poder modificar sem alterar o local principal (Master)
- Facilmente "desligável"
- Múltiplas pessoas trabalhando
- Evita conflitos

## Para criar um brach 
### Após o -b você pode escolher o nome que quiser para sua branch, nesse caso estou usando o nome testing mas poderia ser qualquer outro 

    git checkout -b testing

### Para listar as branches

    git branch

### Pra ir para a branch que você quer

    git checkout testing

### Se quiser voltar para a master

    git checkout master

### Para deletar uma branch

    git branch -D testing

## Unindo branches, existem 2 metodos importantes:
### Merge
Cria um commit novo para juntar as diferenças

![enter image description here](https://github.com/BiancaTeodoroU/Estudo-Git-Github/blob/main/image/Merge.png?raw=true)

#### PRO
- Operação não destrutiva 
#### Contra
- Commit extra
- Histórico poluido
--------------------------------------------------------------
### Rebase
Ele joga as mudanças para o inicio da fila

![enter image description here](https://github.com/BiancaTeodoroU/Estudo-Git-Github/blob/main/image/Rebase.png?raw=true)

#### PRO
- Evita commits extras
- Histórico linear 
#### Contra
- Perde ordem cronológica 
--------------------------------------------------------------
### O que é o fork?
Ele pega um projeto que não é seu e faz uma cópia dele.

### Para que serve o alias?
São atalhos dos comandos 
#### Para criar atalhos você deverá escolher se quer que esse atalho seja global, vai escrever o alias. e a letra que você quer que seja desse comando nessa caso alias.s e depois digitar de qual comando será esse atalho ( que nesse caso status ). 

    git config --global alias.s status

### Pra que serve o revert? 
Ele vai reverter as mudanças feitas, e vai colocar o código anterior, criando 2 commits, um que eu usei o comando revert e ele voltou o código para antes daquela mudança que fiz, e o outro commit vai estar com a alteração mas ai eu posso usar um git reset --hard e apaga-lo.

    git revert numeração da hash

### Como apagar as branches nos repositórios remotos
#### Onde está o testing você deve colocar o nome da branch que deseja apagar ou o nome da tag

    git push origin:testing

### O npm é uma ferramenta de linha de comando que ajuda a interagir com plataformas online, como navegadores e servidores. Essa utilidade auxilia na instalação e desinstalação de pacotes, gerenciamento da versões e gerenciamento de dependências necessárias para executar um projeto.

    npm i

### O comando git pull é usado para buscar e baixar conteúdo de repositórios remotos e fazer a atualização imediata ao repositório local para que os conteúdos sejam iguais. 

    git pull

### Se for feita alguma mudança e ela não estiver completa, e você precisou ir para outro branch, você ainda não commitou  porque elas ainda estão incompletas, então para salvar esse estado que é antes de um commit

#### Clicar em fazer stash

![enter image description here](https://github.com/BiancaTeodoroU/Estudo-Git-Github/blob/main/image/onde%20fica%20a%20op%C3%A7%C3%A3o%20para%20fazer%20um%20stash.png?raw=true)

#### Onde ficou o stash que fiz 

![enter image description here](https://github.com/BiancaTeodoroU/Estudo-Git-Github/blob/main/image/onde%20ficou%20o%20stash%20que%20fiz.png?raw=true)

#### Como apagar um stash 

![enter image description here](https://github.com/BiancaTeodoroU/Estudo-Git-Github/blob/main/image/n%C3%A3o%20quero%20mais%20o%20stash.png?raw=true)

#### OBS: Quando for excluir verificar qual mensagem você colocou no stash que deseja excluir e clicar nele assim que selecionar a opção.

### Como Reverter um commit 
#### OBS: pode ser usada qualquer hash, desde a última até a do meio, qualquer uma, então irá ficar git revert e o número da hash

    git revert 883cf673ebf864564efd55fb132f16f9aac0adc2

#### Após executado esse comando aperte : w q Enter 
#### Assim você terá revertido esse commit, após isso dar o git push origin master ( ou git push )

### Como fazer para editar o último commit 

    git commit --amend

#### Depende do seu tipo de editor se for o vim é só pressionar i para abrir o modo de edição ESQ : w q para sair.


--------------------------------------------------------------

Dados do curso do : 
Willian Justen Cursos
