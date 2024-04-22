# Tutorial


* Conectar num banco de dados Postgres 
* ⁠fazer select , group by, where no banco
* ⁠o que é o apache spark
* ⁠como fazer consultas usando o spark 
* ⁠operações básicas usando Python , criar objeto , função , loop for , if else 
* ⁠como ler arquivo Csv usando o pandas 
* ⁠fazer as operações de filtro, seleção de colunas , e group by usando o pandas


#### Subir o postgres
````
docker compose up -d
````

##### Bancos Relacionais

postgres
mysql
oracle
mysql


#### Conectar no banco

Conectar pelo  Dbeaver no Postgres :

````
hostname: localhost
port: 5432
username: admin
password: admin
````

#### Criar a tabela

Pelo comando SQL
````
create table blabla (
COLUNA_1 varchar(10) primary key
);


CREATE TABLE tabela_2 (
    ID_COLUNA int NOT NULL PRIMARY key,
    COLUNA_1 varchar,
    FOREIGN KEY (COLUNA_1) REFERENCES blabla(COLUNA_1)
);
````


pelo point-click do Dbeaver:

tutorial -> schema -> public -> export -> seleciona o .CSV  e cria a tabela

#### Comandos SQL

##### Select ,join, group by, Where

````
SELECT country,region  FROM tutorial.public.happiness_data hd;
````

`````
SELECT *  FROM tutorial.public.happiness_data hd
where country = 'Iceland'
`````

````
SELECT "Happiness Rank",COUNT(*), sum("Happiness Rank"), avg("Happiness Rank")  FROM tutorial.public.happiness_data hd group by "Happiness Rank"
````

```
select hd_1.country,hd_1.region,hd_2."Family"  from tutorial.public.happiness_data_1 hd_1 -- ALIAS
inner join tutorial.public.happiness_data_2 hd_2  -- inner full (forma) join (direcao)(left right)
on hd_1.country = hd_2.country
```







