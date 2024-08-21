# anotacoes-funcoes
Este repositório conterá minhas anotações sobre funções.

---

Função pode ser um arquivo separado puxado para dentro do seu arquivo ou um bloco dentro do mesmo arquivo puxado em alguma outra parte dele.

E para ficar mais prático, trabalharemos com o bloco de funções dentro da nossa tela para não ficarmos com vários arquivos, mas você consegue trabalhar com arquivo externo.

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













