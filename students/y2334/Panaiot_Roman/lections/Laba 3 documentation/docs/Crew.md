# Crew

## Table
| name           | type           | primary key    | references          |
|:-------------- |:-----------    |:-------------- |:------------------- |
| idCrew         | `integer`      | `true`         | `null`              |
| Staff          | `integer`      | `false`        | `null`              |
| Member         | `integer`      | `false`        | `Member_idMember`   |

## Create table
```
CREATE  TABLE Crew (

  idCrew integer NOT NULL ,

  Staff integer NOT NULL ,

  Member_idMember integer NOT NULL ,

  PRIMARY KEY (idCrew) ,

  CONSTRAINT fk_Crew_Member1

    FOREIGN KEY (Member_idMember )

    REFERENCES Member (idMember)

    ON DELETE NO ACTION

    ON UPDATE NO ACTION);
```

## Commands
```
INSERT INTO Crew VALUES (1, 3, 1),  (2, 3, 2), (3, 3, 3);
```