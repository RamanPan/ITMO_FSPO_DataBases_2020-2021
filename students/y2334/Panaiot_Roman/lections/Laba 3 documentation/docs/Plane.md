# Plane

## Table
| name           | type           | primary key    | references               |
|:-------------- |:-----------    |:-------------- |:-------------------------|
| idPlane        | `integer`      | `true`         | `null`                   |
| Stamp          | `varchar(20)`  | `false`        | `null`                   |
| Places         | `integer`      | `false`        | `null`                   |
| Type           | `varchar(20)`  | `false`        | `null`                   |
| Speed          | `float`        | `false`        | `null`                   |
| AirCarrier     | `integer`      | `false`        | `AirCarrier_idAirCarrier`|

## Create table
```
CREATE  TABLE Plane (

  idPlane integer NOT NULL PRIMARY KEY,

  Stamp VARCHAR(10) NOT NULL ,

  Places integer NOT NULL ,

  Type VARCHAR(45) NOT NULL ,

  Speed FLOAT NOT NULL ,

  AirCarrier_idAirCarrier INT NOT NULL ,

  CONSTRAINT fk_Plane_AirCarrier1

    FOREIGN KEY (AirCarrier_idAirCarrier )

    REFERENCES AirCarrier (idAirCarrier) );
```  

## Commands
```
INSERT INTO Plane VALUES (1,'Mark1',250,'Big',235,1), (2,'Mark3',350,'Big',335,2), (3,'Mark3',150,'Medium',235,3);
```