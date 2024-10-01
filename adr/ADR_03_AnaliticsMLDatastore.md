# ADR_03_AnaliticsMLDatastore
## Problem Statement
Data Aggregation Service Datastore will need to be designed in line with current and future needs for reproting and ML improvements.

## Context
Data points (see req doc) need to be collected and made available for analytics and ML processes to improve Matching, anonymisation, SMART story generation, resume tips

The solution could be a distributed one, following the Data Mesh approach where each service exposes Data Products that can be consumed by other parts of the system including the Reporting and Analytics platform or the other ML systems in use. The other approach is the traditional centralised location for OLAP to be provided by a Datalake or a Data Warehouse.

## Discussin points
Best data structures at rest to collect this data from Event broker, Resume and Job services, surveys, etc.
We've discussed the ideas of Event Storming, Data Mesh, Datalakes, Data Warehouses as options for gathering and storing data for this future processing

## Decision
Given the complexity of the AI systems especially on how data collected will affect the ML process for understanding similarities between job descriptions and resumes as well as improved ways for anonymisation we have decided to postpone on elaborating on this datastore to a further stage.