# light-runbook
A runbook application for support team to respond on error code alerts

### Introduction

In a computer system or network, a runbook is a compilation of routine procedures and operations that the system administrator or operator carries out. System administrators and operators in IT departments use runbooks as a reference. Runbooks can be in either electronic or in physical book form. Typically, a runbook contains procedures to begin, stop, supervise, and debug the system. It may also describe procedures for handling special requests and contingencies. An effective runbook allows other operators, with prerequisite expertise, to effectively manage and troubleshoot a system. Through runbook automation, these processes can be carried out using software tools in a predetermined manner.

Runbooks are typically created by technical writers working for top-tier managed service providers. They include procedures for every anticipated scenario and generally use step-by-step decision trees to determine the effective response to a particular scenario.

### Microservice

For most organizations, the runbook is in Excel or Word format and distributed electronically. It works for monolithic applications as there are dedicated support team per application. When working with micorservices built on top of the light platform, the traditional way is not working any more. 

* First, the same support team might need to support hundreds or even thousands services.

* Second, majority of the procedures defined in each service will be the same for all services as they are the generic procedures for the platform. Each service will only have a small portion of service specific procedures. 

Given the above reasons, it makes sense for us to build an application that can manage the runbook for our customers. For most common procedures, we can predefine them in the system and leave the door open for customization. Each service owner will add their own service specific procedures. The operation team will just go to a website instead of searching from dozens or hundreds of documents in a local directory. 

### Design

The backend will be a microservice built on top of light-hybrid-4j framework and frontend will be a React single page application. We can support both Arango and SQL database for portability. 

This application shoud be OK to deploy independently or as part of the light-portal. 

The procedures defined in the runbook can be manual or automation with light-bot so that there is no human involved for certain triggers. 


