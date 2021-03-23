# Fly

## Table

| name           | type           | primary key    | references                |
|:---------------|:-----------    |:-------------- |:------------------------- |
| Plane          | `integer`      | `true`         | `Plane_idPlane`           |
| Trip           | `integer`      | `true`         | `Trip_idTrip`             |
| Route          | `varchar(40)`  | `false`        | `null`                    |
| Trans_land     | `integer`      | `false`        | `Trans_land_idTrans_land` |
| Crew           | `integer`      | `false`        | `Crew_idCrew`             |


## Create table
```
CREATE  TABLE Fly (

  Plane_idPlane INT NOT NULL ,

  Trip_idTrip INT NOT NULL ,

  Route VARCHAR(45) NOT NULL ,

  Transit_landings_idTransit_landings INT NOT NULL ,

  Crew_idCrew INT NOT NULL ,

  PRIMARY KEY (Plane_idPlane, Trip_idTrip) ,

  CONSTRAINT fk_Plane_has_Trip_Plane1

    FOREIGN KEY (Plane_idPlane)

    REFERENCES Plane (idPlane)

    ON DELETE NO ACTION

    ON UPDATE NO ACTION,

  CONSTRAINT fk_Plane_has_Trip_Trip1

    FOREIGN KEY (Trip_idTrip )

    REFERENCES Trip (idTrip )

    ON DELETE NO ACTION

    ON UPDATE NO ACTION,

  CONSTRAINT fk_Fly_Transit_landings1

    FOREIGN KEY (Transit_landings_idTransit_landings)

    REFERENCES Transit_landings(idTransit_landings)

    ON DELETE NO ACTION

    ON UPDATE NO ACTION,

  CONSTRAINT fk_Fly_Crew1

    FOREIGN KEY (Crew_idCrew)

    REFERENCES Crew(idCrew)

    ON DELETE NO ACTION

    ON UPDATE NO ACTION);
```
## Commands
```
INSERT INTO  Fly VALUES (1,1,'Good',1,1), (2,2,'Bad',2,2), (3,3,'Normal',3,3);
```