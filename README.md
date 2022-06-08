## PCD - Como usar o Git?

No presente repositório desenvolvido para a aula de Prática em Ciência de Dados, é descrito como utilizar o Git.

## Grupo 5
- Artur Hosoi Kimura
- Débora van Putten Chaves
- Pedro Henrique Machado Zanineli
- Pedro Thomazelli Ferreira

### Criação e edição do repositório

Como ponto de partida, o Github foi aberto em um navegador e, na parte superior da esquerda da tela inicial, criamos um repositório, adicionando um arquivo do tipo *README.md* e outros detalhes, um ponto que é relevante ser destacado é o quesito das licensas, que são de extrema importância quando for definir o que outras pessoas podem e o que não podem fazer com seu código. no caso, utilizaremos o GNU General Public License, ou seja, manteremos o código aberto. Em seguida, criamos um arquivo em Python seguindo o caminho `Add File > Create new file`, além de ter realizado uma alteração no *README*.

Tanto na sua criação quanto na alteração, realizamos o *commit*, que pode ser entendido como o ato de tornar permanente uma alteração que foi feita, sendo que sempre pode ser acompanhado de uma mensagem. Uma vez que os *commits* foram feitos, é possível clicar no símbolo de relógio na interface do Github para voltar em um determinado momento.

### Tranferindo um repositório para uma pasta local

Para que possamos trabalhar com as pastas localmente no computador, primeiramente criamos uma pasta local, clicamos com o botão direito do mouse nela e abrimos o painel do Git Bash, em seguida utilizamos o comando __git clone link_do_repositório__, sendo que o link é obtido clicando no botão `Code ` no GitHub e copiando o link disponibilizado (é importante selecionar a opção __HTTPS__, quando gerar o link). Após executar o código, todos os arquivos presentes no momento no repositório são transportados à pasta local especificada.

Também é de extrema importância ressaltar que, toda vez que algum arquivo é alterado localmente, isto é, diretamente num arquivo no computador, as edições não são sincronizadas aos arquivos do repositório no GitHub, sendo assim, é necessário executar uma série de comandos para que sejam armazenadas. Em primeira instância, podemos utilizar o comando __git status__ no diretório para ver se existe algum arquivo que foi alterado e ainda não "salvo". Caso exista, devemos usar o comando __git add .__ (ou __git add nome_do_arquivo_alterado__) seguido pelo __git commit -m "nome_do_arquivo_alterado"__, que irá "confirmar" a edição e gerar a mensagem de *commit*, mas você poderá perceber que as mudanças ainda não foram armazenadas no repositório do GitHub. Para que isso aconteça, é necessário utilizar o  comando __git push__, para finalmente mandar as edições de volta e atualizar o conteúdo do repositório.

### Push do repositório

Em uma pasta criada localmente no computador, buscamos agora, através do comando __git push__ (depois da utilização do comando __git add nome_do_arquivo__ (ou __git add .__, nesse caso não é necessário especificar o nome do arquivo), e do comando __git commit -m "nome_do_arquivo_alterado"__), transferir o tudo o que editamos/criamos definitivamente para o repositório alvo online, no GitHub.

### Pull do repositório

Utilizamos o comando __git pull__ no Git Bash sempre que desejamos transferir algo modificado ou criado no próprio repositório online do GitHub (após os devidos procedimentos de armazenamento dos arquivos, como o commit) para uma pasta criada localmente no computador, como se fosse o processo inverso do __git push__.

### Criando branchs
- Diretamente no GitHub
1. Página principal do repositório;
2. Apertar "main"
3. Criar um branch

__Informações relevantes:__
<br> O que é "branch"?: Branch não é um código novo, mas uma versão nova do seu código 
<br> Alterações nos arquivos (como add uma nova linha) não são automáticas e criar um novo branch, por exemplo, também NÃO é: logo, depois de criá-lo, também precisamos dar um pull no Bash;
<br> A main é um branch também, mas é o 'main branch';
<br> Merge vai juntar as nossas branchs e, depois disos, alterar uma não é sinônimo de alterar a outra;

### Mudança de branch

`git checkout 'nome_branch'` para mudar para uma determinada branch

### Fork e pull request

Um Fork é utilizado quando se quer fazer uma cópia do repositório de uma outra pessoa, permitindo a "clonagem" e modificação os arquivos livremente sem a preocupação de alterar o projeto original. É possível fazer um Fork clicando no botão cinza de mesmo nome no canto superior direito da tela (não é possível criar um Fork de um respositório criado por você mesmo).

Após fazer as modificações e edições desejadas nos arquivos, e tomar as medidas necessárias para armazenar as mudanças (os mesmos comandos para armazenar informações alteradas demonstradas anteriormente), é ainda possível mandá-los de volta para o desenvolvedor original, através do `Pull request`(disponível na aba de ações na parte mais superior da interface, posicionada ao lado da opção "Issues"), porém, o mesmo poderá decidir atualizar seu código com as suas alterações ou rejeitá-las, dependendo de como julgá-las úteis ou melhores que as originais.

<hr>

## Anotações relevantes
#### Geral
<br> __ReadMe__ > cartão de visitas do repositório, com a finalidade de exibir uma descrição do mesmo.
<br>Se os dados forem privados/secretos/particulares, __não__ faça um repositório aberto, porque QUALQUER UM pode acessar. Sempre converse sobre isso com as demais pessoas envolvidas no projeto;
<br>Precisamos escolher __licenças__ para os nossos repositórios, o professor gosta da GNU, que é um Software livre;
<br>As mudanças só são salvas quando apertamos o __commit__ e, para isso, precisamos adicionar uma breve descrição na aba de commit contando o que foi feito;
<br>Arquivos novos criados em 'add file' precisam terminar com ".py", porque eles são extensões de arquivos do Python;
<br>Não precisamos fazer commits o tempo todo, mas é muito interessante e útil enunciar as mudanças que estão sendo feitas. Depois, você consegue navegar no seu histórico de edições com mais facilidade;
<br>O GitHub vai salvando todas as alterações que a gente faz, mantendo as coisas antigas: ele permite que voltemos no tempo e para acessar esse recurso basta clicar em "<>" após acessar "commits + um símbolo de histórico ao lado";
<br> __DICA DE OURO__: dá um pull antes de fazer qualquer coisa, porque vai que tem outra pessoa alterando o arquivo e você não tá ligado;
<br> Alterações __NÃO__ são automáticas, mudar algo no computador não é o mesmo que mudar direto no GitHub vice-versa! Fique atento a isso.

#### Comandos essenciais
<br>Importante:
<br> 1. __git status__: exibe o status do repositório local em relação ao repositório alvo, avisando caso exista alguma alteração a ser salva
<br> 2. __cd__ (change directory): muda de "pastas"/diretórios
<br> 3. __ls__ (list): fala o que tem dentro de diretório
<br> 4. __git add .__ : declara que quer que as alterações que foram realizadas sejam consideradas, muda os arquivos
<br> 5. __git push__: comando final que manda para o servidor o que fizemos, ou seja, tira só do computador e manda para a internet
<br> 6. __git pull__: transporta alterações feitas na internet para o próprio computador;
<br> 7. __git commit -m "..."__: quando fazemos alguma alteração no GitHub na internet, nada funciona se não dermos o "commit". Fazendo as mudanças no computador é a mesma coisa, precisamos dar o commit também para que a mudança seja salva;
