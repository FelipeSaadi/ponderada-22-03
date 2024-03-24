# Ponderada-22-03

## Tecnologia
K6 é uma ferramenta open-source de teste de performance de aplicações. Com ela é possível testar a aplicação tanto em sua confiabilidade como na sua performance, por meio da preparação de conjuntos de testes com diferentes níveis de carga.

Com ela é possível fazer os seguintes testes:
* Teste de Carga;
* Teste de Navegador;
* Teste de Caos e Resiliência da Aplicação;
* Monitoramento de Performance com Periodicidade.

Funcionalidades do K6:
* CLI tool amigável para desenvolvedores de APIs;
* Scripts em Javascript com suporte a Módulos;
* Checks e Thresholds para apoiar a construção de objetivos de monitoramento e automação.

## Conceitos aprendidos
Aprendi a diferença real entre teste de carga e teste de stress, assim como as diferentes parametrizações responsáveis por manipular os testes de carga, permitindo criar testes de monitoramento dinâmicos, com VUs randomizadas e escaladas em diferentes níveis, diferentes conjuntos de dados e coletas de métricas.

No resultado gerado pelo K6, aprendi a ler as informações representadas, sendo capaz de identificar problemas, capturar pontos a serem melhorados e entender as circunstâncias que fazem com que uma aplicação falhe.

## Teste a ser efetuado
Será testado o endpoint de consulta de todas as pesquisas, utilizando 10000 VU (usuários virtuais) e com duração de execução do teste em 15 segundos.

## Executando o teste
Algumas requisições retornaram corretamente, enquanto outras não puderam ser respondidas pela máquina.

![image](https://github.com/FelipeSaadi/ponderada-22-03/assets/54749257/683df5f5-df2f-44dd-a5ca-a2affa3458fc)

![image](https://github.com/FelipeSaadi/ponderada-22-03/assets/54749257/00f18b06-573e-4e20-b1a8-72c0acc16827)

### Quantidade de requisições
Foram enviadas 24496 (1400 req/s).

### Data sended
Foram enviados 570kb de dados (33kB/s).

### Data received
Foram recebidos 7.3mb de dados (420kB/s).

### Duração da Requisição
As requisições duraram em média 149.6ms para serem respondidas para o cliente.

### Taxa de sucesso nas requisições
Das 24496 requisições feitas, 18361 (74.95%) foram mal-sucedidas e 6135 (25.05%) foram bem sucedidas.

### Resultado do teste
A aplicação não é capaz de lidar com uma grande carga de usuários em um espaço curto de tempo, a aplicação acaba sendo derrubada, necessitando que ela seja levantada novamente. Para resolver isso, será necessário implementar tratativas de erros na aplicação, como o try catch, para impedir que a mesma quebre quando não consegue lidar com erros. A implementação de um sistema de filas para acesso ao banco e controle de carga auxiliaria a aplicação a performar com essas altas cargas de solicitações.
