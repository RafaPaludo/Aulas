- Para adicionar um novo campo (nova coluna), usaremos o comando `ALTER TABLE node_tabela ADD COLUMN nome_campo_novo valor_novo_campo`:

```MySQL
ALTER TABLE pessoas
ADD COLUMN profissao varchar(10);
```

- Para remover um campo, usaremos o comando de alterar a tabela junto com o `DROP COLUMN nome_coluna`:

```MySQL
ALTER TABLE pessoas
DROP COLUMN profissao;
```

- Para adicionar o campo em outro lugar, que não seja o último, podemos usar o `FIRST` ou `AFTER nome_campo` para posicionar onde desejarmos.

```MySQL
ALTER TABLE pessoas
DROP COLUMN profissao FIRST;
```

```MySQL
ALTER TABLE pessoas
DROP COLUMN profissao AFTER nome;
```

- Para modificar o tipo e as constraints da coluna, usar o comando `MODIFY` e passando os novos valores. Nesse caso, irá alterar tudo para os novos valores.

```MySQL
ALTER TABLE pessoas
MODIFY COLUMN nacionalidade varchar(50);
```

- Para modificar o NOME da coluna, usar o `CHANGE COLUMN`. Passar o nome antigo, o novo e todas as constraints e tipo da coluna.

```MySQL
ALTER TABLE pessoas
CHANGE COLUMN nacionalidade nac varchar(20) NOT NULL DEFAULT 'Brasil';
```

- Renomear o nome da tabela. Usar `RENAME TO novo_nome`:
```MySQL
ALTER TABLE pessoas
RENAME TO peoples;
```