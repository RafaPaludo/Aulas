## 01) Lista com o nome de todas as mulheres:
~~~MySQL
SELECT nome FROM `gafanhotos`
WHERE sexo = 'F';
~~~


## 02) Lista com dados de todos aqueles que nasceram entre 1/Jan/2000 e 31/Dez/2015:
~~~MySQL
SELECT * FROM `gafanhotos`
WHERE nascimento BETWEEN '2000-01-01' and '2015-12-31';
~~~


## 03) Lista com nome de todos os homens que trabalham como Programadores:
~~~MYSQL
SELECT * FROM `gafanhotos` where sexo = 'm' and profissao = 'programador';
~~~


## 04) Lista com os dados de todas as mulheres que nasceram no Brasil e que têm seu nome iniciando com a letra J:
~~~MYSQL
SELECT * FROM `gafanhotos`
where sexo = 'f' and nacionalidade = 'Brasil' and nome LIKE "J%";
~~~


## 05) Lista com o nome e nacionalidade do todos os homens que têm Silva no nome, não nasceram no Brasil e pesam menos de 100kg:
~~~MYSQL
SELECT nome,nacionalidade FROM `gafanhotos`
where sexo = 'm' and nacionalidade != 'Brasil' and nome like "%silva%" and peso < '100';
~~~


## 06) Qual é a maior altura entre homens que moram no Brasil?:
~~~MYSQL
SELECT max(altura) FROM `gafanhotos` where nacionalidade = "brasil";
~~~


## 07) Qual a média de peso dos homens?:
~~~MYSQL
SELECT avg(peso) FROM `gafanhotos`
WHERE sexo = 'm';
~~~


## 08) Qual o menor peso entre as mulheres que nasceram fora do Brasil e entre 01/Jan/1990 e 31/Dez/2000?:
~~~MYSQL
SELECT min(peso) FROM `gafanhotos`
WHERE sexo = "f" and nacionalidade != "brasil" and nascimento BETWEEN '1990-01-01' and '2000-12-31';
~~~


## 09) Quantas mulheres têm mais de 1.90m de altura?:
~~~MYSQL
SELECT count(altura) from `gafanhotos` where sexo = 'f' and altura > '1.90';
~~~


## 10) Uma lista com as profissões dos gafanhotos e seus respectivos quantitativos.
~~~MYSQL
SELECT profissao, COUNT(*) from gafanhotos
GROUP by profissao;
~~~

## 11) Quantos homens e quantas mulheres nasceram após 01/Jan/2005?
~~~MYSQL
SELECT count(*) from gafanhotos
where nascimento > '2005-01-01'
GROUP by sexo;
~~~

## 12) Uma lista com os gafanhotos que nasceram fora do Brasil, mostrando o país de origem e o total de pessoas nascidas lá. Só nos interessam os países que tiverem mais de 3 gafanhotos com essa nacionalidade.
~~~MYSQL
select nacionalidade, count(*) from gafanhotos
GROUP by nacionalidade
HAVING count(nacionalidade) > 3 and nacionalidade != 'brasil';
~~~

## 13) Uma lista agrupada pela altura dos gafanhotos, mostrando quantas pessoas pesam mais de 100kg e que estão acima da média de altura de todos os cadastrados.
~~~MYSQL
select altura from gafanhotos where peso > 100 group by altura having altura > (SELECT avg(altura) from gafanhotos);
~~~