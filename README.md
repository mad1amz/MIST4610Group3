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

The database includes Flight Crew, Employee, and Crew Role entities. Airlines employ staff members who assist on the tarmac and at the boarding gates, but also on flights themselves as the flight crew. This role, coupled with different roles that employees may hold for a specific flight (i.e., a pilot who staffs a copilot for a particular flight), staff are responsible for ground operations like managing the terminals and assisting passengers, while flight staff includes pilots, copilots, and flight attendants who work aboard the planes. Separating these two groups allows the system to distinguish between ground-based and flight-based employees, each with different roles and responsibilities.
Passengers are another core component of the model. By linking passengers to flights through ticket details, the system can track travel information, seat assignments, and flight capacity. This connection provides important insight into passenger flow and helps ensure effective boarding and scheduling for flights
There are also the airport’s Terminals which provide the physical infrastructure for operations.


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
