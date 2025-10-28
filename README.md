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

Each terminal connects to the route entity, which shows the path between an origin and destination airport along with the distance of that route. The Flights table records every scheduled flight, including its time, date, and the specific route, terminal, and plane used for that trip. Because one route can have many flights over time, this creates a one-to-many relationship between Route and Flights. 

The plane entity represents the aircraft used by the airline. Each plane has details such as the number of seats and airplane type and is linked to an airline through a one-to-many relationship because each airline owns multiple planes. The airline entity itself stores the name of the airline company, and the terminal_airline_association table connects airlines to the terminals they operate in.

Outside of this, the data model keeps track of staffing information in the form of employee, flight crew, and crew role information. Each employee belongs to an airline, forming a one-to-many relationship between Airline and Employee. Employees can hold a variety of different positions at the airline, and can be a part of many different flight crews. Employees also have assigned crew roles, represented by the crew role table. There can be many employees in the same crew role, and many flight crews that have multiple employees occupying the same role. The associative entity flight crew connects employees, crew roles, and specific flights, showing which employees serve on which flights and in what roles.

On the customer side, passengers represent travelers who can purchase multiple tickets, forming a one-to-many relationship between Passenger and Ticket. This table keeps track of relevant passenger information in luggage, ticket, passenger, loyalty account, and loyalty tier entities. Each ticket is tied to a specific flight, meaning one flight can have many tickets sold. This data model also links passengers to their loyalty accounts, allowing airlines to track the status of their frequent fliers quite easily. Additionally, the model links tickets, luggage, and passengers, enabling airlines to ensure that passengers receive their luggage at their final destination in association with their ticket. The luggage table records baggage information for each ticket, showing that a single ticket can have multiple pieces of luggage. The model accounts for situations like passengers booking multiple tickets and bringing multiple articles of baggage on a trip.

Also, to encourage customer loyalty, the model includes a loyalty account entity that stores membership details such as points, enrollment date, and tier level. Each loyalty account is connected to one passenger and one loyalty tier, which defines the name and ranking of the membership levels.

Overall, the various entities and attributes that the data model captures provide an overarching view of the inner workings of an airline. THis model allows for efficient management of day-to-day operations, customer service, and performance tracking across all aspects of the airline’s business.

<img width="1144" height="781" alt="image" src="https://github.com/user-attachments/assets/7017d5f4-7523-485a-ae1b-13090d34e74c" />

## Data Dictionary 

Airports
<img width="820" height="348" alt="image" src="https://github.com/user-attachments/assets/19053db0-99f9-4ec1-a529-d01e21b658af" />

Terminal
<img width="813" height="273" alt="image" src="https://github.com/user-attachments/assets/9b68cdaa-8fb0-4f01-baa8-1c6064399cb8" />

Terminal Airline Assignment
<img width="814" height="366" alt="image" src="https://github.com/user-attachments/assets/a7ed0031-bef1-4dfa-a982-598401ce1e96" />

Airline
<img width="809" height="245" alt="image" src="https://github.com/user-attachments/assets/b9934eed-c1c8-47f2-897a-f2c8df492458" />

Employee
<img width="817" height="576" alt="image" src="https://github.com/user-attachments/assets/b7e87466-441c-4af9-bbdc-2b301d78baa3" />

Crew Role 
<img width="811" height="204" alt="image" src="https://github.com/user-attachments/assets/91c62202-3d7a-4159-a8dd-a8e5ed7fed5e" />

Flight Crew
<img width="813" height="322" alt="image" src="https://github.com/user-attachments/assets/72fa4509-ab46-42fc-b38f-c01c0ac91476" />

Plane 
<img width="811" height="367" alt="image" src="https://github.com/user-attachments/assets/c507df04-6f17-4182-894e-e00ae4f37cb2" />

Route 
<img width="809" height="359" alt="image" src="https://github.com/user-attachments/assets/229da65c-ff70-40db-a9a2-681673fb3d43" />

Luggage 
<img width="807" height="376" alt="image" src="https://github.com/user-attachments/assets/48b448c2-aaca-47a4-bfcb-1e480501649d" />

Passenger
<img width="811" height="267" alt="image" src="https://github.com/user-attachments/assets/22a3d4d7-5dbe-4b4b-b3e4-f19d4e0d5fa9" />

Loyalty Tier
<img width="811" height="224" alt="image" src="https://github.com/user-attachments/assets/fc965363-a420-4d52-ac69-4804c77e2a00" />

Loyalty Account
<img width="813" height="547" alt="image" src="https://github.com/user-attachments/assets/2219b95a-b734-4f83-abab-6206325a9cd4" />

Tickets
<img width="813" height="517" alt="image" src="https://github.com/user-attachments/assets/6a80155d-4afa-4a11-ab20-93bdd0b34b81" />

Flight
<img width="814" height="692" alt="image" src="https://github.com/user-attachments/assets/d43fa693-9e5e-46f2-8bfd-2cd4cb1a897c" />


## Queries

- Query 1: 
<img width="397" height="455" alt="image" src="https://github.com/user-attachments/assets/1b064f55-1a90-40ed-9147-9408090c433b" />

Query 1 lists out all possible roles for an employee and calculates the average salary for each respective role. 
This query will provide airlines necessary data in order to manage salary and uphold industry standards. The average salary for an employee role at an airline could be compared to the national average to see where a company stands financially. This data could also be compared to other years in order to identify trends in payments. This could also help with budgeting and managing expenses. 

- Query 2: 
<img width="559" height="415" alt="image" src="https://github.com/user-attachments/assets/30590df5-f851-4117-9ba3-67e3d0fc0068" />

Query 2 lists out how many pilots and copilots are employed by each airline company. 
This query provides valuable data about an airline’s staff and will help them make certain staffing decisions. Pilots and copilots are essential in flight operations and need to be balanced for the size of an airline. Understaffing will limit how many flights a company can operate, which would lead to a loss in revenue, while overstaffing would lead to unnecessary costs, especially with high-salary employees like pilots and copilots. An airline company needs to avoid both of these issues. 

- Query 3:
<img width="683" height="707" alt="image" src="https://github.com/user-attachments/assets/906a84a6-a228-48a1-83d6-0c4ad42f00be" />

Query 3 outputs the number of passengers that boarded a flight with no luggage. 
This is important for airlines to know, as it gives data on travel habits and preferences. It will also allow companies to manage cabin space and baggage handling and fees. 


- Query 4:
<img width="414" height="705" alt="image" src="https://github.com/user-attachments/assets/bd673c30-b439-4680-989d-7887df020d7a" />

Query 4 lists all of the staff working for a specific airline and their role in the organization.  
The role of all staff members and their roles are key to organizational efficiency. This will help operations run smoothly when employees have a dedicated role. This query gives an overview of how big an airline's staff is and how many people they have in each role/department. This information can be used for staffing purposes, which helps every aspect of the company.

- Query 5: 
<img width="833" height="709" alt="image" src="https://github.com/user-attachments/assets/6c8ce411-1db1-4a1d-a749-a28272b49536" />

Query 5 outputs the name of the airline, and the percentage of how full a flight is. 
Aircrafts only have a certain amount of seats and have a max capacity, and this data allows airlines to see how full a flight is in order to manage that. Knowing the occupancy rate is important for managers to know and understand to implement efficiency measures. This data gives insight on flight demand, seat pricing, scheduling, and more. If a flight is over 100%, then it is overbooked. This would mean there are errors with an airline's operations and they need to be more efficient. 

- Query 6:
<img width="437" height="514" alt="image" src="https://github.com/user-attachments/assets/737862f0-58bb-4824-8f68-ebab1ace8cc6" />


- Query 7:
<img width="606" height="555" alt="image" src="https://github.com/user-attachments/assets/84f5ca95-e740-4088-a2bc-5fc536f2f409" />


- Query 8: 
<img width="670" height="543" alt="image" src="https://github.com/user-attachments/assets/f3416bce-5cf5-41b8-852c-8c223f58d4de" />

Query 8 outputs the flight crew that has the most combined salary. This flight crew is made up of several employees. 
Airline companies need to know which employee teams have the highest salary in order to manage budget and payroll. High-salary teams may be more experienced, and could be put on longer/harder flights. This could also be used for training decisions, where an experienced, highly-paid team could teach others. 

- Query 9:
<img width="794" height="698" alt="image" src="https://github.com/user-attachments/assets/3de3d41f-e7a4-4796-abfe-224aa89bfc67" />

Query 9 lists out all of the customers in the Platinum tier that have more than the average amount of points in that tier. 
Loyalty rewards programs are a great way for customer retention and acquisition. This information will be valuable for the marketing department of an airline. This data can test the effectiveness of the loyalty program as a whole. Airlines can also use this data for targeted discounts and ads and identify their most loyal customers. 

- Query 10:
<img width="510" height="541" alt="image" src="https://github.com/user-attachments/assets/df027c46-b9bd-43d3-b6f5-c4c246b98841" />

Query 10 outputs the name of the terminal that has had the most ticket sales of all time. 
This query will help airline companies identify the busiest terminals at an airport. With this data, companies will be able to identify the busiest terminals and use resources accordingly. Extra staff may be placed and busy terminals and foot traffic control will be considered. 

## Database Information

Name of the database: ns_F25MIST4610_15058_Group3

