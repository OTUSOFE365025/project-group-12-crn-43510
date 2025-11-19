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
| | |
| | |
| | |
| | |

## Step 6: Sketch views and record design decisions

## Step 7: Perform analysis of the current design and review the iteration goal and design objectives
| Not Addressed  | Partially Addressed | Completely Addressed | Design Decisions Made During the Iteration |
| -------------- | ------------------- | -------------------- | ------------------------------------------ |
|  |  | | |
|  |  | | |
|  |  | | |
|  |  | | |
|  |  | | |
|  |  | | |
|  |  | | |
|  |  | | |
|  |  | | |
|  |  | | |
|  |  | | |
