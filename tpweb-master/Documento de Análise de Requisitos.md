# Documento de Análise de Requisitos

## 1. Introdução
Antes de construirmos qualquer projeto precisamos planejar todas nossa solução pode diversos A 1 pa corresponde à fase de levantamento de requisitos, na qual ter nomes variando de acordo com o paradigma de desenvolvimento adotado. Por exemplo, RUP da Rationa) essa conhecida de de Independente do modelo adotado é necessário levantar os requisitos funcionais e não funcionais Como exemplo, vamos propor o cenário para nosso projeto. Um cliente nos solicita sistema tem por objetivo básico controlar as vendas de seus produtos. O sistema deve basicamente registrar as vendas com data do pedido, o total nome do que emitiu o mesmo. previsão de entrega do pedido, deve ser Lembre-se de que todo pedido um emitido por um único vendedor, o qual deverá ser comissionado. Os produtos possuem a go de Barra) único, valor de venda, quantidade atual no estoque e quantidade minima que devem ser registrados. vendedores possuem uma matricula única, nome completo, data de nascimento percentual de Os possuir o status de pendente (A produtos com pedidos podem Os e entregue (neste caso, devemos marcar no sistema a data real de vamos basicamente são do tipo Pe e Não sendo que para os produtos armazenar informações sobre a data de validade e do Para os produtos na temos que armazenar o prazo de garantia dos produtos, o sistema deverá ser desenvolvido linguagem C# de dados Mysql s seguintes relatórios informativos foram solicitados pelo cliente de por vendedor no período; b) Produtos em falta no estoque Estoque atual d) Faturamento por periodo Com base nos requisitos acima precisamos passar para a 2a etapa de nosso projeto, ou seja fase de modelagem, do nosso dados quanto de classes de nosso sistema


## 2. Descrição do Problema
Algumas explicações sobre o diagrama Na classe venda, existe um método denominado Incluir, que não retorna nenhuma informação, ou seja, retorna void. Essa mesma explicação serve para as demais classes. Podemos perceber ainda o relacionamento todo-parte na forma de composição na relação entre as classes Venda e Itens e o relacionamento de agregação na relação Itens e Produto. A classe Produto passa a ser uma classe abstrata, a qual não poderá ser instanciada, auxiliando apenas no processo de modelagem As classes Perecivel e Não Perecivel são subclasses da classe Produto, o que demonstra a relação de herança. Com base na modelagem acima, precisamos passar para a 3a etapa de nosso projeto, a fase de prototipação, na qual as telas de nosso sistema serão desenvolvidas.

## 3. Objetivo

## 4. Escopo da Aplicação

## 5. Descrição do Produto

## 6. Casos de uso

## 7. Classes
![Imagem Diagrama de Classes - Ferramenta Astah](https://github.com/brunopego/tpweb/blob/master/imagens/Clas.jpg)

## 8. Banco de Dados
![Imagem Diagrama ER - Ferramenta MySql](https://github.com/brunopego/tpweb/blob/master/imagens/estoque.png)

## 9. Protótipos
* Link para os códigos fontes

## 10. Cronograma

## 11. Referências

