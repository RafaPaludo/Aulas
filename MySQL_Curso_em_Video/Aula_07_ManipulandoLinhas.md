- Não é possível modificar várias linhas ao mesmo tempo. Porém pode-se modificar uma linha e dentro dela, várias colunas de uma vez. Usamos o UPDATE, SET e WHERE para modificar a tabela, o valor desejado e o local onde a informação se encontra.

~~~MySQL
update cursos
set nome = 'HTML5' 
WHERE idcurso = '1';
~~~

- LIMIT numero, limita a quantidade de linhas para o comando.

~~~MySQL
update cursos
set nome = 'HTML5' 
WHERE idcurso = '1'
LIMIT 1;
~~~

- Para apagar uma linha, usar o comando `DELETE`.

~~~MySQL
delete from cursos
WHERE idcurso = '8';
~~~

- Remover todas as linhas de uma tabela `TRUNCATE`.

~~~MySQL
TRUNCATE TABLE cursos;
~~~

- UPDATE - DML
- DELETE - DML
- TRUNCATE - DML