Learn DevOps
===================

DevOps! What is it?
********************

DevOpss is a collaboration between development, operations and other teams with the recognition that we are tasked with achieving common business goals.

| **How to achieve?**
1. Systems thinking: global optimization, faster as a whole
  - no defect to downstream work centers
  - no allow local optimizationi to create global degradation
  - increase flow
  
2. Feedback loop: Amplify and shorten Feedback Loops
  - page load times
  - measure throughput of work through the system
  - building right thing?
  - Metrics
  - Postmortems/learning reviews
    
3. Culture of Experimentation: continual experimentation and learning failure
  - allocating time for improvement of daily work
  - rewards for taking risks
  - introduce fault into system to increase resilience, site switching?
  
4. Principle of Kaizen: 
  - continuous improvement, getting better all the time
  - systems thinking 
  - quality
  - process control
  - minimal inventory


CAMS model
-----------

| **Culture**
- service ownership
- hack events
- technical debt grooming 
- game days
- destructive testing (shutdown datacenter)
- cross functional teams
- agile 
Cargo culting? no!!

| **Automation**
- why automate? expensive, not scalable, more errors,  

- infrastructure as code - configuration management
- continuous delivery pipeline
- Simian army (?)
- Orchestration engine (?)

| **Measurement**
- why measure? metrics, monitoring, see data
- what to measure? cost?, revenue? how many signed up? how many calls? ...

- Instrumentation platform (Graphite, OpenTSDB ..)
- Information radiators (?)
- Process measurement (cycle time, MTTR, ...)


| **Sharing**  
- why sharing so important?
- visibility(everybody can see) + transparency(why you did) + knowledge transfer

- daily standup
- retrospectives 
- documentation 
- Brown bags/Tech talks/Internal conferences
- ChatOps -log, history


Continuous Delivery
---------------------
what is continuous delivery (CD)? what is continuous deployment? is same?

- system should be automated/repeatable
- run to the pain
- version controlled
- always deployable (working code)
- everyone's reponsibility

What CD systems looks like?
- DO small amount of changes (Unit Tests), fast!
- -> Integration Tests 
- >> Security Tests, >> Test Env A, >> Test Env B
everything went fine, humans can decide to push into production or not, but

Continuous deployment? if all tests passed through the continuous delivery pipelines, software automatically go into the production. Without continuous delivery, there is no continuous deployment.

Life Cycle of DepOvs
---------------------

