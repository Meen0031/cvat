\# Annotation Analytics Assessment — Plan



\## Starting Point

\- CVAT commit: e4e93502ac5d4c8fd25834ee9e88dd3154ff7a22

\- Branch: dev-test01

\- Development environment: Local Docker stack



\## Goal

Add annotation analytics to CVAT that counts annotations by class for a task and presents the results visually in the web interface.



\## Implementation Plan



\### 1. Environment and Codebase Exploration — \~1 hour

\- Start the CVAT Docker stack.

\- Create a superuser and verify the application runs locally.

\- Import a manageable portion of the COCO 2017 validation dataset.

\- Locate the relevant Task, Job, Label, and annotation models.

\- Identify existing CVAT authentication and task permission patterns.



\### 2. Backend API — \~2 hours

\- Create the required Django app named `test`.

\- Add an API endpoint that accepts a task and returns annotation counts grouped by class.

\- Read counts directly from the CVAT database.

\- Reuse CVAT's existing authentication and task-access mechanisms.

\- Verify counts against the test task.



\### 3. Frontend Analytics — \~2 hours

\- Add an annotation analytics page to the CVAT web interface.

\- Call the new backend endpoint.

\- Display annotation counts as a graph.

\- Handle empty-data and failed-request states cleanly.



\### 4. Measurement and Verification — \~1 hour

\- Define and measure an endpoint performance objective.

\- Run the measurement five times.

\- Save raw results and report the median and spread.

\- Record machine specifications and testing conditions.



\### 5. Additional Requirements — \~1 hour

If the core requirements are stable, attempt requirements in order:

\- Additional filter/grouping.

\- Live updates using WebSocket.

\- Connection recovery.



Advanced functionality will not be attempted if it risks the stability of requirements 1–4.



\### 6. Final Verification and Recording — \~1 hour

\- Test the implemented functionality.

\- Complete the Definition of Done with evidence.

\- Document unfinished requirements and reasons.

\- Review the final diff and Git history.

\- Record the required Loom demonstration and technical explanation.



\## Priority

Requirements 1–4 are the minimum deliverable and take priority over all advanced functionality. Authentication/authorization will be addressed after the core analytics flow is working.



\## Current Scope Decision

I will prioritize a correct database-backed API and reliable frontend visualization over WebSocket/live-update functionality. Live updates and reconnection handling will only be attempted if the core implementation, error states, authentication, and measurements are complete.





