#AirCarrier

## Table

| name           | type           | primary key    | references          |
|:-------------- |:-----------    |:-------------- |:------------------- |
| idAirCarrier   | `integer`      | `true`         | `null`              |
| name           | `varchar(20)`  | `false`        | `null`              |
| workers        | `integer`      | `false`        | `null`              |

## Create table

```
  CREATE  TABLE AirCarrier (

  idAirCarrier integer NOT NULL PRIMARY KEY ,

  name text NOT NULL ,

  workers integer NOT NULL

  );
``` 

## Commands
```
INSERT INTO AirCarrier VALUES (1, 'Aeroflot', 250), (2, 'EmiratesAer', 500), (3, 'JangoAer',200);
```