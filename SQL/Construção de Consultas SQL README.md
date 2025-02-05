# Construção de Consultas SQL  
Ao construir consultas SQL, é importante planejar os passos para garantir eficiência, clareza e resultados precisos.  
Antes de escrever uma consulta, pense na pergunta de negócio que deseja responder e identifique a tabela ou tabelas que contêm os dados que você precisa.  

Exemplo:
* __Pergunta do Negócio__:
"Quais foram os pedidos realizados em janeiro de 2023?"

* __Tabela relevante__: pizzavendas.
  No caso da tabela pizzavendas, ela contém variáveis como:
  * Identificadores do pedido (order_id, order_details_id).
  * Detalhes da pizza (pizza_name, pizza_size, pizza_ingredients).
  * Informações financeiras (unit_price, total_price).
  * Datas e horários do pedido (order_date, order_time).

* __Dado relevante__: Decida quais informações da tabela são necessárias para responder às perguntas do negócio e quais variáveis são relevantes para análise.
  Isso ajudará a otimizar as consultas e garantir que apenas os dados essenciais sejam processados.


# Realizando a consulta:

* "Pergunta": Qual foi o faturamento total em janeiro de 2023 por tamanho de pizza?"  
* "Identifique a Tabela": pizzavendas.  
* Adicione um Filtro: Filtre os registros para o mês de janeiro de 2023 usando WHERE:

"WHERE order_date BETWEEN '2023-01-01' AND '2023-01-31';"  

* Especifique as Colunas:  
Selecione apenas as colunas necessárias:  
"pizza_size" para agrupar por tamanho.  
"total_price" para calcular o faturamento.  

* Agrupe os Dados e Some os Valores:  
Use GROUP BY para agrupar por tamanho de pizza e SUM para calcular o faturamento total:

##### Exemplo Completo

SELECT pizza_size, SUM(total_price) AS faturamento_total
FROM pizzavendas
WHERE order_date BETWEEN '2023-01-01' AND '2023-01-31'
GROUP BY pizza_size
ORDER BY faturamento_total DESC;

##### Explicação da Consulta:
SELECT pizza_size, SUM(total_price):
Escolhe o tamanho da pizza e calcula a soma do faturamento total.

FROM pizzavendas:
Informa que os dados serão extraídos da tabela pizzavendas.

WHERE order_date BETWEEN '2023-01-01' AND '2023-01-31':
Filtra os registros apenas para o mês de janeiro de 2023.

GROUP BY pizza_size:
Agrupa os dados por tamanho de pizza.

ORDER BY faturamento_total DESC:
Ordena os resultados do maior para o menor faturamento.

##### Resultados Esperados
pizza_size	faturamento_total
Grande	5,000.00
Médio	3,500.00
Pequeno	2,000.00

