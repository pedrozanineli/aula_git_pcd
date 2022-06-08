## PCD - Como usar o Git?

No presente repositório desenvolvido para a aula de Prática em Ciência de Dados, é descrito como utilizar o Git.

### Grupo 5
- Artur Hosoi Kimura
- Débora van Putten Chaves
- Pedro Henrique Machado Zanineli
- Pedro Thomazelli Ferreira

### <a name="sumario">Sumário</a>
1. [Criação e edição do repositório](#edicao)
2. [Repositório remoto para uma pasta local](#transferencia)
3. [*Push* do repositório](#push)
4. [*Pull* do repositório](#pull)
4. [Criação de *branches*](#branches)
5. 

---

### <a name="edicao">Criação e edição do repositório</a> | [Voltar](#sumario)

Como ponto de partida, o Github foi aberto em um navegador e, na parte superior da esquerda da tela inicial, criamos um repositório, adicionando um arquivo do tipo *README.md* e outros detalhes. Um ponto que é relevante ser destacado é o quesito das licensas, que são de extrema importância na definição do que outras pessoas podem e o que não podem fazer com seu código. No caso, utilizaremos o GNU General Public License, ou seja, manteremos o código aberto. Em seguida, criamos um arquivo em Python seguindo o caminho `Add file > Create new file` (poderíamos também ter feito um upload de arquivo a partir do computador), além de ter realizado uma alteração no *README*.

Tanto na sua criação quanto na alteração, realizamos o *commit*, que pode ser entendido como o ato de tornar permanente uma alteração que foi feita, sendo que sempre pode ser acompanhado de um nome e uma mensagem. Uma vez que os *commits* foram feitos, é possível clicar no símbolo de relógio na interface do Github para voltar em um determinado momento, ou seja, restaurar uma versão específica do código.

### <a name="transferencia">Repositório remoto para uma pasta local</a> | [Voltar](#sumario)

Para que possamos trabalhar com as pastas localmente no computador, primeiramente criamos uma pasta local, clicamos com o botão direito do mouse nela e abrimos o painel do *Git Bash*. Em seguida, utilizamos o comando `git clone 'link do repositório'`, sendo que o link é obtido clicando no botão `Code` no GitHub e copiando o link disponibilizado (é importante selecionar a opção __HTTPS__, quando a janela for aberta). Após executar o código, todos os arquivos presentes no momento que estão no repositório são transportados à pasta local especificada.

Também é de extrema importância ressaltar que, toda vez que algum arquivo é alterado localmente, isto é, diretamente num arquivo no computador, as edições não são sincronizadas aos arquivos do repositório no GitHub, sendo assim, é necessário executar uma série de comandos para que sejam armazenadas. Em primeira instância, podemos utilizar o comando `git status` no diretório para ver se existe algum arquivo que foi alterado e ainda não "salvo" no repositório remoto (arquivos *staged*, *unstaged* e *untracked*).

Caso existam arquivos que ainda não foram carregados, podemos usar o comando `git add .` ou `git add 'nome do arquivo alterado'` - para indicar quais arquivos desejamos realizar o upload, de forma que adicionará todos os arquivos e um especificado, respectivamente - seguido por `git commit -m "explicação da alteração"`, que irá "confirmar" a edição e gerar a mensagem de *commit*. Ainda é possível perceber que as mudanças ainda não foram armazenadas no repositório do GitHub. Para que isso aconteça, é necessário utilizar o  comando `git push`, para finalmente "mandar" as edições de volta e atualizar o conteúdo do repositório remoto.

### <a name="push">*Push* do repositório</a> | [Voltar](#sumario)

Em uma pasta criada localmente no computador, buscamos agora, através do comando `git push` (depois da utilização do comando `git add 'nome do arquivo'` - ou `git add .`, para não especificar o nome do arquivo - , e do comando `git commit -m "explicação da alteração"`), transferir o tudo o que editamos/criamos definitivamente para o repositório alvo online, no GitHub.

### <a name="pull">*Pull* do repositório</a> | [Voltar](#sumario)

Utilizamos o comando `git pull` no *Git Bash* sempre que desejamos transferir algo modificado ou criado no próprio repositório online do GitHub (após os devidos procedimentos de armazenamento dos arquivos, como o commit) para uma pasta criada localmente no computador, sendo o processo inverso do `git push`.

### <a name="branches">Criação de *branches*</a> | [Voltar](#sumario)

Sobre *branches* de um código, podemos entendê-las não como um novo código, mas uma versão alternativa do seu código, um "universo paralelo" do que está acontecendo em um principal. Alterações nos arquivos (como adicionar uma nova linha) não são automáticas e criar um novo branch, por exemplo, também não é: logo, depois de criá-lo, também precisamos dar um *pull* no *Bash*. Note que a *main* também é uma *branch*, porém a principal, e o *merge* irá juntar duas *branches*, de forma que, depois disso, alterar uma não é sinônimo de alterar a outra;

Para criar uma *branch* - diretamente no GitHub:
1. Página principal do repositório;
2. Apertar "main";
3. Escrever o nome desejado para a ramificação;
4. Clicar no botão `Create branch: 'nome da branch' from main`.

### Mudança de branch

`git checkout 'nome_branch'` para mudar para uma determinada branch

### Fork e pull request

Um Fork é utilizado quando se quer fazer uma cópia do repositório de uma outra pessoa, permitindo a "clonagem" e modificação os arquivos livremente sem a preocupação de alterar o projeto original. É possível fazer um Fork clicando no botão cinza de mesmo nome no canto superior direito da tela (não é possível criar um Fork de um respositório criado por você mesmo).

Após fazer as modificações e edições desejadas nos arquivos, e tomar as medidas necessárias para armazenar as mudanças (os mesmos comandos para armazenar informações alteradas demonstradas anteriormente), é ainda possível mandá-los de volta para o desenvolvedor original, através do `Pull request`(disponível na aba de ações na parte mais superior da interface, posicionada ao lado da opção "Issues"), porém, o mesmo poderá decidir atualizar seu código com as suas alterações ou rejeitá-las, dependendo de como julgá-las úteis ou melhores que as originais.

<hr>

## Anotações relevantes
### Geral
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
