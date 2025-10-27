# MIST4610 Group Project 1

## Team Name: 
15058_Group3

## Team Members:
1. Aidan Combs [@acombs122](https://github.com/acombs122)
2. Joey Maitran [@Jbm39435 ](https://github.com/Jbm39435)
3. Praneet Venigalla [@pxv24](https://github.com/pxv24)
4. Cameron White [@cfw10166](https://github.com/cfw10166/MIS-4610-Group-Project-1-)
5. Mariam Zaman [@mad1amz](https://github.com/mad1amz/MIST4610Group3/blob/90084431293fd8ad8af4d262cd1ccada6a1104cf/README.md)

## Scenario Description 

Our project models an operational database for the inner managerial workings of a system that coordinates flights, passengers, luggage, routes, etc., for multiple airlines. The core entity in our model is the Flight entity, which serves as the link between routes, planes, tickets, terminals, etc. Each flight represents an instance of an aircraft journey, complete with flight crew staffing information, passenger and luggage lists, and the tickets issued for the flight. The system supports the storage and reporting of day-to-day operations data for airlines, allowing them to keep track of staffing, ticketing, and luggage management at the same time in one place. Managers can analyze flight efficiency, staff assignments, and passenger trends using SQL queries built on this data.

## Data Model 

This data model is composed of fifteen entities, spanning various points of an airline’s operations.

The data model begins with the airport, terminal, terminal_airline_assignment, and airline entities. This database can track flights for airlines at a variety of different airports. Airports can have many terminals, hence why airports have a 1:M relationship with terminals. Furthermore, since airlines can operate out of many terminals, and terminals can house flights for many different airlines, there is an associative entity (terminal_airline_assignment) that is created.

Outside of this, the data model keeps track of staffing information in the form of employee, flight crew, and crew role information. Employees can hold a variety of different positions at the airline, and can be a part of many different flight crews. There can also be many employees in the same crew role, and many flight crews that have multiple employees occupying the same role. All of this is represented in the 1:M relationships between employees and flight crew, crew role and flight crew, and crew role and employees.

The data model also keeps track of relevant passenger information in luggage, ticket, passenger, loyalty account, and loyalty tier entities. This data model links passengers to their loyalty accounts, allowing airlines to track the status of their frequent fliers quite easily. Additionally, the model links tickets, luggage, and passengers, enabling airlines to ensure that passengers receive their luggage at their final destination in association with their ticket. The model accounts for situations like passengers booking multiple tickets and bringing multiple articles of baggage on a given trip, giving this model wide applicability.

Airline operations are maintained through the route and flight entities. Airlines operate different routes, and each of these routes may have many flights that operate on it on a given day. Furthermore, a terminal can operate many flights at a given time, hence why terminals and flights have a 1:M relationship.

Overall, the various entities and attributes that the data model captures provide an overarching view of the inner workings of an airline and its day-to-day operations to support efficient and effective managers.

## Data Dictionary 
<img width="827" height="352" alt="image" src="https://github.com/user-attachments/assets/d0518b83-9d07-4671-a13b-643d2808fe0d" />
<img width="809" height="276" alt="image" src="https://github.com/user-attachments/assets/a49f2eeb-134f-4a68-8aa7-f66c9618d58c" />
<img width="817" height="309" alt="image" src="https://github.com/user-attachments/assets/c3f18748-d1b3-48e7-b71f-fc6c1326fe17" />
<img width="816" height="260" alt="image" src="https://github.com/user-attachments/assets/4838d7d6-8f5f-4d14-9f8c-f0b7becf6a89" />
<img width="826" height="505" alt="image" src="https://github.com/user-attachments/assets/d05236d4-39fa-408c-a38e-969cb23515b8" />
<img width="816" height="209" alt="image" src="https://github.com/user-attachments/assets/f7ca8d26-49a7-4527-8d1e-eadbc298291c" />
<img width="811" height="302" alt="image" src="https://github.com/user-attachments/assets/009ff155-4693-491f-a6ec-213d5534a94a" />
<img width="812" height="366" alt="image" src="https://github.com/user-attachments/assets/b324f874-62d8-4b9a-bf39-9748e913a836" />
<img width="819" height="366" alt="image" src="https://github.com/user-attachments/assets/92594016-2db6-47cb-8009-c1c9e325b971" />
<img width="819" height="375" alt="image" src="https://github.com/user-attachments/assets/339b11b0-fa81-427a-b671-b7a9f2cd39ee" />
<img width="810" height="278" alt="image" src="https://github.com/user-attachments/assets/a2d13319-25af-44b5-a388-8ef5a848b87a" />
<img width="810" height="231" alt="image" src="https://github.com/user-attachments/assets/2bbfc2ca-3590-4469-871c-78c156f67c3f" />
<img width="822" height="551" alt="image" src="https://github.com/user-attachments/assets/0f0fd3c7-e3df-42c7-8b92-ad0fc76e49a8" />
<img width="815" height="523" alt="image" src="https://github.com/user-attachments/assets/5ab9f6aa-0adf-4c15-a4f9-469fbc3ad345" />
<img width="827" height="651" alt="image" src="https://github.com/user-attachments/assets/8e44febc-5fa7-44be-bb3c-7b345102c608" />

## Queries

## Database Information
