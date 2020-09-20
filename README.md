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

