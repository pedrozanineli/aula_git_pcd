## PCD - Como usar o Git?

No presente repositório desenvolvido para a aula de Prática em Ciência de Dados, é descrito como utilizar o Git.

### Criação do repositório

Como ponto de partida, o Github foi aberto em um navegador e, na parte superior da esquerda da tela inicial, criamos um repositório, adicionando um arquivo do tipo *README.md* e outros detalhes. Em seguida, criamos um arquivo em Python seguindo o caminho `Add File > Create File`, além de ter realizado uma alteração no *README*.

Tanto na sua criação quanto na alteração, realizamos o *commit*, que pode ser entendido como o ato de tornar permanente uma alteração que foi feita, sendo que sempre pode ser acompanhado de uma mensagem. Uma vez que os *commits* foram feitos, é possível clicar no símbolo de relógio na interface do Github para voltar em um determinado momento.

### Push do repositório

Em uma pasta criada localmente no computador, buscamos agora 

### Pull do repositório

### Criando branchs
- Diretamente no GitHub
1. Página principal do repositório;
2. Apertar "main"
3. Criar um branch

Informações relevantes:
<br> O que é "branch"?: Branch nãoé um código novo, mas uma versão nova do seu código 
<br> Alterações nos arquivos (como add uma nova linha) não são automáticas e criar um novo branch, por exemplo, também NÃO é: logo, depois de criá-lo, também precisamos dar um pull no Bash;
<br> A main é um branch também, mas é o 'main branch';
<br> Merge vai juntar as nossas branchs e, depois disos, alterar uma não é sinônimo de alterar a outra;

### Mudança de branch

`git checkout 'nome_branch'` para mudar para uma determinada branch

### Fork e pull request

<hr>

## Anotações relevantes
#### Geral
<br>ReadMe > cartão de visitas do repositório
<br>Se os dados forem privados/secretos/particulares, não faça um repositório aberto, porque QUALQUER UM pode acessar;
<br>Precisamos escolher licenças para os nossos repositórios, o professor gosta da GNU, que é um Software livre;
<br>As mudanças só são salvas quando apertamos o commit e, para isso, precisamos adicionar uma breve descrição na aba de commit contando o que foi feito;
<br>Arquivos novos criados em 'add file' precisam terminar com ".py", porque eles são extensões de arquivos do Python;
<br>Não precisamos fazer commits o tempo todo, mas é muito interessante e útil enunciar as mudanças que estão sendo feitas;
<br>O GitHub vai salvando todas as alterações que a gente faz, mantendo as coisas antigas: ele permite que voltemos no tempo e para acessar esse recurso basta clicar em "<>" após acessar "commits + um símbolo de histórico ao lado";
<br> DICA DE OURO: dá um pull antes de fazer qualquer coisa, porque vai que tem outra pessoa alterando o arquivo e você não tá ligado;
<br> Alterações NÃO são automáticas, mudar algo no computador não é o mesmo que mudar direto no GitHub vice-versa! Fique atento a isso.

#### Comandos essenciais
<br>Importante:
<br> git status: ZANI EXPLICA AQUI
<br> cd (change director): muda de "pastas"
<br> ls (list): fala o que tem dentro de diretório
<br> git add . : declara que quer que as alterações que foram realizadas sejam consideradas, muda os arquivos
<br> push: comando final que manda para o servidor o que fizemos, ou seja, tira só do computador e manda para a internet
<br> git commit -m "...": quando fazemos alguma alteração no GitHub na internet, nada funciona se não dermos o "commit". Fazendo as mudanças no computador é a mesma coisa, precisamos dar o commit também para que a mudança seja salva;
<br> git pull: transporta alterações feitas na internet para o próprio computador;
 
