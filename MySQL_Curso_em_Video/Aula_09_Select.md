- Selecionar os dados de uma tabela, selecionando as colunas desejadas. 

```MySQL
SELECT id, nome, profissao, nascimento, sexo, peso, altura, nacionalidade FROM nome_da_tabela;
```

ou

```MySQL
SELECT * FROM nome_da_tabela;
```

- Podemos usar modificadores de exibição dos resultados pra filtrar:
    - ORDER BY nome_campo;
    - ORDER BY nome_campo asc | desc;
    - ORDER BY nome_campo, nome_campo_2, nome_campo_3 ...;

    - WHERE nome_campo < | > | <= | >= | = | != valor;
    - WHERE nome_campo BETWEEN valor AND valor;
    - WHERE nome_campo IN (valor, valor, valor ...);
    - WHERE nome_campo valor AND | OR valor;


- Operador LIKE "val%". Usado para retornar qualquer registro que começe com val.
- Wildcards:
    -%. Substitui nenhum ou qualquer caractere.
    -_. Obriga a ter ALGUM caractere.


- DISTINCT é usado para retornar apenas uma ocorrência caso existam vários registros iguais.

```MySQL
SELECT DISTINCT name FROM nome_da_tabela;
```

- Podemos agrupar o retorno com o comando GROUP BY. 
```MySQL
SELECT name FROM nome_da_tabela
GROUP BY name;
```

- Ainda com o GROUP BY, podemos filtrar os resultados com HAVING termo > | < | != | = ... termo;

- Podemos agrupar o retorno com o comando GROUP BY. 
```MySQL
SELECT name FROM nome_da_tabela
GROUP BY name
HAVING name != 'Rafael';
```


### Funções de Agragação:
- Funções que executam algo dentro do comando.
    - COUNT() => conta a quantidade de registros que seriam retornados.
    - MAX() => retorno o maior valor;
    - MIN() => retorno o menor valor;
    - SUM() => retorna o valor somado;
    - AVG() => retorna média dos valores;

*SELECT é um comando DML ou DQL.