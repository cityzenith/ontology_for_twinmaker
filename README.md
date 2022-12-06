# ontology_for_twinmaker
Created ontology in N-Triples format.


Created ontology using reference of brick schema ontology doc(https://brickschema.org/ontology).

N-Triple file format (Table) which has Subject-Predicate-object columns.

Ontology name:
 1) Building profile ontology 
 2) sensor model ontology 
 3) spatial model ontology
 4) Site selection ontology
 5) Project ontology

Uploaded N-Triple file into PostgreSQL.

- PostgreSQL database name - TUEng1masterData
- Postgres credential - "psql -h simdata-postgresql.cycxcfqezmhb.us-east-2.rds.amazonaws.com -p 5432 -U user_abc -d threedvis pw - user_abc "

1) Building profile ontology:

Graph location: https://lucid.app/lucidchart/2fbef159-6a25-4c59-827b-3d2b021da306/edit?page=LYTU0jIMkOXf#
it has building metadata.

see the below table for the reference:

|  Component_type   |       Entities      |
|  :-----------:    |     :----------:    |
| bf_hasLocation    |	    virtualSite   |
|	            |       Floor1        |
|	            |       Zone111       |
|	            |       HVAC11        |
|	            |       numberOfFloors|
|	            |       ZipCode       |
| bf_hasDesign	    |       documentation |
|	            |       Model         |
| bf_entityProperty |	    BuiltArea     |
|	            |       Org11         |
|	            |       Experience    |
|	            |       Name          |
|	            |       Email         |
|	            |       FloorArea     |
| bf_designedBy	    |       Architect11   |
| bf_hasAddress	    |       Address       |
| latitude	    |       latitude      |
| longitude	    |       longitude     |
| bf_YearBuiltShape | 	    yearBuilt     |


2) sensor model ontology:

Graph Location: https://lucid.app/lucidchart/d34880d2-2ed8-473e-bd19-793b62066b6d/edit?page=0_0&invitationId=inv_ac226f4d-5251-446d-a87c-b8bea0f0faaf#

| Component	  |         Entities                   |
| :----------:    |        :-----------:               |
| rdf_Type	  |         rec:Building               |
|	          |         rec:level                  |
|	          |         rec:Room                   |
|	          |         brick:Temperature_Sensor   |
|	          |         brick:Temperature_Setpoint   |
|	          |            |
| rec_hasPart	  |         Floor numbers              |
|	          |         Room Numbers	       |
| brick_hasPoint  |         Sensor location            |
| brick_value	  |         Sensor readings            |
| brick_timestamp |         Timestamp                  |

3) spatial model ontology:

Graph location: https://lucid.app/lucidchart/80a44139-5d52-4625-9b04-fd8acc5d3c27/edit?beaconFlowId=71E8A65DC25AC6E2&invitationId=inv_46dca2eb-7ba9-4e11-b8dc-e632fbd2492b&page=0_0#

|  Component	  |         Entities       |
| :---------:     |      :-----------:     |
|  rdf_Type	  |        rec:Building    |
|	          |        rec:level       |
|	          |        rec:Room        |
|  rec_hasPart	  |        Floor Numbers   |
|	          |        Room Numbers    |
|  rec_geometry	  |    Latitude, Longitude |

4) Site selection ontology:

Graph location: https://lucid.app/lucidchart/c8ff8c59-5153-47c5-8e07-e4285f8b0611/edit?beaconFlowId=10ACD616B69157E3&invitationId=inv_7553feda-f3c8-4472-b7d6-89452f11f826&page=0_0#

| Component	      |        Entities  |
  :-------------:     |   :---------------:
| hasLocation         |        WorldMap  |
|	              |        Country   |
|	              |        State     |
|	              |        CityName  |
|	              |        ZipCode   |
| isLocationOf    |        Country   |
|	              |        State     |
|	              |        CityName  |
|	              |        ZipCode   |
|	              |       Building11 |
|	              |        Site      |
|	              |       Parcel/Plot|
| hasAdress	      |        Address   |
|	              |        WorldMap  |
|	              |        Country   |
|	              |        State     |
|	              |        CityName  |
|	              |        ZipCode   |
| latitude	      |        Latitude  |
| longitude	      |        Longitude |
| createdAround	      |        Reference/|
|                     | adjucent building|
| entityProperty      |        BuiltArea |

5) Project ontology:
Graph location: https://lucid.app/lucidchart/1c33a06f-de1e-4b4e-b182-0577e00c4a4e/edit?beaconFlowId=1191006138CDC38E&invitationId=inv_a35e4061-89ac-4346-a3cd-0406e2fa1a43&page=0_0#

|  Component	     |     Entities                  |
| :---------:        |    :-----------:              |
| bf_hasLocation     |    Workspace main(0)          |
|	             |    Location                   |
|	             |    Neighborhood assets        |	     
| bf_isLocationOf    |	  Workspace (1) (2)…         |
| timeseries	     |    mm-dd-yyy tt:ss            |
| isMeasuredBy	     |    Distance (contextual data) |
|	             |    Shadow (Contextual data)   |
