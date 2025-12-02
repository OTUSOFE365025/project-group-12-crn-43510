## 1. **ATAM risk assessment table**

| **Analysing Scenario** | **P1.1** |
|--------------------|-------------|
| Scenario           | Student queries academic information during peak usage       |
| Stimulus           | Student asks "When is my next exam?" via mobile app during peak hours            |
| Environment        | Normal operation with up to 5,000 concurrent users (per RA7), external systems (LMS, Registration, Calendar) available             |
| Response           | System responds within 2 seconds (RS10) with accurate, personalized data while maintaining 99.5% availability (RS11)             |

| **Architecture Design** | **Sensitivity** | **Tradeoff** | **Risk** | **Non-risk** |
|----------------------|-------------|----------|------|----------|
|AD1 Cloud-native scalable microservices                      | S1, S3            | T3         | R1      |N1          |
| AD2 Integration layer with external systems                     | S3            | T2        |R2      | N2         |
|AD3 Multi-channel interface (mobile/web/voice)                     |             | T3         |      | N1         |




## 2. **Description of the risks, non-risks, sensitivity, and tradeoffs**

**Risks:**

* R1 - Performance Bottlenecks in the NLU Pipeline

* R2 - External LMS Failure Affecting User Experience

* R3 - Zero Trust Authorization Increases System Complexity

**Nonrisks**

* N1 - Use of Three-Tier Deployment Pattern

* N2 - Circuit Breaker for External Services

* N3 - Token-Based Caching Strategy

**Sensitivies**

* S1 - Natural Language Processing Pipeline

* S2 - Authorization Layer (Zero Trust & RBAC)

* S3 - External Integration Layer & Circuit Breakers

**Tradeoffs**

* T1 - Security vs Performance

* T2 - Freshness of Data vs Availability

* T3 - High Availability vs System Complexity

## 3. **ATAM utility tree**
<img width="810" height="515" alt="ATAM-Utility-Tree drawio" src="https://github.com/user-attachments/assets/e236e477-1b92-45c4-9ce7-88ed790817a3" />



