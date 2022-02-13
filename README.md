# Desenvolvimento Web - Trabalho 1
 
Alunos: Eliézer da Silva Vaz e Guilherme Müller

A classe Jogador possui os atributos: **cod_jogador**, que representa o ID do jogador, **nome**, **email** e **datanasc**. Também possui métodos **GET** e **SET** para recuperar e atualizar esses atributos. Além disso, a classe jogador conta com dois construtores: (utilizando o princípio de Overload de Programação Orientada a Objetos) um vazio e outro que faz o set dos atributos de nome, email e datanasc. Além disso essa classe cria uma tabela no banco de dados, em que as colunas são os atributos da classse.

A classe Pagamento possui os atributos: **cod_pagamento**, que representa o ID do pagamento, **ano**, **mes** e também o **valor** do pagamento. Além de possuir os métodos **GET** e **SET** para cada um desses atributos. Além disso essa classe cria uma tabela no banco de dados, em que as colunas são os atributos da classse. Pagamento possui um relacionamento de n,1 com a classe jogador, ou seja, um jogador pode possuir vários pagamentos, porém um pagamento só pode pertencer à um jogador. A classe pagamento também conta com dois construtores: um que inicaliza os atributos de ano, mês, valor e de ID do pagamento enquanto outro inicaliza os atributos de ano, mês, valor e de ID do pagamento e atribui esse pagamento a um jogador;

Através dos controllers de jogador e pagamentos, existem os seguintes métodos:

Para jogadores tem-se os seguintes métodos:

Caso não se utilize a ID de um jogador:

* get: http://localhost:8080/api/jogadores  busca todos os jogadores;<br/>
* get: http://localhost:8080/api/jogadores/?nome=[keyword]  busca todos os jogadores que nome contenha determinada palavra-chave;<br/>
* delete: http://localhost:8080/api/jogadores  deleta todos os jogadores;<br/>
* post: http://localhost:8080/api/jogadores  cria um novo jogador;<br/>

Caso se utilize o ID de um jogador pode se utilizar os seguintes métodos: <br/>

* get: http://localhost:8080/api/jogadores/{cod_jogador}  faz uma busca a um jogador com determinado ID;<br/>
* delete: http://localhost:8080/api/jogadores/{cod_jogador}  deleta um jogador com determinado ID;<br/>
* put: http://localhost:8080/api/jogadores/{cod_jogador}  atualiza os dados de um jogador com determinado ID;<br/>

Para pagamentos tem-se os seguintes métodos:

Caso não se utilize a ID de um pagamento:

* post: http://localhost:8080/pagamentos cria um novo pagamento;<br/>
* get: http://localhost:8080/pagamentos  busca todos os pagamentos; <br/>
* delete: http://localhost:8080/pagamentos  deleta todos os pagamentos; <br/>

Caso se utilize o ID de um pagamento pode-se utilizar os seguintes métodos:
* post: http://localhost:8080/pagamentosid  cria um pagamento relacionado a um jogador;<br/>
* put: http://localhost:8080/pagamentos/{cod_pagamento}  atualiza os dados do pagamento com determinado ID;<br/>
* delete: http://localhost:8080/pagamentos/{cod_pagamento}: deleta um pagamento com um determinado ID.

Vale ressaltar que os métodos put e post devem receber em seu corpo o respectivo objeto a ser criado ou alterado


Para o teste de comandos foi utilizado o software Insomnia pela praticidade de poder guardar os comandos para futuros testes. Podem ser vistos os resultados dos testes na pasta de Screenshots.
