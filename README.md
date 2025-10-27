# MIST4610 Group Project 1

## Team Name: 
15058_Group3

## Team Members:
1. Aidan Combs [@acombs122](https://github.com/acombs122)
2. Joey Maitran [@Jbm39435 ](https://github.com/Jbm39435)
3. Praneet Venigalla [@pxv24](https://github.com/pxv24)
4. Cameron White 
5. Mariam Zaman [@mad1amz](https://github.com/mad1amz/MIST4610Group3/blob/90084431293fd8ad8af4d262cd1ccada6a1104cf/README.md)

## Scenario Description 

_**A description of the scenario that you are modeling describing it in sufficient detail that makes
sense in the context of your data model**_

Our project models an operational database for the inner managerial workings of a major airport that coordinates airlines, flights, passengers, aircrafts, etc. The system supports storage of data and reporting for day to day operations. 
The core entity in our model is the Flight entity, which serves as the link between airlines, planes, terminals, gates, etc. Each flight represents an instance of an aircraft journey, complete with departure and arrival information, gate assignments, and the airline responsible for operating the flight.

The database also incorporates includes Airport Staff and Flight Staff entities. Airport staff are responsible for ground operations like managing the terminals and assisting passengers while flight staff includes pilots, copilots, and flight attendants who work abroad the planes. Separating these two groups allows the system to distinguish between ground-based and flight-based employees, each with different roles and responsibilities.

Passengers are another core component of the model. By linking passengers to flights through reservations and ticket details, the system can track travel information, seat assignments, and flight capacity. This connection provides important insight into passenger flow and helps ensure effective boarding and scheduling for flights

There are also the airport’s Terminals and Gates which provide the physical infrastructure for operations. Each terminal contains multiple gates, which are assigned to flights based on their timing and airline. 




## Data Model 

_**explanation of the data model including the
relationships between the entities in natural English. Simply put, what kind of data does your
database support storage of and what kind of data does it not?**_

## Data Dictionary 
<img width="827" height="352" alt="image" src="https://github.com/user-attachments/assets/d0518b83-9d07-4671-a13b-643d2808fe0d" />


## Queries

## Database Information
