<!-- 

Github:

 -->

 # CST8917 – Serverless Service Alternatives Report

---

## 1. Azure Functions (Triggers & Bindings)

| Cloud Provider | Service Name      |
|----------------|-------------------|
| Azure          | Azure Functions   |
| AWS            | AWS Lambda        |
| GCP            | Google Cloud Functions |

**Overview:**  
- Azure Functions: Serverless compute for running code on demand, with triggers and bindings.  
- AWS Lambda: Runs code in response to events from AWS or external sources.  
- Cloud Functions: Lightweight serverless execution in GCP triggered by events.

**Core Features:**  
- Event-driven execution  
- Many trigger types (HTTP, queue, blob, timer)  
- Input/output bindings to other services  
- Auto-scaling based on demand  

**Integration Options:**  
- Works with storage, databases, queues, APIs, and CI/CD pipelines.  

**Monitoring & Observability:**  
- Azure Monitor, Application Insights  
- AWS CloudWatch Logs, X-Ray  
- GCP Cloud Logging, Cloud Monitoring  

**Pricing Model:**  
- Pay for execution time and number of requests.  

**Strengths & Weaknesses:**  
- Strength: Scales automatically, supports many integrations.  
- Weakness: Cold start delays possible for infrequently used functions.

---

## 2. Durable Functions (Chaining, Orchestration, Fan-out/Fan-in)

| Cloud Provider | Service Name                        |
|----------------|-------------------------------------|
| Azure          | Durable Functions                   |
| AWS            | AWS Step Functions + Lambda         |
| GCP            | Workflows + Cloud Functions         |

**Overview:**  
- Durable Functions: Extension of Azure Functions for long-running workflows with state.  
- Step Functions + Lambda: Visual workflow service for AWS that can call Lambda or other services.  
- Workflows + Cloud Functions: GCP orchestration service with serverless functions.

**Core Features:**  
- Function chaining  
- Parallel execution (fan-out/fan-in)  
- State management  
- Error handling and retries  

**Integration Options:**  
- Connects with other serverless and cloud services.  

**Monitoring & Observability:**  
- Azure Monitor, Application Insights  
- AWS CloudWatch, Step Functions Execution History  
- GCP Cloud Logging, Execution Logs  

**Pricing Model:**  
- Pay per execution and state transition.  

**Strengths & Weaknesses:**  
- Strength: Simplifies orchestration logic.  
- Weakness: Vendor-specific syntax and tooling.

---

## 3. Azure Logic Apps

| Cloud Provider | Service Name          |
|----------------|-----------------------|
| Azure          | Azure Logic Apps      |
| AWS            | AWS Step Functions (Express) + EventBridge + AppFlow |
| GCP            | Workflows + AppSheet Automation |

**Overview:**  
- Logic Apps: Low-code/no-code workflows with connectors to many services.  
- AWS combo: Step Functions (Express) for workflow logic, EventBridge for event routing, AppFlow for SaaS integration.  
- GCP: Workflows for orchestration, AppSheet Automation for SaaS tasks.

**Core Features:**  
- Prebuilt connectors  
- Visual designer  
- Trigger and action-based flows  
- Conditional logic  

**Integration Options:**  
- Connects to APIs, databases, SaaS apps, and messaging systems.  

**Monitoring & Observability:**  
- Azure Monitor, Run History  
- AWS CloudWatch, Step Functions monitoring  
- GCP Cloud Logging  

**Pricing Model:**  
- Pay per execution/connector call.  

**Strengths & Weaknesses:**  
- Strength: Easy for non-developers.  
- Weakness: Less flexible for complex logic than code-first approaches.

---

## 4. Azure Service Bus (Queues & Topics)

| Cloud Provider | Service Name            |
|----------------|-------------------------|
| Azure          | Azure Service Bus       |
| AWS            | Amazon Simple Queue Service (SQS) + SNS |
| GCP            | Pub/Sub                  |

**Overview:**  
- Service Bus: Enterprise messaging with queues (point-to-point) and topics (publish/subscribe).  
- AWS SQS + SNS: Separate services for queues and pub/sub messaging.  
- GCP Pub/Sub: Unified pub/sub messaging service.

**Core Features:**  
- Queues and topics  
- Message ordering and delivery guarantees  
- Dead-letter queues  
- Scheduled delivery  

**Integration Options:**  
- Works with serverless functions and apps.  

**Monitoring & Observability:**  
- Azure Monitor, Metrics  
- AWS CloudWatch for SQS/SNS  
- GCP Cloud Logging, Monitoring  

**Pricing Model:**  
- Pay per operation and message volume.  

**Strengths & Weaknesses:**  
- Strength: Reliable messaging with ordering.  
- Weakness: More complex setup for hybrid scenarios.

---

## 5. Azure Event Grid

| Cloud Provider | Service Name    |
|----------------|-----------------|
| Azure          | Azure Event Grid |
| AWS            | Amazon EventBridge |
| GCP            | Eventarc         |

**Overview:**  
- Event Grid: Event routing with publish/subscribe model.  
- EventBridge: AWS event bus for routing between services and apps.  
- Eventarc: GCP event routing from various sources to targets.

**Core Features:**  
- Event-driven architecture  
- Filtering and routing rules  
- Native integration with cloud services  

**Integration Options:**  
- Ties into serverless functions, workflows, and APIs.  

**Monitoring & Observability:**  
- Azure Monitor  
- AWS CloudWatch, EventBridge metrics  
- GCP Cloud Logging  

**Pricing Model:**  
- Pay per event delivered.  

**Strengths & Weaknesses:**  
- Strength: Decouples services easily.  
- Weakness: Latency can vary for high volume.

---

## 6. Azure Event Hubs

| Cloud Provider | Service Name      |
|----------------|-------------------|
| Azure          | Azure Event Hubs  |
| AWS            | Amazon Kinesis Data Streams |
| GCP            | Pub/Sub Lite      |

**Overview:**  
- Event Hubs: Big data streaming platform for event ingestion.  
- Kinesis: AWS real-time data streaming service.  
- Pub/Sub Lite: GCP low-cost streaming service.

**Core Features:**  
- High-throughput event ingestion  
- Partitioned consumers  
- Real-time processing  

**Integration Options:**  
- Works with analytics, serverless, and storage services.  

**Monitoring & Observability:**  
- Azure Monitor  
- AWS CloudWatch for Kinesis  
- GCP Cloud Monitoring  

**Pricing Model:**  
- Pay for throughput units and storage.  

**Strengths & Weaknesses:**  
- Strength: Handles massive data streams.  
- Weakness: Requires planning for scaling.

---

## Quick Reference Table

| Azure Service                     | AWS Equivalent                         | GCP Equivalent                     |
|-----------------------------------|-----------------------------------------|-------------------------------------|
| Azure Functions                   | AWS Lambda                             | Cloud Functions                     |
| Durable Functions                 | Step Functions + Lambda                | Workflows + Cloud Functions         |
| Azure Logic Apps                  | Step Functions (Express) + EventBridge + AppFlow | Workflows + AppSheet Automation |
| Azure Service Bus (Queues/Topics) | SQS + SNS                               | Pub/Sub                             |
| Azure Event Grid                   | EventBridge                            | Eventarc                            |
| Azure Event Hubs                   | Kinesis Data Streams                   | Pub/Sub Lite                        |
