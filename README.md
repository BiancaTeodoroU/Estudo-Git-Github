# Estudo sobre Git e Github


##  Antigamente as pessoas faziam cópias e mais cópias de um mesmo projeto, e outras acabavam sem querer apagando algum arquivo importante e não conseguindo recuperá-los, E a partir dai surgiu o controle de versão.

### o que é o controle de versão?

É um sistema com a finalidade de gerenciar diferentes versões de um documento, ele vai ser o sistema responsável por pegar as diferentes modificações ocorridas no seu projeto, e criar versões desses documentos facilitando com que você consiga avançar versões ou voltar versões sem ter tantas dificuldades.
       
    Nesse caso será abordado somente sobre o Git, mas existem outros.

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

# Comandos terminal

#### Como configurar o Git 

#### Comando para definir seu nome de usúario, que vai passar para todos os seus repositórios ( config de usúario (Global))

git config --global user.name "Seu nome"

#### Comando para configurar o e-mail

git config --global user.email "Seu E-mail"

#### Como configurar qual é o editor principal do Git
git config --global core.editor (passar aqui o comando do seu editor, por exemplo se usa sublime será subl ou vscode)

#### Se voce não definir ele vai usar o vim por padrão.
#### Pra saber qual é o valor daquele dado que você digitou
##### Exemplo: Qual seu user name
git config user.name

##### Qual seu e-mail ?
git config user.email

#### Caso queira saber tudo é só utilizar o comando, e vai mostrar todas as informações do seu Git
git config --list


### Comando para criar uma pasta 
mkdir (nome da pasta)

### Para entrar dentro da pasta 
cd (nome da pasta)

### Responsável por inicializar o repositório e ficar enxergando todas as mudanças nesse projeto.
git init

#### Ele vai mostrar todos os diretórios
ls -la

#### Para voltar no diretório anterior 
cd ..

#### editar o nome do arquivo 
vim(ou outro que você estiver usando) (nome do arquivo)
ficaria : vim Readme.md

Assim que executado o comando Apertar a tecla i
Depois de escrever tudo que você preferir apertar a tecla ESQ, e apertar :  ( que indica que você vai iniciar algum comando ), apertar o w ( que significa que você quer escrever, salvar), e apertar o q ( que significa que você quer sair).

#### Serve para reportar como está o repositório 
git status

#### Adicionar o arquivo ao Git
git add ( Nome do arquivo )
ou git add . ( Para adicionar todos os arquivos )

#### O que é um commit? 
O commit é o momento em que você irá avisar o git, olha pegue todos esses arquivos do meu repositório e crie uma versão dele.

#### Uma boa prática colocar sempre nos seus comentários, o que voce de fato fez de modificação, se você fez uma nova funcionalidade etc..

##### Para commitar : 
git commit -m "Escrever aqui seu commit dentro das aspas dupla"

#### Mostra os commits ja feitos, e quais arquivos mudaram
git log 

#### Mostra algumas informações, por exemplo mudou de branch para outra, que tags foram geradas.
git log --decorate 

#### Pode se filtrar pelo autor (Nome) 
##### Exemplo usando meu Nome, mas deve se colocar o seu que foi criado
git log --author="Bianca" 

#### Ele mostra em ordem alfabetica, quais foram os autores, quantos commits eles deram, e quais eles foram.
git shortlog

#### Se quiser ver só a quantidade de commits e a pessoa
git shortlog --sn 

#### Mostra em forma gráfica o que está acontecendo com as brachs e as versões
git log --graph

#### Dentro do git log existe uma hash, pela hash da pra se identificar o que aconteceu nesse commit, o que foi modificado etc...
Para descobrir quais modificações foram feitas, copie o hash ( o hash é o que está grifado de vermelho ).
E use o comando git show ( e a numeração da hash ) então ficaria:

    git show 345019c00ad7df85074d8aaaa7e34d9dbee48a74 

![enter image description here](https://github.com/BiancaTeodoroU/Estudo-Git-Github/blob/main/image/rash.png?raw=true)






git clone SSH

git pull

code .

npm i

git checkout -b (-b é para criar uma brach nova) nome/branch

git checkout ( para mudar de branch )

git add

git add . (adicionar todos)

git commit -m "chore: meu primeiro commit e adicionado configurações"

git push.

Caso o git commit -m e o git push estiver dando erro, tentar usar ( git commit -m "Mensagem q preferir" --no-verify)(git push --no-verify ou git push origin master --no-verify).
