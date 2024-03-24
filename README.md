# ponderada-22-03

## Teste a ser efetuado
Será testado o endpoint de consulta de todas as pesquisas, utilizando 10000 VU (usuários virtuais) e com duração de execução do teste em 15 segundos.

## Executando o teste
Algumas requisições retornaram corretamente, enquanto outras não puderam ser respondidas pela máquina.

![image](https://github.com/FelipeSaadi/ponderada-22-03/assets/54749257/683df5f5-df2f-44dd-a5ca-a2affa3458fc)

![image](https://github.com/FelipeSaadi/ponderada-22-03/assets/54749257/00f18b06-573e-4e20-b1a8-72c0acc16827)
### Quantidade de requisições
Foram enviadas 24496 (1400 req/s)
### Data sended
Foram enviados 570kb de dados (33kB/s)
### Data received
Foram recebidos 7.3mb de dados (420kB/s)
### Duração da Requisição
As requisições duraram em média 149.6ms para serem respondidas para o cliente
### Taxa de sucesso nas requisições
Das 24496 requisições feitas, 18361 (74.95%) foram mal-sucedidas e 6135 (25.05%) foram bem sucedidas

### Resultado do teste
A aplicação não é capaz de lidar com uma grande carga de usuários em um espaço curto de tempo, a aplicação acaba sendo derrubada, necessitando que ela seja levantada novamente. Para resolver isso, será necessário implementar tratativas de erros na aplicação, como o try catch, para impedir que a mesma quebre quando não consegue lidar com erros. A implementação de um sistema de filas para acesso ao banco e controle de carga auxiliaria a aplicação a lidar com essas altas cargas de solicitações.
