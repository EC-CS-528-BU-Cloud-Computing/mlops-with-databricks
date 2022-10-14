# MLOps with Databricks in Public Clouds

## Team

* Parker Dunn (pgdunn@bu.edu)
* Alan Dautov (dautal@bu.edu)
* Balaji Sathyanarayanan (balajis@bu.edu)
* Suyash Bhatia (suyashb@bu.edu)
* Rifat Maxyutov (rifat555@bu.edu)

## Links to Important Materials

[Bi-weekly sprint presentations (videos)](TBD)
[Presentations about Databricks features](TBD)

## Project Description

** **
## 1. Vision and Goals for the Project

Machine learning is a subset of AI which is extensively leveraged in many practical applications today. A machine learning model is implemented through a machine learning lifecycle. A ML lifecycle is a series of steps which are executed to produce and deploy a machine learning model. A ML pipeline is related to the ML lifecycle. The pipeline is a process to automate the workflow it takes to produce a ML model. It is an iterative process consisting of independent modules which are repeated multiple times to increase the efficiency of the ML model.

Our project is MLOps with Databricks in public clouds. MLOps stands for Machine Learning Operations. It is a core function of Machine Learning engineering, focused on streamlining the process of taking machine learning models to production, and then maintaining and monitoring them. It can also be thought of as a set of practices that aims to deploy and maintain ML models in production efficiently and reliably.

The financial firm we are working with has many in-house built ML pipelines which are centrally managed by different departments on the on-prem MLOps solutions, Datarobot (a ML platform that manages models). Databricks is another platform which can deal with huge amounts of data and we can explore the data through ML models. Databricks has extended capabilities and features when compared with Datarobot. We are trying to investigate the MLOps capabilities of Databricks. We are evaluating the possibility of transitioning MLOps workloads from on-prem Datarobot to public cloud Databricks. We will also replicate some MLOps pipelines deployed in on-prem Datarobot in Databricks on two public clouds. We are trying to explore Databricks and understand whether it is more efficient than Datarobot in handling ML workloads. Solutions will be evaluated from ease of transformation, cost and efficiency perspectives. 

By and large, our end goal is to give our collaborators a starting point to help them migrate to Databricks. We want to give them enough information and documentation so that it is a seamless process. We will also have to contest Databricks against the current platform they are using in order for them to know the advantages of using Databricks over the other.

** **
## 2. Users/Personas of the Project

The industry collaborators provide a platform for customers in the financial industry.

This description is broad because the scope of the products included in this project is large. The type of service being provided is straight-forward: data pipelines, data analysis, and production machine learning services. However, the implementation of each of these can vary quite a bit across the platform that we are helping to build on Databricks.

We will build pipelines that retreive, prepare/process, and monitor data. This, on its own, may be a service that is offered by the platform in some cases. A more involved pipeline would involve these data engineering steps in addition to development of machine learning models. These pipelines have additional steps of preparing, training, and validating a machine learning model. A robust model may allow the platform to provide new insights to customers. Additionally, we will monitor and provide continuous developement and deployment support for ML models, ensuring initial insights provided by the platform are sustainable in the long-term as well. This described pipeline is a prototypical example of the services of an ML operations (MLops) platform. In many cases, users may expect the entire pipeline of services to be offered to support their applications. However, the Databricks platform has many useful services that do not match this prototypical example, which we may also have to implement at the request of our collaborators.

We have also bene tasked with assessing Databricks by our collaborators. Thus, in addition to their clients, our collaborators are also a user of our work. For this part of our project, we will provide two services: (1) assessment of the capabilities of Databricks and (2) the integration/substitution potential of Databricks and Datarobot. Our collaborators currently perform MLops with Datarobot. We are tasked with identifying what elements of their current MLops can be transitioned to Databricks.


** **
## 3. Scope and Features of the Project

The broad scope of our project is all components of machine learning pipelines. The focus of our project, espeically toward the beginning, will be preparing and transforming data in Databricks. Our collaborators from a financial firm develop a platform that delivers data using machine learning and analytics. Machine learning (ML) is an important element of the service, but our focus is building up the infrastructure that supports ML tasks rather than the development of ML models. The financial firm has models providing the insights they need. Now, we are hoping to help them migrate to a new platform.

The tool we will be using is the Databricks lakehouse platform. It provides a workspace with storage and computation service integration in AWS and Azure. Our work will be completed, at least primarily, in Databricks. However, we are also tasked with determining how to integrate with these other public clouds. Thus, we may be responsible for knowing and working in these other cloud platforms. However, it is not in the scope of this project to build out separate ML operations platforms on Azure and AWS. The additional public clouds are included due to the features that integrate with Databricks. For example, Amazon S3 buckets can be accessed and manipulated from Databricks.

In Databricks, we will develop data pipelines that support ML tasks and user applications (- these are users of the financial firm's platform). Loading, preparing, manipulating, and monitoring data are all within the scope of our work on the Databricks platform. As well as monitoring and deployment of ML models. Development of new ML models from scratch is not a primary concern of our project. For example, we may be provided with raw data and asked to produce a machine learning pipeline with a model that makes predictions. However, the model design is not our concern. We focus on creating a servicable model, not a novel one. Additionally, we would be encouraged to explore the Databricks ML tools (like MLflow, which has some pre-determined ML models) rather than developing something novel.

In addition to implementation of operations, evaluation of the cloud platforms discussed so far is in the scope of this project. We expect to primarily replicate existing work when it comes to impelmentation. An important part of our work is evaluating and comparing what is offered by Databricks to what is offered by the current service used by the financial firm - Datarobot. We are evaluating the features available with Databricks and the feasibility of migrating/replicating existing operations. We are not assessing administrative components of the clouds, just the potential of using Databricks for an platform that is already providing a service.


** **
## 4. Solution Concept
MLops is an approach that aims to efficiently deploy, maintain, and monitor machine learning models. Since machine learning lifecycle has many steps such as data ingest, model training, model deployment, it is important for data engineering, data science and ML engineering teams to collaborate synchronously and efficiently. One way to do so is to use Databricks with public clouds such as Microsoft Azure or Amazon Web Services. Databricks allows data engineers, data scientists, and analysts to work together since it provides collaborative notebooks, IDEs, dashboards, and other tools to access and analyze common underlying data. 

The solution implies exploring what can Databricks offer in terms of data warehousing, data engineering, data streaming and machine learning. The main goal is to evaluate Databricks solutions from ease of transformation, cost, and efficiency perspectives and then give an assesment on whether it is reasonable to use Databricks.

![azure-databricks-modern-analytics-architecture-diagram](https://user-images.githubusercontent.com/75428513/194418588-d0de82ac-da30-41fb-9548-e236f2576045.png)

1. Azure Databricks ingests raw streaming data from Azure Event Hubs.
2. Data Factory loads raw batch data into Data Lake Storage.
3. For data storage: 
    1. Data Lake Storage houses data of all types, such as structured, unstructured, and semi-structured. It also stores batch and streaming data.
    2. Delta Lake forms the curated layer of the data lake. It stores the refined data in an open-source format.
    3. Azure Databricks works well with a medallion architecture that organizes data into layers: Bronze: Holds raw data. Silver: Contains cleaned, filtered data. Gold: Stores aggregated data that's useful for business analytics.
4. The analytical platform ingests data from the disparate batch and streaming sources. (Data preparation, Data exploration, Model preparation, Model training.)
5. Azure Databricks stores information about models in the MLflow Model Registry. The registry makes models available through batch, streaming, and REST APIs.
6. Services that work with the data connect to a single underlying data source to ensure consistency. For instance, users can run SQL queries on the data lake with Azure Databricks SQL Analytics. 
7. Power BI generates analytical and historical reports and dashboards from the unified data platform. 
8. Users can export gold data sets out of the data lake into Azure Synapse via the optimized Synapse connector. SQL pools in Azure Synapse provide a data warehousing and compute environment.
9. The solution uses Azure services for collaboration, performance, reliability, governance, and security.

More details here: https://learn.microsoft.com/en-us/azure/architecture/solution-ideas/articles/azure-databricks-modern-analytics-architecture




** **
## 5. Acceptance criteria

__*Minimum Acceptance*__  
We must be able to provide an evaluation of Databricks on public clouds for the financial firm. Our work will start in Databricks, so we are expected to learn enough that we can implement some machine learning operations on the platform. It should be clear by the end of our project what the platform is capable of so that the financial firm understands how they can use the platform for their work. This minimum acceptance work will come in the form of write ups and/or presentations that explain capabilities and limitations of Databricks for ML operations accompanied by examples generated by our team. Even if we do not have a chance to complete migration of the financial firm's Datarobot MLops to Databricks, it should be clear how Databricks can be integrated or how it can replace Datarobot.

__*Stretch Goals*__  
Our partner financial firm does not currently use Databricks in any capacity. There will be a significant learning and experimenting period for this project. We hope to accomplish this portion of the project and leave enough time to assist the financial firm with integrating Databricks into their current operations.
This stretch goal would broadly involve implementing data processing pipelines, deploying ML models, and managing/monitoring deployment of ML services. Ideally, all of these features will be implemented on Databricks to provide the financial firm's platform engineering team with a new platform for providing their services to user applications.

** **
## 6. Release Planning

We will not produce *"regular"* updates to a single platform or project. We will deliver new features in the form of functional machine learning operatoins pipelines.

Each pipeline we develop will have a clear start and end. We will identify a data source to use and determine a target piece of information or MLops service to produce. In general, the pipelines we are working on have not and will not be defined in advance. We will work on them as requested by our collaborators as we go or as determined by the Databricks features that we would like to learn and test.

For example, our first product will be a machine learning pipeline that starts with financial transaction data, implements an ML model to identify financial fraud, and assesses the performance of the ML model in the context of the problem. This particular task will not explore the possibilities of production-level ML tools, so another product will focus on these services on Databricks.

** **
