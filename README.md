# Estudo sobre Git e Github


##  Antigamente as pessoas faziam cópias e mais cópias de um mesmo projeto, e outras acabavam sem querer apagando algum arquivo importante e não conseguindo recuperá-los, E a partir dai surgiu o controle de versão.

### o que é o controle de versão?

É um sistema com a finalidade de gerenciar diferentes versões de um documento, ele vai ser o sistema responsável por pegar as diferentes modificações ocorridas no seu projeto, e criar versões desses documentos facilitando com que você consiga avançar versões ou voltar versões sem ter tantas dificuldades.
       
    Nesse caso será abordado somente sobre o Git, mas existem outros.

## Mas afinal quem inventou o Git? qual é a história dele? 

### História do Git
Existia uma empresa chamada BitKeeper que guardava todo o cóigo do kernel do linux, então todo o linux era versionado nesse sistema, só que houve uma quebra entre a linux e a BitKeeper, fazendo com que a linux não fosse mais isenta de pagar pelo uso da ferramenta, com isso o linux teria que começar a pagar para usar.
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
