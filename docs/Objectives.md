\# Objectives



\## MO-1 — Annotation Analytics API Response Time



\*\*What is measured:\*\*  

Response time of the annotation-count API for a populated CVAT task.



\*\*How:\*\*  

Send the same authenticated request to the analytics endpoint five times against the local Docker environment and record the response time of each request.



\*\*Target:\*\*  

Median response time of the five runs should be at or below 500 ms.



\*\*Conditions:\*\*  

\- Local CVAT Docker stack

\- Same populated test task for all five runs

\- No intentional concurrent workload

\- Same machine and network conditions



\*\*Not included:\*\*  

\- Docker/container startup time

\- Dataset import time

\- First request immediately after a cold start



\## Environment



\- CVAT starting commit: `e4e93502ac5d4c8fd25834ee9e88dd3154ff7a22`

\- Operating System: Windows

\- CVAT running locally using Docker



CPU and RAM specifications will be recorded before measurement.



\## Results



To be completed after implementation.



| Run | Response Time |

|---|---:|

| 1 | |

| 2 | |

| 3 | |

| 4 | |

| 5 | |



\*\*Median:\*\* Pending  

\*\*Spread (min–max):\*\* Pending  

\*\*Target result:\*\* Pending

