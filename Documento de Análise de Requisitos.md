# Documento de Análise de Requisitos

## 1. Introdução
Dada a necessidade de desenvolvermos um projeto para a disciplina de Sistemas Web I, identificamos a necessidade de um problema no estoque de pequenas empresas, a idéia inicial do projeto é comtemplar estoque de produtos unitários com apoio de simples sistema para gerenciar vendas desses produtos.


## 2. Descrição do Problema
O desenvolvimento de um sistema de estoque, requer o conhecimento detalhado do produto. Muitas vezes essa especificação pode fazer o produto se tornar específico e não suportando o gerenciamento de um estoque genérico. Como por exemplo o controle de produtos como peso, medida, entre outras especificações.

## 3. Objetivo
Com o objetivo de gerenciar estoques, o sistema será capaz de cadastrar diversos produtos e vendê-los de forma que a cada venda um vendedor seja comissionado. Portanto, quando registrado uma venda um vendedor deve estar associado, e os itens também devem ser cadastrados. Esses itens são compostos por produtos, no caso da venda de *n* produtos um único item, corresponde a esse produto, bem como a sua quantidade. O problema em questão é relacionar tais itens com os produtos registrados e dessa forma conseguir gerenciar o estoque.

## 4. Escopo da Aplicação
A área de domínio do projeto é cobrir a necessidade de um sistema gerencial, que é capaz de gerenciar o estoque de produtos, no nosso caso de produtos eletrônicos. Com isso o sistema é limitado a esse tipo de serviço, não atendendo a estoque de produtos que exijam data de validade, peso, ou características do tipo.

Para o desenvolvimento do sistema utilizamos um template grátis chamado [siminta][1] que serviu como base para a elaboração do projeto.

## 5. Descrição do Produto
Antes de construirmos o projeto precisamos planejar diversas soluções para a proposta. A primeira fase do projeto corresponde à fase de levantamento de requisitos, na qual definimos e analisamos o que seria necessário para desenvolvermos o projeto adotado. Como exemplo, vamos propor o cenário para nosso projeto. Um cliente nos solicita um sistema que tem por objetivo básico controlar as vendas de seus produtos. O sistema deve basicamente registrar as vendas com data do pedido, o total da venda e o nome do vendedor que emitiu o mesmo. Também a previsão de entrega do pedido, deve ser cadastrada. Lembrando de que todo pedido deverá ser emitido por um único vendedor, o qual deverá ser comissionado pela venda. Os produtos possuem um código único, valor de venda, quantidade atual no estoque e quantidade minima que devem ser registrados. Os vendedores possuem um código único, nome completo, data de nascimento e percentual de comissão. 

Os possuir o status de pendente (A produtos com pedidos podem Os e entregue (neste caso, devemos marcar no sistema a data real de vamos basicamente são do tipo Pe e Não sendo que para os produtos armazenar informações sobre a data de validade e do Para os produtos na temos que armazenar o prazo de garantia dos produtos, o sistema deverá ser desenvolvido linguagem C# de dados Mysql s seguintes relatórios informativos foram solicitados pelo cliente de por vendedor no período; b) Produtos em falta no estoque Estoque atual d) Faturamento por periodo Com base nos requisitos acima precisamos passar para a 2a etapa de nosso projeto, ou seja fase de modelagem, do nosso dados quanto de classes de nosso sistema
## 6. Casos de uso
  1. Caso de Uso
    * **Nome:** Cadastrar Venda
    * **Escopo:** STOCK_WEB
    * **Nível:** Objetivo de usuário
    * **Ator primário:** Operador
    * **Interessados:**
      1. _Usuário:_ Possibilita o usuário a cadastrar uma venda
      2. _Empresa:_ Garante o controle de estoque de acordo com o nivelamento atual
    * **Pré condições:**
      1. Usuário deve estar devidamente logado
      2. O estoque de um produto deve estar positivo e maior do que o solicitado na compra
    * **Garantias de sucesso:** Venda é feita com sucesso
    * **Cenário de sucesso principal:**
      1.	Usuário operador deve efetuar o login
      2.	Operador acessa a página de cadastro de vendas
      3.	Operador preenche os campos necessários para cadastro (Vendedor, Produto, Data da compra, Data prevista, Valor Unitário, Quantidade)
      4.	Operador efetua a venda.
      5.	Sistema faz o balanço de estoque e o armazenamento das informações no banco de dados.
    * **Extensões:**
      * a) Dados do usuário incorreto: Sistema sinaliza erro solicita reentrada dos dados
      * d) Venda só é realizada se há estoque disponível daquele produto:	Sistema sinaliza erro
    * **Requisitos especiais:**
      1. Texto visível até 1 metro de distancia 
    * **Frequência de ocorrência:** Diário/Semanal/Mensal
  
  2. Caso de Uso
    * **Nome:** Consultar Venda
    * **Escopo:** STOCK_WEB
    * **Nível:** Objetivo de usuário
    * **Ator primário:** Operador
    * **Interessados:**
      1. _Usuário:_ Possibilita o usuário a consultar as vendas cadastradas
      2. _Empresa:_ Fornece as informações de vendas já efetuadas
    * **Pré condições:**
      1. Usuário deve estar devidamente logado
    * **Garantias de sucesso:** Consulta é feita com sucesso
    * **Cenário de sucesso principal:**
      1.	Usuário operador deve efetuar o login
      2.	Operador acessa a página de consulta de vendas
      3.	Operador pesquisa a venda através de vários filtros disponíveis
    * **Extensões:**
      * a) Dados do usuário incorreto: Sistema sinaliza erro solicita reentrada dos dados
      * c) Pesquisa só é feita para dados existentes no banco de dados: Sistema sinaliza erro
    * **Requisitos especiais:**
      1. Texto visível até 1 metro de distancia 
    * **Frequência de ocorrência:** Diário/Semanal/Mensal
  
  3. Caso de Uso
    * **Nome:** Cadastrar produto
    * **Escopo:** STOCK_WEB
    * **Nível:** Objetivo de usuário
    * **Ator primário:** Operador
    * **Interessados:**
      1. _Usuário:_ Possibilita o usuário a cadastrar um novo produto
      2. _Empresa:_ Aumenta a diversidade de produtos ofertados
    * **Pré condições:**
      1. Usuário deve estar devidamente logado
    * **Garantias de sucesso:** Produto é cadastrado com sucesso
    * **Cenário de sucesso principal:**
      1.	Usuário operador deve efetuar o login
      2.	Operador acessa a página de cadastro de produtos
      3.	Operador insere a descrição do produto (Nome, valor unitário)
      4.	Usuário salva o novo cadastro do produto
    * **Extensões:**
      * a) Dados do usuário incorreto: Sistema sinaliza erro solicita reentrada dos dados
    * **Requisitos especiais:**
      1. Texto visível até 1 metro de distancia 
    * **Frequência de ocorrência:** Diário/Semanal/Mensal
  
  4. Caso de Uso
    * **Nome:** Excluir produto
    * **Escopo:** STOCK_WEB
    * **Nível:** Objetivo de usuário
    * **Ator primário:** Operador
    * **Interessados:**
      1. _Usuário:_ Possibilita o usuário a excluir um produto
      2. _Empresa:_ Elimina os produtos inativos da base de dados
    * **Pré condições:**
      1. Usuário deve estar devidamente logado
    * **Garantias de sucesso:** Produto é eliminado com sucesso
    * **Cenário de sucesso principal:**
      1.	Usuário operador deve efetuar o login
      2.	Operador acessa a página de exclusão de produtos
      3.	Operador insere o código do produto a ser deletado
      4.	Usuário confirma a exclusão do produto
    * **Extensões:**
      * a) Dados do usuário incorreto: Sistema sinaliza erro solicita reentrada dos dados
      * d) Exclusão só é feita para produtos existentes na base de dados:	Sistema sinaliza erro
    * **Requisitos especiais:**
      1. Texto visível até 1 metro de distancia 
    * **Frequência de ocorrência:** Diário/Semanal/Mensal
  
  5. Caso de Uso
    * **Nome:** Cadastrar vendedor
    * **Escopo:** STOCK_WEB
    * **Nível:** Objetivo de usuário
    * **Ator primário:** Operador
    * **Interessados:**
      1. _Usuário:_ Possibilita o usuário a cadastrar um novo vendedor
      2. _Empresa:_ Aumenta a quantidade de vendedores ligados à empresa
    * **Pré condições:**
      1. Usuário deve estar devidamente logado
    * **Garantias de sucesso:** Vendedor é cadastrado com sucesso
    * **Cenário de sucesso principal:**
      1.	Usuário operador deve efetuar o login
      2.	Operador acessa a página de cadastro de vendedores
      3.	Operador insere os dados do vendedor (Nome, data de nascimento, comissão, status)
      4.	Usuário salva o novo cadastro de vendedor
    * **Extensões:**
      * a) Dados do usuário incorreto: Sistema sinaliza erro solicita reentrada dos dados
    * **Requisitos especiais:**
      1. Texto visível até 1 metro de distancia 
    * **Frequência de ocorrência:** Diário/Semanal/Mensal
  
  6. Caso de Uso
    * **Nome:** Inativar vendedor
    * **Escopo:** STOCK_WEB
    * **Nível:** Objetivo de usuário
    * **Ator primário:** Operador
    * **Interessados:**
      1. _Usuário:_ Possibilita o usuário a inativar um vendedor
      2. _Empresa:_ Inativa o vendedor
    * **Pré condições:**
      1. Usuário deve estar devidamente logado
    * **Garantias de sucesso:** Vendedor é inativado com sucesso
    * **Cenário de sucesso principal:**
      1.	Usuário operador deve efetuar o login
      2.	Operador acessa a página de edição de vendedores
      3.	Operador insere o código do vendedor a ser inativado
      4.	Usuário confirma a inativação do vendedor
    * **Extensões:**
      * a) Dados do usuário incorreto: Sistema sinaliza erro solicita reentrada dos dados
      * d) A inativação só é feita para vendedores existentes na base de dados:	Sistema sinaliza erro
    * **Requisitos especiais:**
      1. Texto visível até 1 metro de distancia 
    * **Frequência de ocorrência:** Diário/Semanal/Mensal

## 7. Classes

Algumas explicações sobre o diagrama:
Na classe venda, existe um método denominado Incluir, que não retorna nenhuma informação, ou seja, retorna void. Essa mesma explicação serve para as demais classes. Podemos perceber ainda o relacionamento todo-parte na forma de composição na relação entre as classes Venda e Itens e o relacionamento de agregação na relação Itens e Produto. A classe Produto passa a ser uma classe abstrata, a qual não poderá ser instanciada, auxiliando apenas no processo de modelagem As classes Perecivel e Não Perecivel são subclasses da classe Produto, o que demonstra a relação de herança. Com base na modelagem acima, precisamos passar para a 3a etapa de nosso projeto, a fase de prototipação, na qual as telas de nosso sistema serão desenvolvidas.
![Imagem Diagrama de Classes - Ferramenta Astah](https://github.com/brunopego/tpweb/blob/master/imagens/Class.jpg)

## 8. Banco de Dados
![Imagem Diagrama ER - Ferramenta MySql](https://github.com/brunopego/tpweb/blob/master/imagens/estoque.png)

## 9. Protótipos

Os protótipos do projeto juntamente com o código fonte podem ser encontrado no link abaixo, onde basta acessar as páginas *html*

* https://github.com/brunopego/tpweb/tree/master/Stock_Web

## 10. Cronograma

## 11. Referências

[1]: http://www.free-css.com/free-css-templates/page197/siminta
1. http://www.free-css.com/free-css-templates/page197/siminta
