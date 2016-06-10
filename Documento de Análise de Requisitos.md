# Documento de Análise de Requisitos

## 1. Introdução



## 2. Descrição do Problema

## 3. Objetivo

## 4. Escopo da Aplicação

## 5. Descrição do Produto
Antes de construirmos o projeto precisamos planejar diversas soluções para a proposta. A primeira fase do projeto corresponde à fase de levantamento de requisitos, na qual definimos e analisamos o que seria necessário para desenvolvermos o projeto adotado. Como exemplo, vamos propor o cenário para nosso projeto. Um cliente nos solicita um sistema que tem por objetivo básico controlar as vendas de seus produtos. O sistema deve basicamente registrar as vendas com data do pedido, o total da venda e o nome do vendedor que emitiu o mesmo. Também a previsão de entrega do pedido, deve ser cadastrada. Lembrando de que todo pedido deverá ser emitido por um único vendedor, o qual deverá ser comissionado pela venda. Os produtos possuem um código único, valor de venda, quantidade atual no estoque e quantidade minima que devem ser registrados. Os vendedores possuem um código único, nome completo, data de nascimento e percentual de comissão. 

Os possuir o status de pendente (A produtos com pedidos podem Os e entregue (neste caso, devemos marcar no sistema a data real de vamos basicamente são do tipo Pe e Não sendo que para os produtos armazenar informações sobre a data de validade e do Para os produtos na temos que armazenar o prazo de garantia dos produtos, o sistema deverá ser desenvolvido linguagem C# de dados Mysql s seguintes relatórios informativos foram solicitados pelo cliente de por vendedor no período; b) Produtos em falta no estoque Estoque atual d) Faturamento por periodo Com base nos requisitos acima precisamos passar para a 2a etapa de nosso projeto, ou seja fase de modelagem, do nosso dados quanto de classes de nosso sistema
## 6. Casos de uso
  1. Caso de Uso
    * **Nome:**

## 7. Classes

Algumas explicações sobre o diagrama Na classe venda, existe um método denominado Incluir, que não retorna nenhuma informação, ou seja, retorna void. Essa mesma explicação serve para as demais classes. Podemos perceber ainda o relacionamento todo-parte na forma de composição na relação entre as classes Venda e Itens e o relacionamento de agregação na relação Itens e Produto. A classe Produto passa a ser uma classe abstrata, a qual não poderá ser instanciada, auxiliando apenas no processo de modelagem As classes Perecivel e Não Perecivel são subclasses da classe Produto, o que demonstra a relação de herança. Com base na modelagem acima, precisamos passar para a 3a etapa de nosso projeto, a fase de prototipação, na qual as telas de nosso sistema serão desenvolvidas.
![Imagem Diagrama de Classes - Ferramenta Astah](https://github.com/brunopego/tpweb/blob/master/imagens/Clas.jpg)

## 8. Banco de Dados
![Imagem Diagrama ER - Ferramenta MySql](https://github.com/brunopego/tpweb/blob/master/imagens/estoque.png)

## 9. Protótipos
* https://github.com/brunopego/tpweb/tree/master/tpweb-master/Stock_Web

## 10. Cronograma

## 11. Referências

