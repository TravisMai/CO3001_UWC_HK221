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
- Trần Trí Đạt (2052443)
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
- Back officer
1. Have an overview of janitors and collectors, their work calendar
2. Have an overview of vehicles and their technical details (weight, capacity, fuel consumptions, etc)
3. Have an overview of all MCPs and information about their capacity. Information should be updated from MCPs every 15 minutes with the availability of at least 95% of their operating time.
4. Assign vehicles to janitors and collectors
5. Assign janitors and collectors to MCPs (task)
6. Create a route for each collector. Assigned route is optimized in term of fuel consumption and travel distance.\
7. Be able to send message to collectors and janitors

- Collectors and janitors:
1. Have an overview of their work calendar
2. Have a detail view of their task on a daily and weekly basic. All important information should  be displayed in one view (without scrolling down).
3. Be able to communicate with collectors, other janitors and back officers. The messages should be communicated in a real-time manner with delay less than 1 second.\
4. Check in / check out task every day
5. Be notified about the MCPs if they are fully loaded.


### Task 1.2
#### Functional Requirement
1. Back officers
- View calendar
- View detailed information and manage the vehicle
- Get information about the MCPs
- Assign vehicles to collectors and janitors
- Assign collectors and janitors to MCPs
- Create route for each collectors
- Communicate with collectors and janitors
2. Collector and Janitors
- Check in and check out
- View calendar
- View tasks (daily, weekly)
- Get information about the MCPs
- Communicate with other collectors, other janitors and back officers

#### Non-Functional Requirement
1. Usability requirement
- Janitors and collectors can easily use basic functions immediately
- The back officers can use after 15 minutes training.
- Interfaces in Vietnamese, with an opportunity to switch to English.
2. Performance requirement
- The system must respond in less than 30 seconds. After 30 seconds, the system will notify the user.
- Can handle real-time data.
- Allow at least 100 users access at the same time without crashing.
- The task’s status has to be updated in 5 seconds when the janitors or collectors update it.
- MCPs information must be updated every 15 minutes.
3. Space requirement
- The system can handle 500 concurrent visits without any effect on the system efficiency.
- The system should be able to handle data from at least 1000 MCPs at the
moment and 10.000 MCPs in five years.
4. Availability requirement
- Working time of the system all days of the week, from 4am to 12pm.
- The system should not be down more than 10 minutes continuously, maximum 30 minutes a day.
5. Environmental requirement
- The system runs on internet browsing.
6. Security requirement
- Password require when login
- Encryption ensure with MD5
- Ensure not leak user information
7. Operational requirements
- System data is backed up every month to prevent data loss

#### Use-case diagram for the whole system
![](/Picture/Task%201.2.png?raw=true)

| Use Name             | Use Case: Task Assignment     | 
| ---                  | ---                       |
| **Created By**       | QLDA Team                 |
| **Date Created**     | Sep 18, 2022              |
| **Primary Actor**    | Back Officer              |
| **Description**      | Assign task for janitors and collectors |
| **Trigger**          | Click the button “Assign Task”          |
| **Preconditions**    | PRE-1. System available <br> PRE-2. Device connects to the Internet|
| **Postconditions**   | POST-1.Successfully assigned the janitor or collectors. <br> POST-2. Notify the task to the worker <br> POST-3. Record the task to the   |
| **Normal Flow**      |  1. Back officer chooses the assignee. <br> 2. The system checks the availability of the assignee.<br> 3. Back officer choose day of work. <br>4. The system displays the info of all vehicles. <br> 5. Back officer chooses the vehicle for the assignee. <br> 6. Back officer chooses the MCPs. <br> 7. Back officer determines routes for the assignee. <br> 8. The system checks the availability of the routes. <br> 9. Send the notification to the assigned worker.|
| **Alternative Flow** | - End users first triggers the flow by adding any meal to their cart <br> - They can either add more food or drink to the cart or choose to view cart <br> -  After viewing the cart, the users can proceed to checkout <br> - If **delivery** option is picked, the users must provide delivery information before payment <br> - When done, the users are sent directly to the purchasing site, where they can choose payment method and enter the banking information <br> - The 3rd party bank issuer is involved to handle the transaction at this point <br> - Upon successful payment, users are encouraged to give feedback on their ordering experience <br> - If any feedback is given, it will be recored by the system <br> - In the mean time, clerks verify the purchased order by confirming it or canceling it <br> - If order is plausible, it will be recorded by the system; otherwise, a refund is processed |
| **Exceptions**       | The system is down <br> Order is placed in non-working hours <br> Number of orders per day exceeds 300         |
