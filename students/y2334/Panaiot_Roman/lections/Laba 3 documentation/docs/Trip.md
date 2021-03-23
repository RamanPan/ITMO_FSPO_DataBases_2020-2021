# Trip

## Table

| name           | type           | primary key    | references          |
|:-------------- |:-----------    |:-------------- |:------------------- |
| idTrip         | `integer`      | `true`         | `null`              |
| pointdeparture | `varchar(40)`  | `false`        | `null`              |
| Destination    | `varchar(40)`  | `false`        | `null`              |
| Date_departure | `date`         | `false`        | `null`              |
| Date_destin    | `date`         | `false`        | `null`              |
| Distance       | `float`        | `false`        | `null`              |
| TicketSold     | `integer`      | `false`        | `null`              |

## Create table
```
CREATE  TABLE Trip (

  idTrip integer NOT NULL ,

  pointdeparture VARCHAR(45) NOT NULL ,

  Destination VARCHAR(45) NOT NULL ,

  Date_departure date NOT NULL ,

  Date_destination date NOT NULL ,

  Distance float NOT NULL ,

  Tickets_sold integer NOT NULL ,

  PRIMARY KEY (idTrip) );

``` 

## Commands
```
INSERT INTO Trip VALUES (1, 'Moscow', 'Saint-Petersburg','2021-02-10','2021-02-11',700,300),(2, 'Moscow', 'Saint-Petersburg','2021-02-10','2021-02-11',700,300), (3, 'Moscow', 'Saint-Petersburg','2021-02-10','2021-02-11',700,300);
```