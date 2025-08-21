# Azure & AWS

## AWS 

### 🌩️ What is Cloud Computing?
````
Instead of buying your own big computer (servers, storage, network), you rent them from a company (like AWS) using the internet.
You pay only for what you use (like electricity, water).

Earlier companies used to buy their own infrastructure like servers, storage, and networking. But instead of building and maintaining all this, now we can use AWS cloud services. In AWS we only pay for what we use, like electricity or water bill.

````
#### 🌟 Advantages of AWS
```
1.COST SAVING:-
  In AWS we do not need to buy costly hardware
  we pay only for what we use

2.SCALABILITY & FLEXIBILITY:-
  If work load increases, we can aquickly add more storage or servers.
  If workload decreases, we can reduce resources

3.High Availability & Reliability:-
  AWS has multiple regions and availability zones.
  Even if one datacenter fails, our application can run from another.

4.Global Reach:
  AWS has datacenters all over the world.
  We can host applications closer to users (low latency).

5.Security:-
AWS follows high-level security standards.
Features like IAM (Identity & Access Management) help us control access.

6.Managed Services:-
We don’t have to manage everything.
Example: AWS RDS manages database backups, patching, and updates automatically.

7.Innovation & Variety:-
AWS provides 200+ services (AI, Machine Learning, IoT, Big Data).
We can choose the right tool as per requirement.

```
🏗️ Services of AWS
```
AWS provides
1.Infracture as a service,
2.Platform as a Service,
3.Swaftware as a service.


🔵 0. On-Premises () :- 
👉 Company owns everything – from hardware to applications.
We Manage all (100% Responsibility)

1.Networking (switches, routers, firewalls)
2.Storage (disks, SAN/NAS)
3.Servers (physical machines)
4.Virtualization (VMware, Hyper-V)
5.OS (Windows/Linux installation & patching)
6.Middleware (web servers, app servers)
7.Runtime (Java, .NET, Python environments)
8.Data (databases, files)
9.Applications (ERP, CRM, websites, etc.)
10.Security (firewalls, access control, backups, DR)

🟢 1. IaaS (Infrastructure as a Service)
👉 AWS provides raw infrastructure (compute, storage, networking, virtualization, physical security).
👉 We install and manage OS, DB, and applications.
We Manage:- OS,Middleware,Runtime,Data,Applications
AWS Manages:- Networking,Storage,Servers (hardware), Virtualization, Security (infrastructure-level)

AWS IaaS Services:-
⚡ Compute
EC2 (Elastic Compute Cloud – virtual servers)
EC2 Auto Scaling (automatic scaling of servers)
Elastic Load Balancer (ELB) (distribute traffic)
💾 Storage
EBS (Elastic Block Storage – hard disks for EC2)
EFS (Elastic File System – shared storage)
S3 (object storage)
Glacier / S3 Glacier (long-term backup)
Storage Gateway (hybrid storage between AWS & on-prem)
🌐 Networking
VPC (Virtual Private Cloud)
Elastic IPs
Direct Connect
VPN
Transit Gateway
🔒 Security & Access
IAM (Identity & Access Management)
KMS (Key Management Service)
CloudHSM
Shield, WAF
📊 Monitoring
CloudWatch (monitoring infra)
CloudTrail (logs and auditing)


🟡 2. PaaS (Platform as a Service)
👉 AWS provides infrastructure + platform (OS, middleware, runtime).
👉 We only focus on data & applications.
We Manage:-Data,Applications
AWS Manages:-Networking,Storage,Servers,Virtualization,OS,Middleware,Runtime,Security

AWS PaaS Services:-
⚡ Databases (Managed DBs)
RDS (Relational Database Service: MySQL, PostgreSQL, SQL Server, Oracle)
Aurora (AWS proprietary DB)
DynamoDB (NoSQL DB)
ElastiCache (Redis/Memcached cache service)
⚡ Application Services
Elastic Beanstalk (easy app deployment)
Lambda (serverless code execution)
API Gateway (API management)
⚡ Analytics / Integration
Kinesis (real-time streaming data)
Glue (ETL service)
EMR (Hadoop/Spark clusters, managed)

🔴 3. SaaS (Software as a Service)
👉 AWS (or vendor) provides full application ready to use.
👉 You don’t manage anything, just use the software.
You Manage:- Nothing (only use application)
AWS Manages:- Everything (Networking → Application)

AWS SaaS Services:-
WorkMail (managed email service)
Chime (video conferencing, collaboration)
QuickSight (Business Intelligence dashboards)
Connect (cloud contact center / call center solution)
Cognito (partially SaaS) (user authentication, login for apps)
Many Marketplace SaaS apps (3rd party on AWS Marketplace)

```
```
| Layer          | On-Prem | IaaS   | PaaS   | SaaS |
| -------------- | ------- | ------ | ------ | ---- |
| Applications   | You     | You    | You    | AWS  |
| Data           | You     | You    | You    | AWS  |
| Runtime        | You     | You    | AWS    | AWS  |
| Middleware     | You     | You    | AWS    | AWS  |
| OS             | You     | You    | AWS    | AWS  |
| Virtualization | You     | AWS    | AWS    | AWS  |
| Servers        | You     | AWS    | AWS    | AWS  |
| Storage        | You     | AWS    | AWS    | AWS  |
| Networking     | You     | AWS    | AWS    | AWS  |
| Security       | You     | Shared | Shared | AWS  |

```

🌐 Key Components of AWS Global Infrastructure
```
1. Regions
A Region is a geographical area where AWS has multiple data centers.
Each Region is isolated for fault tolerance and compliance.
AWS currently has 37 launched Regions with plans for more.

2. Availability Zones (AZs)
AZs are physically separate data centers within a Region.
They’re designed for high availability—if one AZ fails, thers can take over.
Each Region has at least three AZs, ensuring resilience

3. Edge Locations & regional Edge location
These are part of Amazon CloudFront, AWS’s content delivery network (CDN).
They cache content closer to users for low-latency delivery.
AWS has 700+ CloudFront Points of Presence (POPs) globally.

4. Local Zones & Wavelength Zones
Local Zones extend AWS services to metro areas for ultra-low latency.
Wavelength Zones are designed for 5G mobile edge computing.

5. Global Network Backbone
AWS uses 6+ million kilometers of fiber optic cabling to connect its infrastructure.
This ensures fast data transfer, low latency, and high throughput.

🛡️ Benefits of AWS Global Infrastructure
High Availability: Multiple AZs per Region ensure uptime.
Scalability: Easily expand across Regions and Zones.
Security & Compliance: Meets strict global standards.
Low Latency: Edge locations and local zones bring services closer to users.
```
🧠 EC2 (Elastick compute cloud):- 
```
Amazon EC2, or Elastic Compute Cloud, is a core AWS service that provides scalable virtual servers in the cloud. Instead of investing in physical hardware, EC2 lets you launch instances—virtual machines—with customizable configurations of CPU, memory, and storage.

One of its biggest strengths is scalability. You can easily scale resources up or down depending on traffic or workload, which is perfect for dynamic applications. EC2 also offers strong security features like security groups (which act as virtual firewalls), encrypted storage, and private networking through VPCs.

You can choose from pre-built Amazon Machine Images (AMIs) or create your own, giving you full control over the operating system and software stack.

Overall, EC2 is ideal for hosting websites, backend services, data processing jobs, and even gaming servers. And since it's pay-as-you-go, it's cost-efficient—you only pay for the compute time you actually use."
```

```

```
















AZ 900 - Azure Fundamentals
- Understand cloud models, Azure services, pricing, and governance.
- Estimated time: 1–2 weeks (part-time)
-------------------------------------------------------

AZ-104: Azure Administrator Associate
- Focus on identity, compute, storage, and networking.
- Helps you manage VMs, virtual networks, and resource groups that host your PostgreSQL servers.
- Estimated time: 4–6 weeks (part-time)

-----------------------------------------------------
 DP-3021: Configure and Migrate to Azure Database for PostgreSQL
- Why: Specifically designed for DBAs working with Azure PostgreSQL. Covers architecture, performance tuning, security, and migration strategies.
- Time: 1–2 days (intensive course)
- Key Skills:
- PostgreSQL architecture in Azure
- Query optimization and monitoring
- Security and encryption
- Migration from on-prem or AWS RDS to Azure

🧠 Bonus: What You’ll Learn in DP-3021
- Write-ahead logging and vacuum processes
- Query tuning with pg_stat_statements and Query Store
- Role-based access and firewall rules
- System catalogs and concurrency handling
You can explore the course details on CloudThat’s official page.

Would you like a weekly study plan combining AZ-900, AZ-104, and DP-3021? I can map it out for you based on your schedule.

🟣 Phase 3: Database Specialization
Dive deep into Azure Database for PostgreSQL Flexible Server.
- Key Topics to Learn:
- Architecture and high availability setup
- Backup and restore strategies
- Performance tuning and scaling
- Security and firewall configuration
- Maintenance windows and patching
- Integration with Azure AI and analytics tools



