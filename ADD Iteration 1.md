## Step 1: Review Inputs
Design Purpose: To create an application that uses AI to answer questions about the school conversationally.

Primary functionality requirements: 
* UC-1 Schedule Retrieval: A student asks about their class schedule. The system uses AI to interperet their question, recieve the data, and respond with relevant information.
* UC-2 Announcement Posting: A lecturer uses a conversational command to post an announcement. The system checks for authorization, then posts it.
* UC-3 Dashboard Monitoring: An administrator monitors system usage through the dashboard, showing things like health, latency, and errors.
* UC-6 Request Lecture Materials: A student asks the assistant for lecture slides. The system checks the lecturer has shared the files, retrieves them, and provides the link to the student.
  
The prioritized quality attribute scenarios:
| Scenario ID  | Attribute | Importance to Customer | Difficulty of Implementation |
| ------------ | --------- | ---------------------- | ---------------------------- |
| QA-1 | Performance: 2 second response time | High | High |
| QA-4 | Security: Specific authorization | High | High |
| QA-3 | Availability: 99.5% uptime | High | Medium |
| QA-2 | Scalability: 5000 concurrent users | Medium | Medium |
| QA-5 | Reliability: LMS data retrieval | Medium | Low |

QA-1, QA-4, QA-3, and QA-2 are selected as drivers for Iteration 1.

Constraints:
* CON-1: Establishing secure integration with university systems.
* CON-2: Ensuring accurate access to academic data.
* CON-3: Defining clear roles and permissions within the system.

Concerns:
* CRN-1: Ensuring that the user data is stored securely.
* CRN-2: Maintaining accurate and reliable data sources.
* CRN-3: Ensuring system availability and responsiveness.

## Step 2: Establish iteration goal
Iteration 1 Goal: Establish an overall system structure

Certain concerns to keep in mind:
* QA-1 Performance: 2 second response time
* QA-4 Security: Specific authorization
* QA-3 Availability: 99.5% uptime
* QA-2 Scalability: 5000 concurrent users
* CON-1: Establishing secure integration with university systems.
* CON-3: Defining clear roles and permissions within the system.
* CRN-3: Ensuring system availability and responsiveness.

## Step 3: Select elements to refine
We want to refine the entire AIDAP system.

## Step 4: Choosing design concepts

## Step 5: Instantiating architectural elements, allocating responsibilities and defining interfaces

## Step 6: Sketch views and record design decisions

## Step 7: Perform analysis of the current design and review the iteration goal and design objectives
