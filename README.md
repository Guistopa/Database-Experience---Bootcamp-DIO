# Database-Experience - Bootcamp-DIO
## Desafio DIO Banco de Dados Ecommerce
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



## Segundo Desafio - Oficina  Motocar

Administrar uma oficina mecânica tem especificidades que outro negócio não tem, como o conhecimento técnico, mas a base é a mesma de qualquer empreendimento. Além de prestar um bom serviço, o negócio de carros exige boa apresentação, bom atendimento e conhecimentos de gestão. É um desafio diário, que exige comprometimento do proprietário. Assim, a empresa CENTROCAR percebeu a necessidade de criar e manter um banco de dados com o intuito de auxiliar uma tomada de decisão orientada por dados. Desse modo, foi contruido de acordo com as necessidades da empresa o seguinte modelo conceitual:

Ficha do Veículo

Placa VARCHAR(7): É a chave primária dessa entidade;
Modelo VARCHAR(45): Armazena o modelo do carro;
Ano YEAR: Armazena o ano de fabricação do carro;
Características gerais do veículo VARCHAR(45) (câmbio, combustível, pneus, etc): Armazena características das peças do carro.

Clientes

CPF VARCHAR(11): É a chave primária dessa entidade e tem o propósito da identificação do cliente;
IdentidadeVARCHAR(12): identificação do cliente;
PagamentoVARCHAR(16): Método de pagamento escolhido, possui quatro variáveis: cartão de débito, cartão crédito, dinheiro, pix;

Serviço

Natureza do serviço BIT(8): Descreve qual o tipo de serviço foi requerido pelo cliente, sendo as opções:Reparos automotivos (1), Troca de óleo (2),Alinhamento e, balanceamento (3), Manutenção de embreagem (4), Revisão dos componentes de freio (5), Checagem do nível de água no radiador (6), Revisão Geral (7), outro (8). Os dados serão armazenados de acordo com a numeração de cada tipo, sendo assim, 0 a 7;
Urgência BIT(2): Descreva se o serviço precisa ser realizado com urgência. Tem como data type boolean, sendo 0 'sem urgência' e 1 'com urgência';
Descrição do serviço VARCHAR(256): Descreve alguma especificação sobre o serviço (opcional). Orçamento
Peças BIT(2) (câmbio, combustível, pneus, etc): Descreve se o foi comprado/consertado determinada peça do carro. Tem como data type boolean, sendo 0 'não trocou' e 1 'trocou', existe um atributo para cada peça;
Mão de obra BIT(4): descreve o valor da mão de obra de acordo com tempo estimado que será necessário para o concerto. Desse modo, os dados serão armazenados de 0 a 3 e que indicam as seguintes informações 1-7 dias (1), 8-14 dias (2), 9-21 dias (3), > 1 mês (4);

Equipe

Numero de Funcionarios INT: Descreve quantos funcionários tem na equipe;
Especialidade VARCHAR(45): Descreve a especialidade da equipe;
Relacionamento: Valor do Pagamento
Preço DOUBLE: descreve o valor total a ser pago apartir das variaveis serviço e orçamento.

Resultado
A seguir se encontra o resultado do  desafio pode ser observado no Arquivo 2°  Desafio Ecomerce Banco de Dados.png

## Terceiro  Desafio - E-Commerce- SQL

### Descrição do Desafio

Replique a modelagem do projeto lógico de banco de dados para o cenário de e-commerce. Fique atento as definições de chave primária e estrangeira, assim como as constraints presentes no cenário modelado. Perceba que dentro desta modelagem haverá relacionamentos presentes no modelo EER. Sendo assim, consulte como proceder para estes casos. Além disso, aplique o mapeamento de modelos aos refinamentos propostos no módulo de modelagem conceitual.

Assim como demonstrado durante o desafio, realize a criação do Script SQL para criação do esquema do banco de dados. Posteriormente, realize a persistência de dados para realização de testes. Especifique ainda queries mais complexas dos que apresentadas durante a explicação do desafio. Sendo assim, crie queries SQL com as cláusulas abaixo:

Recuperações simples com SELECT Statement
Filtros com WHERE Statement
Crie expressões para gerar atributos derivados
Defina ordenações dos dados com ORDER BY
Condições de filtros aos grupos – HAVING Statement
Crie junções entre tabelas para fornecer uma perspectiva mais complexa dos dados
Diretrizes
Não há um mínimo de queries a serem realizadas;
Os tópicos supracitados devem estar presentes nas queries;
Elabore perguntas que podem ser respondidas pelas consultas;
As cláusulas podem estar presentes em mais de uma query;
O projeto deverá ser adicionado a um repositório do Github para futura avaliação do desafio de projeto. Adicione ao Readme a descrição do projeto lógico para fornecer o contexto sobre seu esquema lógico apresentado.

Objetivo:
[Relembrando] Aplique o mapeamento para o  cenário:

“Refine o modelo apresentado acrescentando os seguintes pontos”

Cliente PJ e PF – Uma conta pode ser PJ ou PF, mas não pode ter as duas informações;
Pagamento – Pode ter cadastrado mais de uma forma de pagamento;
Entrega – Possui status e código de rastreio;
Algumas das perguntas que podes fazer para embasar as queries SQL:

Quantos pedidos foram feitos por cada cliente?
Algum vendedor também é fornecedor?
Relação de produtos fornecedores e estoques;
Relação de nomes dos fornecedores e nomes dos produtos;


Resultado pode ser observado no arquivo Banco de Dados E-commerce SQL

## Quarto Desafio - E-Commerce- SQL

### Descrição do Desafio

Para este cenário você irá utilizar seu esquema conceitual, criado no desafio do módulo de modelagem de BD com modelo ER, para criar o esquema lógico para o contexto de uma oficina. Neste desafio, você definirá todas as etapas. Desde o esquema até a implementação do banco de dados. Sendo assim, neste projeto você será o protagonista. Tenha os mesmos cuidados, apontados no desafio anterior, ao modelar o esquema utilizando o modelo relacional.

Após a criação do esquema lógico, realize a criação do Script SQL para criação do esquema do banco de dados. Posteriormente, realize a persistência de dados para realização de testes. Especifique ainda queries mais complexas do que apresentadas durante a explicação do desafio. Sendo assim, crie queries SQL com as cláusulas abaixo:

Recuperações simples com SELECT Statement;
Filtros com WHERE Statement;
Crie expressões para gerar atributos derivados;
Defina ordenações dos dados com ORDER BY;
Condições de filtros aos grupos – HAVING Statement;
Crie junções entre tabelas para fornecer uma perspectiva mais complexa dos dados;
Diretrizes
Não há um mínimo de queries a serem realizadas;
Os tópicos supracitados devem estar presentes nas queries;
Elabore perguntas que podem ser respondidas pelas consultas
As cláusulas podem estar presentes em mais de uma query
O projeto deverá ser adicionado a um repositório do Github para futura avaliação do desafio de projeto. Adicione ao Readme a descrição do projeto lógico para fornecer o contexto sobre seu esquema lógico apresentado.

Resultado pode ser observado no arquivo Banco de Dados Oficina SQL
