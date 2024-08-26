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

def soma():
    a = 2 + 3;

print(soma())

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













