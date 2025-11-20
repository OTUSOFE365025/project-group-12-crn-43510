## Step 2: Establish iteration goal
Iteration 2 Goal: Refine the internal subsystems and improve performance, security, and reliability

Certain concerns to keep in mind: 
* QA-1 Performance: Improve response path
* QA-4 Security: Improve user authorization implementation
* QA-5 Reliability: Improve reliability when the external LMS fails
* QA-3 Availability: Improve the system to maintain an uptime of 99.5%
* CON-2: Ensuring accurate and real-time access to academic data for students and lecturers
* CON-3: Defining  roles and permissions for students, lecturers, and administrators
* CRN-2: Maintaining accurate and reliable data sources and ensuring precise responses
* CRN-3: Ensuring system availability and responsiveness to ensure reliable and timely responses 

## Step 3: Select elements to refine

We want to refine the subsystems that are related to performance, security, and reliability

## Step 4: Choosing design concepts
| Design Decisions and Location | Rationale |
| ------------ | --------- |
| Implement Piles and Filters | This turns the natural language interpreter into smaller, faster stages to improve performance (QA-1) |
| Implement Zero Trust Authorization | Makes it so every request is put through authentication and authorization before reaching the backend server (QA-4, CON-3) |
| Implement Circuit Breaker | Prevents cascading errors when external services become slow or unavailable (QA-5)  |
| Implement a Token-Based Caching Strategy | Helps maintain a 99.5% availability (QA-3) |
| Implement Data Transfer Objects | Ensures a safe, consistent, and structured data flow, limiting errors (CRN-2) |

## Step 5: Instantiating architectural elements, allocating responsibilities and defining interfaces
| Design Decisions and Location | Rationale |
| ------------ | --------- |
|Instantiate the NLU Pipes-and-Filters pipeline inside the Conversational Engine |Breaks the NLU into small processing stages, improving response speed (QA-1) and making responsibilities clearer without fully completing the model this iteration. |
|Introduce an API Gateway + Auth Service enforcing Zero Trust |Ensures all requests pass authentication and permission checks, supporting system security and role enforcement (QA-4, CON-3).|
|Create External Service Adapters with Circuit Breakers for LMS, email, and registration systems |Isolates failures in external systems and prevents cascading errors, improving reliability when services like the LMS fail (QA-5). |
|Instantiate a CacheManager using token-based caching between Orchestrator and Data Sources |Reduces repeated external calls to maintain availability and improve performance (QA-3, QA-1). |

## Step 6: Sketch views and record design decisions

## Step 7: Perform analysis of the current design and review the iteration goal and design objectives
| Not Addressed  | Partially Addressed | Completely Addressed | Design Decisions Made During the Iteration |
| -------------- | ------------------- | -------------------- | ------------------------------------------ |
|  |QA-1 Performance  | |Pipes-and-Filters NLU pipeline created to speed up response time, but deeper optimization is still needed. |
|  |QA-4 Security | |Zero Trust layer added (API Gateway + Auth Service), but complete RBAC policies are not yet implemented. |
|  |  |QA-5 Reliability |Circuit Breakers in External Service Adapters fully address LMS failure handling and prevent cascading errors. |
|  |QA-3 Availability  | |Token-based caching improves uptime and reduces external dependency load, but redundancy/failover still required. |
|  |CON-2 Real-time Academic Data  | |Authorization framework enforces roles, but fine-grained permission rules still need refinement. |
|  | CRN-2 Accurate & Reliable Data Sources | |DTO standardization + resilient adapters improve accuracy, but stronger validation will come later. |
|  |CRN-3 System Responsiveness & Timely Responses  | |Caching + NLU filters increase responsiveness, but larger-scale performance tuning is upcoming. |
|  |UC-1 General Queries  | |Faster pipeline improves handling of frequent student queries. |
|  |UC-2 Course Information Requests | |DTOs + External Adapters improve accuracy but rely on external system speed. |
|  | UC-5 Calendar/Timetable Requests | |Caching reduces load, but real-time updates not fully addressed. |
|  | UC-7 Authentication & Authorization | |Zero Trust Gateway addressed core auth flows but not advanced auth scenarios. |
