# 				**Disaster Recovery**

### What is Disaster Recovery(DR)?

- **Disaster Recovery (DR)** is a strategic framework of policies, tools, and procedures used to restore an organization's critical IT infrastructure and systems after a major disruptive event. While often confused with data backup, DR is broader; it focuses on regaining full functionality of applications, networks, and hardware so business operations can resume as quickly as possible.

### How Cloud Disaster Recovery Works

- Disaster recovery works by creating a redundant environment that can take over when the primary systems fail. This involves several key technical processes: 

  - **Replication:** Continuously copying data and computer processing from a primary site to an off-premises recovery site.

  - **Failover:** An automated or manual process that switches IT operations to a secondary system during an outage.

  - **Failback:** The process of moving operations back to the primary location once it is fully restored.

### Core Metrics of Success

- Organizations use two critical metrics to define their DR goals: 

  - **Recovery Time Objective (RTO):** The maximum amount of time a system can be down before the consequences become unacceptable (e.g., "we must be back online within 2 hours").

  - **Recovery Point Objective (RPO):** The maximum amount of data loss an organization can tolerate, measured in time from the last successful backup (e.g., "we cannot lose more than 1 hour of data").

### Common Recovery Methods

- Depending on budget and urgency, organizations choose different recovery site named "temperatures" :

  - **Hot Site:** A fully functional, real-time replica of the primary site that allows for near-instant recovery but is the most expensive.

  - **Warm Site:** A secondary facility equipped with hardware and up-to-date data, but requires some manual steps to fully activate systems.

  - **Cold Site:** A basic facility with power and connectivity but no active IT equipment; it takes the longest to set up during a disaster.

  - **DRaaS (Disaster Recovery as a Service):** A cloud-based model where a third-party provider handles the entire replication and orchestration process. 

# 					RTO & RPO

- **Recovery Time Objective (RTO)** and **Recovery Point Objective (RPO)** are the two most critical metrics in disaster recovery and business continuity planning. While they both measure time, they focus on two different aspects of a crisis: **downtime** and **data loss**.

![img](https://miro.medium.com/v2/resize:fit:875/1*wgR8oapYESi6QmNeUK7jmw.png)

### **1. Recovery Time Objective (RTO)**

- RTO is the "downtime" limit. It represents the maximum amount of time your organization can afford for a system to be offline before the consequences become unacceptable.

  - **The Question:** "How fast can we recover?"

  - **Example:** If an online shop has an RTO of **1 hour**, IT must have the site restored within 60 minutes of the crash to avoid massive revenue loss.

  - **Cost Factor:** Lower RTOs require expensive solutions like **hot standby** servers and automated failover systems.

### **2. Recovery Point Objective (RPO)**

- RPO is the "data loss" limit. It determines how far back in time you must be able to recover data from your last backup.

  - **The Question:** "How much data can we afford to lose?"

  - **Example:** If your bank's RPO is **15 minutes**, your systems must back up data at least every 15 minutes. If a crash occurs, you only lose 15 minutes of transactions at most.

  - **Cost Factor:** Stricter RPOs require more frequent backups, continuous data protection (CDP), and higher storage capacity.

### **How to Set Your Targets**

- Organizations often use a **tiering system** to balance cost and safety:

  - **Tier 1 (Mission-Critical):** Payments, core banking. Requires near-zero RTO/RPO.

  - **Tier 2 (Business-Critical):** Key business apps. Targets are often 1–4 hours.

  - **Tier 3 (Standard/Low Priority):** Internal reporting or archives. Can tolerate 24+ hours. 

### **Key Differences at a Glance**

| Feature            | Recovery Time Objective (RTO)                                | Recovery Point Objective (RPO)                               |
| :----------------- | :----------------------------------------------------------- | :----------------------------------------------------------- |
| **Focus**          | **Downtime**: How quickly you must be back online.           | **Data Loss**: How much data you can afford to lose.         |
| **Measurement**    | Time **forward** from the disaster (e.g., "Back up in 2 hours"). | Time **backward** from the disaster to the last backup (e.g., "Lose 15 mins of data"). |
| **Primary Driver** | Drives system architecture and **recovery strategy**.        | Drives **backup frequency** and replication schedule.        |
| **Business Goal**  | Minimize the duration of system outages.                     | Minimize data loss and ensure data integrity.                |