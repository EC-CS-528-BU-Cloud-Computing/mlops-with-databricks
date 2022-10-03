# MLOps with Databricks in Public Clouds

**Team**

Boston University - Group 11
* Parker Dunn (pgdunn@bu.edu)
* Alan Dautov (dautal@bu.edu)
* Balaji Sathyanarayanan (balajis@bu.edu)
* Suyash Bhatia (suyashb@bu.edu)
* Rifat Maxyutov (rifat555@bu.edu)

State Street Financial
* Ata Turk (aturk@statestreet.com)

## Project Description

** **
## 1. Vision and Goals for the Project
*in progress*

** **
## 2. Users/Personas of the Project
*in progress*

** **
## 3. Scope and Features of the Project

The broad scope of our project is all components of machine learning pipelines. The core of our project, espeically toward the beginning, will be preparing and transforming data in Databricks. The State Street team that we are working develops a platform that delivers data using machine learning and analytics. Machine learning (ML) is an important element of the service, but our focus is on building up the infrastructure that supports ML tasks rather than the development of ML models for any particular task. State Street Financial has models providing the insights they need. Now, we are hoping to help migrate them to a new platform.

The core tool we will be using is the Databricks lakehouse platform. It provides a cloud computing workspace with storage and computation service and integrates with AWS and Azure tools. Our work will be completed, at least primarily, in Databricks. However, we are also tasked with determining how to integrate with these other public clouds. Thus, we may be responsible for knowing and working in these other cloud platforms. However, it is not in the scope of this project to build out separate ML operations platforms on Azure and AWS. The additional public clouds are included due to the features that integrate with Databricks. For example, Amazon S3 buckets can be accessed and manipulated from Databricks.

In Databricks, we will develop data pipelines that support ML tasks and user applications (- these user applications use the State Street team's platform). Loading, preparing, manipulating, and monitoring data are all within the scope of our work on the Databricks platform. As well as monitoring and deployment of ML models. Development of new ML models from scratch is not a primary concern of our project. *_I should probalby include an example of at least one 'user story' here._*

In addition to implementation of operations, evaluation of the cloud platforms discussed so far is in the scope of this project. We expect to primarily replicate existing work when it comes to impelmentation. An important part of our work is evaluating and comparing what is offered by Databricks to what is offered by the current service used by State Street Financial - Datarobot. We are evaluating the features available with Databricks and the feasibility of migrating/replicating existing operations. We are not assessing administrative components of the clouds, just the potential of using Databricks for an platform that is already providing a service.

OUTLINE:
* Highlight that the core of our project is "ops" not ML
* Discuss the services that we need to use/learn
* Discuss what kind of work goes into "ops"
* Discuss evaluation as a goal and what that looks like

FOLLOW UP:
* I didn't have any epics/stories/examples to give an example of what is *_in_* the scope of the project
* Are there any kind of metrics or specifics that we can use to evaluate the Databricks platform? I just wrote about how it is within the scope of our project to determine how we can integrate Databricks with current work.

** **
## 4. Solution Concept
*in progress*

** **
## 5. Acceptance criteria
*in progress*

** **
## 6. Release Planning
*in progress*

** **
## General Questions
1. What AWS/Azure tools are you looking to use? Is there already data in these sources or are you looking for other products like AWS SageMaker?
  - Follow up: Would you be interested in using the Databricks version of AutoML (from Datarobot) for example?
