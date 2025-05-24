# pre plan
Write the scenario for the whole system, how it operates and how it triggers

# making the plan
1. extract the triggers from the scenario
2. design a system that can handle the triggers
3. isolate components and write detailed description


# Scenario 
1. The temperature sensor from the incubation or fruiting room will update the current temperature frequently
2. The server will check the temperature and trigger the hvac system to heat up the room
3. The server will keep track of the fan run time to make sure the air in the room is new
4. The server will always store sensor data into the database for future R&D.


* The temperature sensor will send an XX value to the server, the server will check if the value is in range (22-25 incubation, 16-18 fruiting), if not the HAVC function should kick off until we get new sensor values that the temperature is in range
* The HVAC function is still unknown at the moment as it has many variables that are not defined yet
* An internal timer will determine if the room air needs to be renewed, it will also take into account the outdoor temperature and pre condition the heat exchangers to meet the required value.

# Triggers
1. Room temperature sensor
2. Internal timer for fan uptime

# The system
A web server will have some end points for all the sensors in the system and it will be responsible as a control unit as well as logging

# Components
1. Incubation room temperature sensor
2. Fruiting room temperature sensor
3. Outdoor temperature sensor
4. boiler Water temperature sensor
5. Incubation room heat exchanger output water temperature sensor
6. Incubation room heat exchanger output air temperature sensor
7. Incubation room heat exchanger water electro valve
8. Fruiting room heat exchanger output water temperature sensor
9. Fruiting room heat exchanger output air temperature sensor
10. Fruiting room heat exchanger water electro valve

# The Server
1. Endpoints
2. Database
3. control logic