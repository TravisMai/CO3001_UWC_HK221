# HK221-CO3001-UWC-2.0
**Team name** QLDA\
**Task 1**  Requirement elicitation\
**Task 2**  System modelling\
**Task 3**  Architecture Design\
**Task 4**  Implementation - Sprint 1\
**Date:** November 9<sup>th</sup>, 2022 (task 4)

## Members
- Lê Tuấn Hưng (2052508)
- Mai Hữu Nghĩa (2052612)
- Trần Trí Đạt (2042443)
- Đinh Xuân Phú (2052650)
- Dương Gia An (1952163)

## Task 1
### Task 1.1
#### Context of Project
Service provider Y has hired Organization X to create the UWC 2.0 information
management system in order to increase the effectiveness of rubbish collection. Task
Management will be a part of the solution.

#### Relevent Stakeholder
-  Back Office
- Collectors and janitors
- Organization X
- Service provider Y

#### Expected jobs
- Back officer:
1. Have an overview of janitors and collectors, their work calendar
2. Have an overview of vehicles and their technical details (weight, capacity, fuel consumptions, 
etc)
3. Have an overview of all MCPs and information about their capacity. Information should be 
updated from MCPs every 15 minutes with the availability of at least 95% of their operating 
time.
4. Assign vehicles to janitors and collectors
5. Assign janitors and collectors to MCPs (task)
6. Create a route for each collector. Assigned route is optimized in term of fuel consumption 
and travel distance.
7. Be able to send message to collectors and janitors

- Collectors and janitors:
1. Have an overview of their work calendar
2. Have a detail view of their task on a daily and weekly basic. All important information should 
be displayed in one view (without scrolling down).
3. Be able to communicate with collectors, other janitors and back officers. The messages 
should be communicated in a real-time manner with delay less than 1 second.
4. Check in / check out task every day
5. Be notified about the MCPs if they are fully loaded
