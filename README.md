# Architectural Katas Fall - 2024EquiVisionaries

Here is my initial view of how the Anonymiser and the CV to Job spec Matcher integrate with the rest of the application
I think it's important to accommodate these long running processes as well as the fact that job specs and CVs are dropped in randomly and they should be processed as soon as possible making judicious use of the AI tools.
[diagram](/ideas.drawio.png)

## Members
- John Hutchison [[LinkedIn](https://www.linkedin.com/in/john-hutchison-is-awesome/)]
- Yogesh Pekhale [[LinkedIn](https://www.linkedin.com/in/yogeshpekhale/)]
- Sorin Slavescu  [[LinkedIn](https://www.linkedin.com/in/sorin-slavescu/)]
- Vaibhav Agarwal [[LinkedIn](https://www.linkedin.com/in/vaibhav-agarwal-39500914/)]

## Table of Contents 
```
1. Problem Background
  1.1 Clear view
  1.2 Functional Requirements
  1.3 Glossary 
2. Problem Analysis
  2.1 Business Goals & Business Drivers
  2.2 Engagement Model
  2.3 Other Considerations
3. Architecture Analysis
  3.1 Architecturally Significant Requirements
  3.2 Constraints and Assumptions
  3.3 Actors, Actions, and Components
  3.4 Key Architecture Characteristics
  3.5 Capacity Planning
  3.6 Data Storage Considerations
  3.7 Guiding (Architecture) Principles
  3.8 Architecture Style Selection
4. Architecture Decision Records (ADRs)
  001-
5. Solution Overview
  5.1 High-Level Architecture
  5.2 Deployment Architecture
  5.3 Employer Dashboard UI View
  5.4 Admin UI View
  5.5 Candidate UI

```
