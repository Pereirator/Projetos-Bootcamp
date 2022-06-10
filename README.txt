31/05/22

SUPORTE: santander@dio.me

** Resgatar acesso ao GitHub no sábado (portifólio de projetos)

Para integração com a comunidade do bootcamp, utilizar os canais rooms e o forum.

As avaliações, desafios e projetos são verificadas pelo sistema se a solução foi atingida, caso esteja errado existe um sistema de pontuação (hearts), a cada cinco hearts perdidos o aluno terá que aguardar um tempo até poder realizar o teste novamente. O objetivo disso, é ajudar o aluno a se concentrar e não fazer o bootcamp muito rápido sem prestar atenção no que está aprendendo.

Os projetos serão submetidos pelo GitHub, é possível usar um fork do projeto base do expert, mas não há objeção contra baixar o código em zip ou iniciar do zero. Após concluído, selecionar a opção de entergar projeto na plataforma DIO e colar o link do repositório. Foi sugerido colocar descrição.



Escrever um aprendizado é como retirar da memória RAM e gravar no HD. Facilita o processo de aprendizado.

O pensamento computacional pode ser dividido em 4 pilares: 
- Decomposição: Dividir um problema maior e mais complexo em sudivisões mais simples e fáceis de ser resolvidas
- Reconhecimento de padões: Identificar padrões, tendências, similaridades e diferenças entre os problemas
- Abstração: Explorar o problema de uma forma generalista, uma fórmula matemática por exemplo pode ser aplicada de forma geral ao invés de uma única situação
- Design de Algoritmos: Definir passo a passo a solução do problema.

Outros processos que podem envolver o pensamento computacional:

RACIOCÍNIO LÓGICO <-> DECOMPOSIÇÃO <-> PADRÕES <-> ABSTRAÇÃO <-> ALGORITMOS <-> REFINAMENTO <-> RACIOCÍNIO LÓGICO...

O processo da decomposição envolve quebrar um problema maior em partes menores e menos complexas, porém também envolve recompor o problema original para dar sentido à solução.

É possível realizar uma decomposição sequencial ou paralela.


-----------------------------------------------------------
02/06/22 mentoria
parque de stacks F1RST:
FRONT END: ANGULAR
BACK END: JAVA 
FRAMEWORK: SPRING E APACHE CAMEL
INFRAESTRUTURA CLOUDS: AMAZON, AZURE, DATA CENTER EM CAMPINAS
MOBILE
ANDROID: JAVA, KOTLIN
IOS: OBJECTIVE 6, SWIFT (falta no mercado)

Atualização do app semanal (toda segunda-feira), release diária de atualização. Release de microserviços e angular (páginas SPA). É feito 4-20 deploys por dia através dos canais digitais.

Cloud, engenharia de software, técnicas de resiliência
---------------------------------------------------------

03/06/22
São chamados de instruções primitivas as operaçoes matemáticas (subtração, divisão, etc de nº reais ou inteiros) utilizadas no processamento dos dados de um algoritmo.

Estruturas condicionais de lógica de programação verificam se uma condição é verdadeira ou falsa, existem também estruturas de repetição (loop) onde novas varreduras podem ser executadas num ciclo definido ou então até atingir uma certa condição.

Vetores e matrizes são utilizados para economia de espaço, sendo necessário atribuir um menor número de variáveis dentro de um programa para armazenar valores. Uma lista é um tipo de vetor. 
Assim como em tabelas uma matriz é definida pelo nº de colunas e linhas. Os estacionamentos de shopping normalmente são organizados como matrizes, os corredores de uma direção recebem nº e os corredores interseccionais recebem letras.

Funções são blocos de código ou containers. O resultado obtido é retornado ao programa principal, mas  variável local contida dentro dela é desalocada da memória (ram).

Quando a saída do programa retorna com um resultado de erro de sintaxe, normalmente é mais fácil de identificar e corrigir o problema uma vez que o editor de código costuma informar a(s) linha(s) em que houve o problema. No entanto, também é possível que o código não apresente erro de sintaxe, apesar disso não imprime o resultado desejado (erro de semântica/significado), nesses casos é necessário verificar linha por linha até encontrar o problema.


Uma linguagem de programação é um método padronizado composto por um conjunto de regras sintáticas e semânticas de implementação de um código fonte.


06/06/2022

Paradigma são formas de resolução de um problema com diretrizes e limitações específicas de cada paradigma através de linguagem de programação.
Pode ser classificado como orientação à objeto (+ usado, ex: Java), procedural, funcional, estruturado (+ usado, ex: C), computação distribuída e lógico.


cmd

dir = lista 
cd / = change directory nome da pasta
cd .. = voltar
cls = limpar a tela
tab completa a digitação do nome de um arquivo ou pasta
mkdir = make directory/criar pasta, nome da pasta em seguida
echo > nomedoarquivo.txt = criação de um arquivo através do prompt
del = deletar arquivos de um repositório
a seta para cima é um atalho para acessar o histórico de comandos
rmdir = remove directory/apagar a pasta
"rmdir diretorio S/ Q/" = O S e o Q são flags, não entendi a aplicação, foi utilizado para apagagar a pasta teste workspace

08/06/22

O sha1 é um tipo de encriptação criada pela NSA e usada pelo sistema do GIT para identificar modificações. Alterando um simples ponto de um arquivo será gerado uma string de 40 digitos (hexadecimais pelo que eu notei) única. Caso hajam modificações posteriores de forma que o texto volte a apresentar a formatação original, a string gerada pelo sha1 será a mesma. Exemplo real de modificação abaixo de um arquivo chamado texto.txt :

591d24108360e3d58751fa3110bbf8244a50f8ff
b553914436cfb15ebe6425a1fe8d917b859ef17a
591d24108360e3d58751fa3110bbf8244a50f8ff

 - Blob armazena metadados de um objeto no GIT, contendo as seguintes informações: tipo, tamanho do arquivo/string, \0 o sha1 do arquivo e conteúdo. O blob encapsula o comportamento de diretórios de arquivos.
 - Trees também armazenam metadados, contendo o nome do arquivo, tamanho, o blob (as trees podem apontar para um blob ou para uma outra tree que pode apontar consequentemente para outro blob...) além de um sha1 encriptado especificamente para a tree. O sha1 da tree apesar de diferente do blob ao qual ela se relaciona, acompanha as modificações executadas no arquivo que ambos fazem referência. Ex:

	/ "README" - <Blob>
<Tree>	- "Rakefile" - <Blob>
	\ <Tree> - "simplegit.rb" - <Blob>

 - Commit é o objeto que junta tudo, ele aponta para uma árvore, um parente (para o último commit realizado antes dele), um autor e uma mensagem, possuem em seus metadados um timestamp que informa o dia e horário da modificação. A mensagem dá o significado para os arquivos que o commit faz referência e como medida de segurança é possível identificar facilmente a origem (autor) e horário (timestamp) daquela modificação. O commit possui um sha1 próprio.

Os arquivos que acabaram de ser criados ou que foram apagados estão na situação de não rastreados (untracked) pelo GIT, devemos deixá-los preparados na situação staged ao executar o comando git add (nome do arquivo), caso tenham mais alterações pode-se usar o comando git add *. Dessa forma, os arquivos saem do diretório de trabalho e vão para a staging area estando prontos para serem direcionados para o repositório Local, para isso basta dar o comando git commit -m e informar o resumo da modificação em aspas (git commit -m "alteração do título"). Somente com os arquivos commitados/dispostos no repositório local é que é possível enviar para o repositório Remoto/GitHub.

Para criar um repositório no GitHub entrar nas opções de perfil > Your Repositories > New

Será possível ver o link https da página do repositório, copiar e colar junto com o comando git remote add origin (git remote add origin https://github.com/Pereirator/Livro-de-receitas.git), sendo que o origin é um apelido usado para abreviar o endereço da página, dessa forma não será necessário colar no próximo comando. Para fazer o envio, empurrar as alterações para o repositório remoto (GitHub), o comando é: git push origin master

Este parágrafo foi criado especificamente para gerar um segundo commit no desafio de projeto.
