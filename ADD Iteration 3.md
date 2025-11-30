## Step 2: Establish iteration goal
For this iteration we will focus on the QA-3 scenario:
When anybody accesses the system at any time, it should be available at least 99.5% of the time every month, including peak periods.

## Step 3: Select elements to refine
To support this scenario, we will refine the components that affect runtime identified during the first two iterations: 
* API Gateway
* Authentication  Service
* Conversational Engine

## Step 4: Choosing design concepts
| Design Decisions and Location | Rationale |
| ------------ | --------- |
| Introduce the active redundancy tactic for the AI | The system continues to run if one instance fails helping with the availability goal.|
| Introduce a load balancer in front of backend | Distributes user requests evenly and reroutes when the system fails. |
| Introduce a message queue between API Gateway and backend | Prevents loss of user's questions to the chatbot during any outages. |

## Step 5: Instantiating architectural elements, allocating responsibilities and defining interfaces
| Design Decisions and Location | Rationale |
| ------------ | --------- |
|Deploy dedicated load balancer node | Gives failure protection and sends user requests to available services.|
| Share AI data across multiple instances| Ensures constant AI processing during system failures.|
| Deplay a persistent message queue | Ensures user queries are not lost during outages.|

## Step 6: Sketch views and record design decisions

## Step 7: Perform analysis of the current design and review the iteration goal and design objectives
| Not Addressed  | Partially Addressed | Completely Addressed | Design Decisions Made During the Iteration |
| -------------- | ------------------- | -------------------- | ------------------------------------------ |
| | | |
