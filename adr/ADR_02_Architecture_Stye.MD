Problem: Define an Inital Archtechtural Style

Context:  Defining an architectural style before development begins will allow a framework to help inform future decisions

Discussion: The requirements for this software mean that certain tasks (e.g. smart story creation, resume decontruction)
will take a significant time to complete. If implemented in a synchronous fashion user experience would be significantly degraded, 
bringing the system into conflict with the stakeholders stated goal of an easy to use system.  Additionally, it is likely that the AI and 
Machine learning aspects of the software will evolve and significantly change over time and would benefit from an architectural style that 
is well-suited to evolvibility. Being able to abtract AI into bounded services seems likely to support the system's ability to evolve as well. Also, certain aspects of the system (such as the AI) will likely need to scale at higher rates than other parts of the system. 
Decision: The intial style will make use of an event-driven Architecture, but to reduce complexity will allow for synchronous communication between components on a case-by-case basis.  We will favor corregograpy over orchestration to support ease of workflow change.  Specifc servces may play the role of "micro-orchestrators" over the functionality within their domain as needed.

Consequenses: A message broker will need be defined and configured.  The system overall will be more complex than an a synchronous-based solution.
The system will be more complex to set up initally than a rest-based solution, but should be easier to reason about, maintain and evolve.  

