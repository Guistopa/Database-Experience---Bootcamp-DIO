# Database-Experience---Bootcamp-DIO
Desafio DIo Banco de Dados Ecommerce
Sobre
O desafio propõe a análise de um cenário em que a empresa fictícia ECOMMERCE Loja Mais Barato busca agragar as informações sobre suas vendas. Desse modo, se faz necessario a criação de um banco de dados que possui as entidades produto, estoque, fornecedor, pedido e cliente. Assim, é desafiado ao participante a execução da criação de um projeto conceitual a partir de um modelo ER.

As entidades requeridas pelos stakeholders possuem as seguintes características:

Com relação aos produtos

São vendidos por uma unica plataforma online, contudo, estes podem ter vendedores distintos
Cada produto possui apenas um fornecedor
Um pedido pode ser composto por um ou mais produtos.

Com relação aos clientes

o cliente pode se cadastrar no site com CPF ou CNPJ
O endereço irá determinar o valor do frete
Um cliente pode comprar mais de um pedido. Este tem um período de arência para devolução do produto
Com relação aos pedidos

Os Pedidos são Criados por clientes e possuem informações de compra, endereço e status da entrega
Um produto ou mais compoem o pedido
O pedido pode ser cancelado

Com relação aos Fornecedores e Estoque
cabe ao participante modelar essas informações

Metodologia

Projeto Conceitual

Um modelo conceitual é um modelo abstrato que descreve a estrutura de um banco de dados de forma independente do SGBD. Dessa forma, será usado o workbanch do mysql, para criar um diagrama de relações de entidades. Nele será descritos as entidades e seus atributos previamente definidos pelas partes interessadas, incremento dos atributos requeridos de Fornecedores e estoque, assim como foi definido pelo participante alguns refinamentos. Sendo eles:

Cliente PJ e PF – Uma conta pode ser PJ ou PF, mas não pode ter as duas informações, dessa forma, foi criado a entidade informação que relaciona o CPF/CNPJ com o email do cliente(id), assim como foi criado um atributo booleano que explicita o tipo de registro legal, caso seja um CPF será atribuído 0 e caso CNPJ será atribuído 1;
Pagamento – Pode ter cadastrado mais de uma forma de pagamento, sendo definido a opção de registrar apenas 1 informação por método;
Entrega – Possui status, código de rastreio e data máxima de entrega;
O resultado desse processose encontra no arquivo Desafio Ecomerce Banco de Dados. png
