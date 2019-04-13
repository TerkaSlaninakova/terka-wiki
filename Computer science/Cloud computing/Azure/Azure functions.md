# Intro
Azure functions are **events (trigger, e.g. scheduler, new data) and code (does something)** 

### Difference between Azure functions and existing services
* IaaS - complete control over server, but also responsibility of tuning, maintaining a server / group of servers

* Azure Cloud services - Web roles / worker roles - microsoft manages automatic scaling

* Azure Web applications - easy to deploy, scale up to many servers
    * background tasks: **web jobs** - **azure functions are built on top of web jobs sdk**

### Advantages
- no boilerplate code, just the relevant 'business' code rensponding to events
- more cost-effective (pay only for what you use)

### Serverless
- as a developer, you focus purely on business (use 3rd party P(latform)aaS to run your code whenever possible - e.g. using DocumentDb instead of server and installing database yourself). But sometimes you do need to write some custom backend logic, that's where functions (or FaaS) come in.
    - Azure functions is not a serverless framework, but it fulfills the 'service' part of serverless approach. Use it in conj. w/ other services to create a full serverless architecture

### Example
Instead of having a monolithic server doing everything for a running web app, select the payment provider hook to be run by an Azure function that posts a message about a payment to a queue. Another function will handle generation of license message. Another for reporting. Another for validating license API, and so on. **The goal is decomposition into loosely coupled functions.** There's also a concept of **Function apps**, which are groupings of Azure functions.

### Use cases
- great for experiments and prototyping, automation (hosting slack webhook to CI server)
- https://www.troyhunt.com/azure-functions-in-practice/