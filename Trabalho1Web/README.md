# Trabalho1Web
 
Alunos: Eliézer da Silva Vaz e Guilherme Müller

A classe Jogador possui os atributos: cod_jogador, que representa o ID do jogador, nome, email e datanasc. Também possui métodos get e set para recuperar e atualizar esses atributos. Além disso, a classe jogador conta com dois construtores: (utilizando o princípio de Overload de Programação Orientada a Objetos) um vazio e outro que faz o set dos atributos de nome, email e datanasc. Além disso essa classe cria uma tabela no banco de dados, em que as colunas são os atributos da classse.

A classe Pagamento possui os atributos: cod_pagamento, que representa o ID do pagamento, ano, mes e também o valor do pagamento. Além de possuir os métodos get e set para cada um desses atributos. Além disso essa classe cria uma tabela no banco de dados, em que as colunas são os atributos da classse. Pagamento possui um relacionamento de n,1 com a classe jogador, ou seja, um jogador pode possuir vários pagamentos, porém um pagamento só pode pertencer à um jogador. A classe pagamento também conta com dois construtores: um que inicaliza os atributos de ano, mês, valor e de ID do pagamento enquanto outro inicaliza os atributos de ano, mês, valor e de ID do pagamento e atribui esse pagamento a um jogador;

Através dos controllers de jogador e pagamentos, existem os seguintes métodos:

Para jogadores tem-se os seguintes métodos:

Caso não se utilize a ID de um jogador:

/jogadores get: busca todos os jogadores;<br/>
/jogadores delete: deleta todos os jogadores;<br/>
/jogadores post: cria um novo jogador;<br/>

Caso se utilize o ID de um jogador pode se utilizar os seguintes métodos

/jogadores get: faz uma busca a um jogador com seterminado ID;<br/>
/jogadores delete: deleta um jogador com determinado ID;<br/>
/jogadores put: atualiza os dados de um jogador com determinado ID;<br/>

Para pagamentos tem-se os seguintes métodos:

Caso não se utilize a ID de um pagamento:
/pagamentos get: busca todos os pagamentos através da ID de um jogador; <br/>
/pagamentos delete: deleta todos os pagamentos de um jogador; <br/>

Caso se utilize o ID de um pagamento pode-se utilizar os seguintes métodos:
/pagamentosid post: cria um pagamento relacionado a um jogador;<br/>
/pagamentos put: atualiza os dados do pagamento com determinado ID.<br/>

O servidor atende na URL http://localhost:8080/api 

Para o teste de comandos foi utilizado o software Insomnia pela praticidade de poder guardar os comandos para futuros testes. Podem ser vistos os resultados dos testes na pasta de Screenshots.

