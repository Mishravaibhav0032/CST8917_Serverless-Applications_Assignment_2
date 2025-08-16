# CST8917_Serverless-Applications_Assignment_2
# Serverless Alternatives Across Clouds: Azure, AWS, and GCP
**Course:** CST8917 – Serverless Applications  
**Assignment:** 2 – Serverless Alternatives Across Clouds: Azure, AWS, and GCP Report  
**Due Date:** 15th August, 2025  
**Author:** Vaibhav Mishra (041165850) 

## Overview
This analysis examines the primary Azure serverless offerings from the **CST8917 Serverless Applications** curriculum, juxtaposing them against comparable services in **Amazon Web Services (AWS)** and **Google Cloud Platform (GCP)**.  
Key aspects evaluated include core functionalities, event triggers and integrations, connectivity with other tools, observability features, and cost structures, fostering a broader perspective on serverless design choices.

---

## 1. Azure Functions

**Description**  
Azure Functions delivers on-demand, event-triggered code execution in a serverless environment, with built-in scaling and support for diverse programming languages, seamlessly linking to Azure's broader portfolio.

| Aspect | Azure Functions | AWS Lambda | Google Cloud Functions |
|--------|-----------------|------------|------------------------|
| Name | Azure Functions | Lambda | Cloud Functions |
| Event Triggers & Bindings | Webhooks, Schedules, Storage Blobs, Message Queues, Event Grids, Streaming Hubs | REST APIs via Gateway, Object Storage, NoSQL Tables, Event Buses, Queues | HTTP Requests, Messaging Topics, Object Buckets |
| Supported Runtimes | .NET, Node.js, Python, JVM Languages, Shell Scripts | JavaScript, Python, JVM, GoLang, .NET Core, Ruby | JavaScript, Python, GoLang, JVM, .NET |
| Auto-Scaling | Dynamic (Consumption), Enhanced (Premium), Fixed (App Service) | Demand-Based | Fully Managed Scaling |
| Cost Basis | Executions + Runtime Duration | Invocations + Processing Time | Calls + Execution Duration |

**Connectivity Features**
- **Azure:** Workflow Tools, Messaging Buses, Event Routers, File Storage, API Gateways  
- **AWS:** REST Gateways, Orchestrators, Notifications/Queues, Key-Value Stores  
- **GCP:** API Managers, Orchestration Engines, Topics/Subs, Document Databases  

**Observability Tools**
- Azure Insights & Logging Suite  
- AWS Unified Monitoring Platform  
- GCP Integrated Metrics & Logs  

**Advantages**
- Extensive event bindings  
- Deep ties to Azure tools  
- Varied deployment models  

**Drawbacks**
- Initial delay in cold starts (basic plan)  
- Elevated expenses for sporadic use in advanced tiers  

---

## 2. Durable Functions

**Description**  
An add-on to Azure Functions enabling persistent orchestrations, supporting patterns such as sequencing, parallel branching, and interactive approvals.

| Aspect | Durable Functions (Azure) | Step Functions (AWS) | Workflows (GCP) |
|--------|---------------------------|----------------------|-----------------|
| Name | Durable Functions | Step Functions | Workflows |
| Workflow Styles | Sequencing, Branching/Joining, Long-Running APIs, Approval Flows | Linear/Concurrent Machines | Linear/Concurrent Orchestrations |
| Persistence Mechanism | Azure Blob/Table Storage | NoSQL/S3 Buckets | Bucket/Document Storage |
| Cost Basis | Function Runs + Data Persistence | Transitions + Compute | Orchestration Runs |

**Connectivity Features**
- Azure Code Execution, Workflows, Event Distributors, Messaging  
- AWS Compute, Notifications, Queues, REST Interfaces  
- GCP Code Execution, Topics, Task Managers  

**Observability Tools**
- Azure Metrics & Insights  
- AWS Monitoring Suite  
- GCP Metrics Platform  

**Advantages**
- Seamless state handling  
- Code-centric approach like standard functions  

**Drawbacks**
- Dependency on Azure for persistence  
- Tricky troubleshooting for stateful logic  

---

## 3. Azure Logic Apps

**Description**  
A drag-and-drop orchestration platform for automating processes with extensive pre-built integrations.

| Aspect | Logic Apps (Azure) | Step Functions/AppFlow (AWS) | Workflows + Connectors (GCP) |
|--------|--------------------|------------------------------|------------------------------|
| Name | Logic Apps | Step Functions or AppFlow | Workflows with Connectors |
| Connectivity | Over 200 Adapters, Business Packs | Native AWS + Third-Party Links | GCP Adapters & APIs |
| Cost Basis | Triggers/Actions | Transitions (Steps) or Flows | Steps per Run |

**Connectivity Features**
- Azure Code, Messaging, Events  
- AWS Compute, REST, Data Flows  
- GCP Code, Messaging  

**Observability Tools**
- Azure Metrics  
- AWS Logs/Metrics  
- GCP Logging  

**Advantages**
- Vast adapter ecosystem  
- Quick setup for connections  

**Drawbacks**
- Steep fees for expansive automations  
- Constraints on intricate computations  

---

## 4. Azure Service Bus (Queues/Topics)

**Description**  
Robust messaging infrastructure for direct queuing and broadcast subscriptions.

| Aspect | Service Bus (Azure) | SQS/SNS (AWS) | Pub/Sub (GCP) |
|--------|---------------------|--------------|---------------|
| Name | Service Bus | Simple Queue/Notification Services | Pub/Sub |
| Standards | Advanced Messaging Protocol | Custom | Custom |
| Capabilities | Ordered Delivery, Error Queues, Timed Sends, Deduplication | Ordered, Error Handling, Delays | Guaranteed Delivery, Sequencing |
| Cost Basis | Operations + Egress | Requests | Messages + Volume |

**Connectivity Features**
- Azure Code, Workflows, Events  
- AWS Compute, Orchestrators, Interfaces  
- GCP Code, Stream Processors  

**Observability Tools**
- Azure Metrics  
- AWS Suite  
- GCP Metrics  

**Advantages**
- Advanced messaging options  
- On-prem/cloud bridging  

**Drawbacks**
- Setup overhead versus basic queues  

---

## 5. Azure Event Grid

**Description**  
Managed pub-sub system for routing events efficiently.

| Aspect | Event Grid (Azure) | EventBridge (AWS) | Eventarc (GCP) |
|--------|--------------------|-------------------|----------------|
| Name | Event Grid | EventBridge | Eventarc |
| Origins | Azure Natives, Custom, Partners | AWS Natives, Apps, Custom | GCP Natives, Apps, Custom |
| Destinations | Azure Code, Workflows, Messaging | AWS Compute, Orchestrators, Messaging | GCP Runtimes, Code, Messaging |
| Cost Basis | Operations | Events | Events |

**Connectivity Features**
- Azure Code, Workflows, Messaging  
- AWS Compute, Orchestrators  
- GCP Runtimes, Code  

**Observability Tools**
- Azure Metrics  
- AWS Suite  
- GCP Logs  

**Advantages**
- Strong Azure linkages  
- Rapid propagation  

**Drawbacks**
- Primarily Azure-oriented  

---

## 6. Azure Event Hubs

**Description**  
Scalable ingestion for massive event streams.

| Aspect | Event Hubs (Azure) | Kinesis Streams (AWS) | Pub/Sub (GCP) |
|--------|--------------------|-----------------------|---------------|
| Name | Event Hubs | Kinesis Data Streams | Pub/Sub |
| Capacity | High-Volume Events | High-Volume | High-Volume |
| Applications | Sensor Data, Real-Time Pipes | Analytics Streams | Ingestion Streams |
| Cost Basis | Capacity Units + Storage | Shard Time + Data | Volume + Storage |

**Connectivity Features**
- Azure Stream Processors, Code  
- AWS Compute, Stream Analytics  
- GCP Processors, Code  

**Observability Tools**
- Azure Metrics/Logs  
- AWS Suite  
- GCP Metrics  

**Advantages**
- Extreme scale, Multi-Consumer Partitions  
- Kafka Compatibility  

**Drawbacks**
- Cost variability for irregular loads  

---

## Consolidated Comparison

| Azure Offering | AWS Counterpart | GCP Alternative |
|----------------|-----------------|-----------------|
| Functions | Lambda | Cloud Functions |
| Durable Functions | Step Functions | Workflows |
| Logic Apps | Step Functions/AppFlow | Workflows + Connectors |
| Service Bus | SQS/SNS | Pub/Sub |
| Event Grid | EventBridge | Eventarc |
| Event Hubs | Kinesis Streams | Pub/Sub |

---

## Final Thoughts
Grasping these multi-cloud parallels empowers better strategic choices, efficiency in spending, and resilience in designs. Azure shines in cohesive serverless environments, yet AWS and GCP present robust options with distinct benefits and trade-offs.
