# Runbook-for-Retail-Web-Application-ver.-2.0.0
Runbook for Retail Web Application ver. 2.0.0

Introduction
This runbook is basically a documentation for  cloud migration strategy, migrating a monolithic application to an Azure serverless environments. building a serverless-based microservices architecture.Serverless offers a consumption-based pricing where you only pay for what you use and nothing more manage scaling resources to meet demand automatically. When developing microservices-based applications and managing them using serverless functions it offers the opportunity of combining the flexibility and service isolation of a microservices architecture.
Monolithic architecture offers tight coupling between tiered layers, the individual components can't be scaled. In developing modern applications that needs to be hosted in the cloud, statelessness is an essential factor in developing cloud-aware applications.
## Assumption on preexisting monolithic applications
Based on the traditional .NET Framework.
ASP.NET MVC
ASP.NET Web Forms 
N-Tier app with a WinForms client desktop app consuming a WCF service backend.

![alt text](https://github.com/raphaeljuwe/Runbook-for-Retail-Web-Application-ver.-2.0.0/blob/master/Capture.PNG)

![alt text](https://github.com/raphaeljuwe/Runbook-for-Retail-Web-Application-ver.-2.0.0/blob/master/State%20storage.PNG)

## Proposed Microservice Applications
The new platform is all about architecting cloud-native applications, targeting large and complex applications with multiple independent development teams working on different microservices that can be developed and deployed autonomously based on : 
.NET Core or ASP.NET Core
Cloud-Native platforms 

## Serverless Microservices reference architecture
![alt text](https://github.com/raphaeljuwe/Runbook-for-Retail-Web-Application-ver.-2.0.0/blob/master/Refrence.PNG)


The microservice-based architecture solves challenges of  distributed mission-critical applications being that it builds on a collection of services that can be developed, tested, deployed, and versioned independently. A reference architecture is a template of required components and the technical requirements to implement them. A reference architecture isn't custom-built for a customer solution, but is a high-level  scenario based on extensive experience. 
Common serverless architecture patterns include:
Serverless APIs, mobile and web backends.
Event and stream processing, Internet of Things (IoT) data processing, big data and machine learning pipelines.
Integration and enterprise service bus to connect line-of-business systems, publish and subscribe (Pub/Sub) to business events.
Automation and digital transformation and process automation.
Middleware, software-as-a-Service (SaaS) like Dynamics, and big data projects.

Azure Functions are a great multi-purpose easy to spin-up service for Compute, Machine learning, Analytics and Transactions  but in de-constructing monolithic applications Azure functions are not a good fit, instead  Fabric which is designed explicitly for Microservices and various Docker capabilities which are well suited for Microservices. Functions don’t really have the management layers in place to be the key for large-scale microservices.


## Azure resources required to deploy the serverless solution

Resource Group

Storage Account

Function App

MSSQL server DB Container

Web App Service Plan

SQL Database Server

SQL Database

SQL Database Table

Web App Service

API Management Service

## Assignment

### (1) Diagram a serverless architecture (SaaS) on a cloud platform preferably Azure. Keep in mind that the codebase is C# (.NET framework), elaborate on the diagram.

The diagram can be found at : https://app.cloudskew.com/viewer/ece70ed1-43a5-421e-9241-7f96ba9442a6

### (2) Create a “go live plan” and document the steps that would have to be taken prior to going live on the new environment. Try to be as detailed as possible.

The migration process described here is meant to go from an on-premises, monolithic architecture to a microservices-based architecture running on Azure.
There are three main patterns for migrating to the cloud: lift and shift, improve and move, and rip and replace. During migration, the application has a hybrid architecture where some features are in the cloud and some are still on-premises. After the migration is finished, the complete application is hosted in the cloud, but it still interacts with backend services that remain on-premises. 

#### The proposed “go live plan” offers a clear boundary between services.
##### Questions in migrations;
How much data is to be migrated?
How often does this data change?
Downtime cost, how does it effect your business?
What is your current data consistency model?
1)	An iterative process of idea generation, prototyping, automation, presentation, information capturing, analysis and learning, defining the target Serverless Architecture (Have a fully serverless architecture involves removing the Azure VM instance).
(2) Build separate, serverless version of the application, following a Step by Step Migration to Serverless Approach. 
(3) Migrate in chunks, avoiding large big-bang cutovers as far as possible.  
In the migration process, in the initial state of the migration the, public APIs are hosted on Azure, while the backend on-premises systems can be exposed as private APIs that are consumed only by microservices on Azure.
## Features with independent datasets
In migrating features whose datasets are independent from other datasets. These independent datasets are easier to extract from your legacy system than datasets that have dependencies. (when compared to migrating stateless features, migrating features that have independent datasets requires additional work, namely creating and managing the new data store along with actually migrating the data.)
##Features with shared datasets
Features with shared datasets are the hardest to migrate due to the requirements for consistency, distribution, access, and latency.
Data processed by Azure Functions can be stored into various Azure data services such as Azure storage, Azure SQL DB and Document DB.
(4) Choosing which features to migrate and when to migrate them is one of the most important decisions an organization will make during this stage of the project. When making this decision, an organization must take into account the web of dependencies between features. Some features might heavily depend on others to work correctly, while others might be fairly independent. The fewer dependencies a feature has, the easier it is to migrate. Create a plan to deploy your Azure resources, including the AKS clusters, using infrastructure as code (IaC). 
5.) Choose a platform to send all alerts for incidence management.
6.) Implement best practices for team’s collaboration in the platform so that the actions/knowledge are captured.
7.) Build basic action plans with clear steps on how to resolve the issues, who to contact, what to refer to, where to find documentation, etc. and what didn’t work. 
