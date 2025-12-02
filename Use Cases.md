| Use Case  | Description | Associated Requirement ID |
| --------- | ----------  | ------------------------- |
| UC-1:     | A student interacts with the system to ask about their class schedule. The system uses AI to interpret natural language queries, receives the data and responds with relevant information using both stored knowledge and live data. | R1, R3, R5, R6, RS1 |
| UC-2:     | A lecturer uses a conversational command to post an announcement. The system checks that the lecturer is authorized, and then sends the announcement to the students in that class. | R5, RL2, RL8 |
| UC-3:     | An administrator monitors system usage through the dashboard, which shows things like health, latency, and errors. The system collects this data from its logged metrics. | RA4, RM2, RM4 |
| UC-4:     | A lecturer queries the assistant for summarized class analytics such as average attendance or grades. The system checks the lecturer for authorization, receives the corresponding data, and then displays it | RL3, RL6, R3, R5, R6 |
| UC-5:     | The system maintainer is prompted to update the current system; this update is to be deployed with zero downtime using continuous pipelines, while creating a secure backup and restore of user and configuration data | RM1, RM3, RM6, R6, R7 |
| UC-6:     | A student asks the assistant for lecture slides or reading materials. The system checks that the lecturer has shared the files, retrieves them from the connected LMS, and provides the download or access link to the student. | R1, R3, R6, RS7, RS8, RL1|

Use Case Diagram:

<img width="494" height="382" alt="Phase1UseCaseDiagram drawio" src="https://github.com/user-attachments/assets/75548235-e10e-4afa-b4b4-9b5ecd15b67d" />
