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
                             ## Proposed Microservice Applications
The new platform is all about architecting cloud-native applications, targeting large and complex applications with multiple independent development teams working on different microservices that can be developed and deployed autonomously based on : 
.NET Core or ASP.NET Core
Cloud-Native platforms 


# Serverless Microservices reference architecture

## The reference architecture
