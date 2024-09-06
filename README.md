# Funções

Este repositório conterá minhas anotações sobre funções.

---

Funções nada mais são que o encapsulamento (ou empacotamento) de um bloco de ações que executa determinada tarefa mediante sua invocação. 

Uma das características da programação é a possibilidade de desenvolver aplicações replicáveis com códigos otimizados e estruturas que possam ser reaproveitadas ao longo do processo de execução de um algoritmo. O motivo disso é bem simples: aumenta-se a coesão e se diminui o acoplamento entre os módulos e partições de um código.

As funções na programação servem, basicamente, para se empacotar uma sequência de comandos que devem ser executados de maneira sequencial conforme haja a invocação explícita da função em qualquer ponto do código.

Função pode ser um arquivo separado puxado para dentro do seu arquivo ou um bloco dentro do mesmo arquivo puxado em alguma outra parte dele.

---

A nível de exemplo, pressuponha que você precisa fazer a validação de um campo de e-mail constante em seu site, entretanto, este mesmo campo de e-mail está presente em mais de 10 páginas. As opções para resolução deste problema seriam:

Escrever um código de validação em cada uma das 10 páginas e
a cada página nova que recebesse o campo de e-mail, o código deveria ser novamente escrito;
qualquer mudança na estrutura de validação necessitaria de uma modificação em cada uma das páginas que contivesse o código de validação
a manutenção do código seria manual, demorada e passível de erros.
Escrever apenas um código de validação, aloca-lo em um ambiente separado e
sempre que houvesse a necessidade de validar um campo de e-mail, faria-se a invocação do código de validação;
qualquer página nova que recebesse o campo de e-mail, precisaria apenas invocar este arquivo com o código de validação;
ainda que o site tivesse milhares de páginas, o código de validação seria apenas um, concentrado em apenas um local, o que facilitaria o processo de manutenção do algoritmo
Em suma, o uso de funções se resume exatamente a isso: alocar toda a estrutura de um algoritmo em um só local, de maneira que a manutenção geral do sistema seja mais eficiente, rápida e com menos chances de resultar em falhas ou erros.

---

### Escopo de funções

E para ficar mais prático, trabalharemos com o bloco de funções dentro da nossa tela para não ficarmos com vários arquivos, mas você consegue trabalhar com arquivo externo.

Uma função em Python é caracterizada pela palavra def, seguida de um nome e um par de parênteses: def nome_funcao(). Os nomes das funções podem ter a estrutura desejada, mas eles devem seguir os mesmos princípios dos nomes de variáveis, ou seja, sem espaços, sem caracteres especiais e sem iniciar com números.

def soma():          (ESCOPO DA FUNÇÃO)
    a = 2 + 3;       (ESCOPO DA FUNÇÃO)

print(soma())        (INVOCAÇÃO DA FUNÇÃO)

Ao executar este trecho de código, todavia, o resultado “none” é apresentado no console de nossa IDE. Isso ocorre porque toda função, por ser um pacote fechado, ela guarda para si o resultado de seu processamento, ou seja, ainda que a função “soma” tenha realizado de fato uma soma e atribuído o resultado a variável “a”, este resultado ficou “preso” dentro do escopo da própria função, não retornando o número 5.

Assim, sempre que uma função precisar de fato retornar algum valor ao trecho que a invoca, é necessário utilizar o comando return como última instrução da função. Atente-se a este detalhe: o return precisará sempre ser a última instrução, pois tanto o Python quanto outras linguagens simplesmente irão ignorar qualquer código que for alocado após a palavra “return”.

def soma():        
    a = 2 + 3;       
    return a

print(soma()) 

---

Obviamente que ter uma função com valores fixos não torna o código tão atrativo e sequer escalável. Espera-se que uma função seja capaz de interagir com o usuário, recebendo valores dinâmicos e utilizando este valores para executar ações.

Para isso, existem os conceitos de argumentos e parâmetros.

Os argumentos são enviados no ato de invocação de uma função e então, são recebidos como parâmetros pela função. Entenda que um argumento e um parâmetro, na prática, são a mesma coisa, mas recebem nomes diferentes dependendo do local em que estiverem.

Agora iremos analisar linha a linha para compreender em detalhes o que está sendo feito. Para fins didáticos, iniciaremos na linha 119 e depois partiremos para a linha 115.

Linha 119: foi disparado um comando de impressão na tela. Este comando invoca a função “soma”, passando dois argumentos numéricos: 2 e 3;
Linha 115: a função soma é definida e recebe dois parâmetros (argumentos enviados). Esses parâmetros são armazenados em “a” e “b”;
Linha 116: Uma variável “c” é criada e recebe a soma de “a” e “b”, que são os parâmetros recebidos;
Linha 117: A função “soma” retorna o valor da variável “c”, que por sua vez, é transferido à linha 119, responsável pela impressão do resultado na tela.
Desta forma, uma mesma função pode executar várias somas diferentes, desde que valores diferentes sejam enviados via argumento como é apresentado na Figura 30.

def soma(a, b):
    c = a + b;
    return c

print(soma(2, 3))
print(soma(1, 10))
print(soma(6, 20))
print(soma(9 , 8))

TODA FUNÇÃO TEM UMA CARACTERÍSTICA:

FUNÇÃO (A PALAVRA-CHAVE)
NOME DA FUNÇÃO
() PARÊNTESES (ONDE POSSO PASSAR ALGUNS VALORES)
CORPO DA FUNÇÃO (PODEMOS TER QUANTAS LINHAS DESEJARMOS)
RETORNO (TODA FUNÇÃO DEVE RETORNAR UM VALOR CASO VOCÊ QUEIRA IMPRIMIR ALGO NA TELA)

---

PARA CHAMAR UAM FUNÇÃO É NECESSÁRIO O USO DA PALAVRA-CHAVE def (def de define pois você irá definir uma função)

EM SEGUIDA DEFINIMOS O NOME DA FUNÇÃO

---

#### A LÓGICA POR TRÁS DAS FUNÇÕES:

Você precisa escrever um código/algoritmo em Python e precisa recorrentemente escrever esse mesmo código em vários arquivos/páginas/telas diferentes.

E você tem uma mesma estrutura sendo repetida várias vezes e temos 2 formas mais práticas e inteligentes de fazer essa estrutura:

PRIMEIRA: FUNÇÕES
SEGUNDA: ORIENTAÇÃO A OBJETOS

Você está desenvolvendo um site e esse site tem uma tela, nessa tela tem um trecho de código em Python, e esse trecho de código executa uma função no escopo da página.

Esse trecho de código tem um total de 30 linhas.

BLOCOS CUJA FUNÇÃO CHAMA-SE SOMA:

def soma():
   print("Imprimindo função na tela")

PARA CHAMAR ESSA FUNÇÃO NA TELA:

soma()

Essa função não tem um retorno porque dentro do código da própria função já estamos imprimindo um conteúdo, então não preciso fazer um comando de impressão quando for chamar a função.

SE EU NÃO TENHO UM COMANDO DE PRINT NA TELA, EU PRECISO APONTAR UM RETORNO.

def soma():
    txt = "Imprimindo resultado com variável"
    return txt

print(soma())

TEMOS O ARQUIVO DE FUNÇÃO POR FORA E O CÓDIGO FONTE.

NO SITE DA RECEITA FEDERAL, O USUÁRIO DIGITARÁ O CPF NO CÓDIGO FONTE, O NÚMERO DIGITADO SERÁ ENVIADO PARA O ARQUIVO DE FUNÇÃO E O ARQUIVO DE FUNÇÃO IRÁ VALIDAR ESSE CPF, OU O CPF ESTÁ VÁLIDO OU ESTÁ INVÁLIDO.

ESSA INFORMAÇÃO DE QUE SE O CPF ESTÁ VÁLIDO OU INVÁLIDO VOLTA PARA A TELA DO CÓDIGO FONTE NO MOMENTO EM QUE DAMOS UM RETORNO (return).

A FUNÇÃO DO RETORNO É ABASTECER O MEU ARQUIVO/TELA/ALGORITMO COM ALGUM DADO/INFORMAÇÃO QUE EU QUEIRA BASEADO NA EXECUÇÃO DA MINHA FUNÇÃO.

---

#### FUNÇÕES RECURSIVAS

Na função recursiva, chamamos a função dentro da própria função, de forma que conseguimos deixar o código muito mais compacto e mais otimizado.

Uma função recursiva segue os mesmos princípios de uma função não-recursiva, porém com uma característica peculiar: ela chama a ela mesma dentro de seu próprio escopo, ou seja, ela executa a si própria até chegar atingir o que chamamos de “case base”. Este caso base é o ponto que definimos como limite para que a função cesse sua execução e então retorne os resultados.

Para somar 2 números, posso criar a variável C e fazer com que ele receba a soma de a + b. Porém a minha função não sabe quem é o a e o b, pois não é uma variável, elas são valores que estão vindo de algum lugar como parâmetros.

Então como essa função soma irá funcionar?
Na hora que eu chamar a função irei passar dois valores ( a e b) e esses valores serão recebidos pela minha função na parte de cima.
E ao serem recebidos, eles serão calculados em forma de soma e atribuídos a minha variável c.

E isso na prática facilitará muito o processo de desenvolvimento, pois sempre que você precisar realizar algum tipo de cálculo você não precisará criar toda essa estrutura, você irá apenas chamar a função, passar os números que você deseja somar e a própria estruturá fará o cálculo por você.

def soma(a, b):
    c = a + b
    return c

print(soma(4,9))

---

PARA VERIFICAR SE A VARÍAVEL C É PAR:

def soma(a,b)
    c = a + b
    if c % 2 == 0:
       return "Par"
    else:
       return "Ímpar"

print(soma(4,9,8))

---

### EXEMPLOS PRÁTICOS DE FUNÇÕES

Como base para estudos, iremos utilizar uma função recursiva para fazer um algoritmo de fatorial. Um número fatorial, na matemática, é representado por n!, em que n equivale a um número qualquer multiplicado por seus antecessores, por exemplo:

Representação de um fatorial: 5! = 5 * 4 * 3 * 2 * 1 = 120

E conseguimos fazer validação de CPF utilizando o cálculo fatorial.

FAZENDO UMA FUNÇÃO RECURSIVA QUE RESOLVA O CÁLCULO FATORIAL:

---

É possível escrever esta instrução utilizando uma função recursiva. Existem outras formas de fazer isso também (uma delas é com laço de repetição) mas faremos com funções para que consigamos aplicar o conhecimento aprendido de forma prática.

def fatorial(n):
    if n == 1:
         return 1
    return n * fatorial(n - 1)

print(fatorial(5))

Vamos detalhar a execução de cada linha, iniciando pela linha 129 e em seguida partindo para a linha 124:

Linha 129: Imprime-se na tela o resultado advindo da função fatorial, a qual recebe como argumento o número 5;
Linha 124: A função fatorial é definida e recebe-se um parâmetro n que, no caso, equivale ao número 5, enviado como argumento;
Linha 125: Define-se o caso base, ou seja, o ponto em que a função deve parar de ser executada, evitando um loop infinito. Neste caso, quando o valor de n for igual a 1, a função chega ao seu caso base e retorna o valor 1 (linha 126);
Linha 127: É onde a mágica de fato acontece. O retorno da função será uma nova chamada para a mesma função, porém com argumentos diferentes: passa-se o valor n-1, ou seja, o valor 4;
Linha 124: o valor 4 é recebido e como ele não é igual a 1 (linha 125), ele parte para a linha 127, que invoca novamente a função, passando o valor n-1, ou seja, 3;
Isso ocorre de forma sequencial até que o valor de n seja igual a 1, recaindo então sobre a linha 125, que é o caso base.

Funções recursivas tendem a ser bastante céleres, mas dependendo do valor de entrada elas podem demorar consideravelmente para finalizarem o ciclo de execução, desta forma, o ideal é analisar a complexidade de algoritmos para avaliar se uma função recursiva é a melhor opção dentro do algoritmo que você estiver desenvolvendo.

---

### EXEMPLOS PRÁTICOS DE FUNÇÕES INSERIDS PELO USUÁRIO

Com a inserção de um input (utilizando o casting de Inteiro), o usuário consegue inserir qualquer número e deixar que a função fatorial() resolva seu cálculo.

def fatorial(n):
    if n == 1:
        return 1
    return n * fatorial (n - 1)

valor = int(input("Digite um número: ")
print(fatorial(valor))

---

### FUNÇÕES NATIVAS

Essas funções que criamos até aqui são chamadas de funções de usuário, uma vez que são criadas pelo programador, que define todas as regras de seu escopo. Existem, entretanto, funções e tipos integrados nativos do próprio Python (Python.org), que podem ser utilizadas a qualquer momento (e algumas até já utilizadas em nossas aulas, como a input() e a print().

Na documentação oficial do Python você encontra uma lista completa de funções nativas, listas em ordem alfabética.

---

### TESTANDO FUNÇÕES

Embora existam muitas funções nativas do Python, algumas são, indiscutivelmente, mais utilizadas que outras. Abaixo você encontra uma lista de funções bem interessantes que vale a penas você conhecer e testar:

abs(): retorna o valor absoluto de um número;
pow(): realiza cálculos de potência;
next(): retorna o próximo elemento de uma lista iterativa
hash(): retorna o valor em hash de um objeto
open(): permite trabalhar com arquivos (veremos isso mais adiante!)

CHAMAR OUTRAS FUNÇÕES DENTRO DA FUNÇÃO: FUNÇÃO RECURSIVA

CHAMAR UMA OUTRA FUNÇÃO QUE NÃO ESTÁ CHAMANDO ELA MESMA (FUNÇÃO EXTERNA)

### TÓPICOS AVANÇADOS

Existem alguns tipos de estrutura de dados na computação e uma delas é a lista.

A lista pode ser do tipo Pilha ou Fila. Uma pilha, como o nome já alude, empilha dados (variáveis, posições de vetor ou informações) como se fosse uma pilha de pratos. O último prato inserido é o primeiro que deve ser retirado. Já uma fila, aloca os dados de maneira sequencial, mas o primeiro elemento que entra é também o primeiro a sair.

### Leitura complementar

“Estrutura de Dados em C”.

 Embora seja uma linguagem pesada, a C é perfeita para se compreender a estrutura de dados de forma profunda.

 ---

 ### CÓDIGOS UTILIZADOS NA DISCIPLINA

 https://github.com/FaculdadeDescomplica/Python













