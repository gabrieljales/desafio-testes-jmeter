# Teste de Desempenho


Este repositório contém os relatórios e resultados dos testes de desempenho realizados para a aplicação Regres API, utilizando o [Apache JMeter](https://jmeter.apache.org/download_jmeter.cgi).


## Ferramentas Utilizadas 🛠️

Os testes foram executados com as seguintes ferramentas e plugins:


- **Apache JMeter**: Ferramenta principal para execução dos testes de desempenho.

- **Regres API**: Aplicação testada, especificamente na rota **GET /api/users?page=2**. Mais informações podem ser encontradas [aqui](https://reqres.in/).

- **Plugin Manager**: Necessário para a instalação de plugins adicionais, disponível [aqui](https://jmeter-plugins.org/install/Install/).

- **Custom Thread Groups**: Plugin necessário para utilizar o **Stepping Thread Group**, disponível [aqui](https://jmeter-plugins.org/?search=jpgc-casutg).

- **3 Basic Graphs**: Plugin utilizado para visualização de gráficos adicionais, disponível [aqui](https://jmeter-plugins.org/?search=jpgc-graphs-basic).


## Desafios Propostos 📊


### Teste de Carga

- **Cenário**: Simule 100 usuários simultâneos fazendo requisições ao endpoint de **GET /api/users?page=2**.

- **Objetivo**: Medir o tempo médio de resposta, throughput e a taxa de erro.

- **Critério de Sucesso**: O tempo médio de resposta deve permanecer abaixo de 2 segundos para 95% das requisições, com uma taxa de erro inferior a 1%.


### Teste de Estresse

- **Cenário**: Inicie com 10 usuários simultâneos e aumente gradualmente até 500 usuários no endpoint de **GET /api/users?page=2**.

- **Objetivo**: Identificar o ponto em que o tempo de resposta começa a se deteriorar ou ocorrem erros frequentes.

- **Critério de Sucesso**: A API deve suportar até 300 usuários simultâneos com um tempo de resposta abaixo de 3 segundos e taxa de erro inferior a 5%.


## Plugins Instalados 🔌

- **Custom Thread Groups**: Instalado para utilizar o **Stepping Thread Group** e realizar o desafio de Teste de Estresse.

- **3 Basic Graphs**: Instalado para visualizar gráficos como "Active Threads Over Time", "Response Times Over Time" e "Transactions Per Second".

## Resultados 📈

- Os resultados do teste de carga estão descritos [aqui](teste_carga_100_users/RESULTS.md).

- Os resultados do teste de estresse estão descritos [aqui](teste_estresse_10min/RESULTS.md).

---