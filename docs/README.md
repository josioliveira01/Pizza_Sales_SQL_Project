# 📋 Passo a Passo para importar o arquivo do computador
#### Acesse o SQLite Online
Abra o navegador e vá para o site do SQLite Online ([sqliteonline.com](https://sqliteonline.com/)).
Na interface inicial, você verá um editor SQL no lado direito e a estrutura de banco de dados no lado esquerdo.

#### Importe os Arquivos CSV
O arquivo devem estar organizado e salvo no seu computador.
#### Utilize a Opção "Import"
Na parte superior central da interface, localize a opção Import.
* Clique em Import para abrir as opções de importação.
* No menu Import, clique em Open.
- Isso abrirá o gerenciador de arquivos do seu computador.
- Selecione o arquivo correspondente que deseja importar:
- Pizza Vendas → pizzavendas.csv
- Confirme a seleção para carregar o arquivo na plataforma.

Na janela de importação, revise:
- Tipo: Deve estar como CSV.
- Delimitador: Configure conforme o arquivo (padrão é vírgula).
- Column Name: Altere de New Auto para First Line, para que a primeira linha do arquivo seja usada como nome das colunas.
- Após confirmar que os nomes das colunas estão corretos (ex.: "pizza_id", "total_pizza"), clique em OK.
- Verifique que a tabela foi importada corretamente no painel lateral esquerdo.

Agora que a tabela pizzavendas foi importada com sucesso, você pode realizar a primeira consulta para visualizar os dados.  

SELECT * FROM pizzavendas;  

Após inserir o código no editor, selecione-o e clique em Run para executá-lo.
Os resultados da consulta serão exibidos abaixo da área de edição.

##### 📌 Boa Prática
Sempre use o ponto e vírgula (;) ao final de cada comando SQL, mesmo que seu SGBD não o exija.
