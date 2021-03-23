# Transit landings

## Table
| name               | type           | primary key    | references          |
|:-----------------  |:-------------- |:-------------- |:------------------- |
| idTransit_landings | `integer`      | `true`         | `null`              |
| Point_landings     | `varchar(40)`  | `false`        | `null`              |
| Date_landings      | `date`         | `false`        | `null`              |

## Create table
```
CREATE  TABLE Transit_landings (

  idTransit_landings integer NOT NULL ,

  Point_landings VARCHAR(45) NOT NULL ,

  Date_landings DATE NOT NULL ,

  PRIMARY KEY (idTransit_landings) );
``` 

## Commands
```
INSERT INTO  Transit_landings VALUES (1, 'Gibraltar', '2021-02-10'),(2, 'Stambul', '2021-03-10'), (3, 'Horizon', '2021-05-10');
```