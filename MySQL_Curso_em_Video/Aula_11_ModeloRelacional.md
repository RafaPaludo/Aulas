## Modelo Relacional
- Temos ENTIDADES, que representam uma tabela no BD.
- Cada entidade possui dados, chamados de ATRIBUTOS. Um atributo principal é a CHAVE PRIMÁRIA.
- Duas ou mais entidades se relacionam, essa interação é o RELACIONAMENTO.
- Cardinalidade, quantidade de relação que uma entidade pode ter com outra.

## Diagrama Entidade Relacionamento - DER
- Diferentes tipos de relacionamentos:
    - Muitos para muitos, n -> n
    - Um para um, 1 -> 1
    - Um para muitos, 1-> n | n -> 1

- Relacionar duas entidades é na verdade pegar uma chave primária e enviar para a outra entidade, virando assim uma chave ESTRANGEIRA.

- Regras: 
    - Um para um, pode juntar as duas tabelas se fizer sentido. Ou deixa separado e joga a chave primária de um para a entidade dominante.
    - Um para muitos, chave primária do lado UM e coloca no lado muitos como chave estrangeira.
    - Muitos para muitos, o relacionamento vira uma entidade. Essa nova entidade se relaciona com cada entidade em 1 -> N | 1 -> N. A regra dai é a mesma da anterior. 

## Engine de Banco de dados
- MyISAM
- InnoDB - Padrão
- ExtraDB

- ACID:
    - Atomicidade: ou tudo aconte, ou nada é considerado
    - Consistência: antes e depois da transação devem ser mantidos
    - Isoalmento: ações não podem ocorrer ao mesmo tempo
    - Durabilidade: dados se deve manter pelo tempo que for necessário 