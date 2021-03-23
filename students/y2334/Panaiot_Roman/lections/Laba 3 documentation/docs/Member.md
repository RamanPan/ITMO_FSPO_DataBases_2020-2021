# Member


## Table

| name           | type           | primary key    | references          |
|:-------------- |:-----------    |:-------------- |:------------------- |
| idMember       | `integer`      | `true`         | `null`              |
| name           | `varchar(20)`  | `false`        | `null`              |
| age            | `integer`      | `false`        | `null`              |
| role           | `varchar(20)`  | `false`        | `null`              |
| age_exp        | `integer`      | `false`        | `null`              |

## Create table
```
CREATE  TABLE Member (

  idMember integer NOT NULL ,

  Name VARCHAR(45) NOT NULL ,

  Age integer NOT NULL ,

  Role VARCHAR(45) NOT NULL ,

  Age_experience integer NOT NULL ,

  PRIMARY KEY (idMember) );
```

## Commands
```
INSERT INTO Member VALUES (1, 'Roman', 20, 'Pilot',1), (2, 'Eithne', 20, 'Pilot',2), (3, 'Aglais', 30, 'Stuard',3);
```