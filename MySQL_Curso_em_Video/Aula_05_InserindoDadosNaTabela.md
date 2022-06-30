CREATE TABLE / DATABASE - São comandos DDL - DataDefinitionLenguage

- Nessa aula, vimos o comando de inserção de dados na tabela. Para inserir algum dado, basta usar o comando `INSERT INTO nome_tabela`, passar os dados da tabela que serão inseridos e os valores para cada dado especificado na ordem correta.

```MySQL
INSERT INTO pessoas
(nome, nascimento, sexo, peso, altura, nacionalidade)
VALUES
('Godofredo', '1984-01-02', 'M', '78.6', '1.83', 'Brasil');
```

- Para dados definidos como DEFAULT na criação da tabela, podemos passar apenas o valor DEFAULT também no INSERT INTO. Nesse caso seria o ID e NACIONALIDADE.

```MySQL
INSERT INTO pessoas
(id, nome, nascimento, sexo, peso, altura, nacionalidade)
VALUES
(DEFAULT, 'Maria', '1990-05-10', 'F', '58.6', '1.53', DEFAULT);
```

- Se a ordem dos campos for exatamente igual a ordem definida nos campos, não é necessário informar os dados no comando.

```MySQL
INSERT INTO pessoas VALUES 
('Godofredo', '1984-01-02', 'M', '78.6', '1.83', 'Brasil');
```

- Para inserir vários dados ao mesmo tempo, é possível, só precisa passar cada um separado por ,.

```MySQL
INSERT INTO pessoas
(id, nome, nascimento, sexo, peso, altura, nacionalidade)
VALUES
(DEFAULT, 'Rafael', '1997-05-30', 'M', '73.6', '1.79', DEFAULT),
(DEFAULT, 'Mike', '1980-07-10', 'M', '108.6', '1.93', 'Rússia'),
(DEFAULT, 'Suzan', '1995-06-02', 'F', '85.6', '1.73', 'EUA');
```

INSERT INTO - São comandos DML - DataManipulationLenguage
