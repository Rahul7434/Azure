# Azure
```
1.AZ-900 → Fundamentals
2.AZ-104 → Administration
3.AZ-500 → Security & Sentinel
4.DP-900 → Data Fundamentals
5.DP-300 → Database Administration
6.Optional: AI-900 / AZ-400 for specialization

```
### Az-900 Fundamentals

##### What is cloud:- 
```
Microsoft Azure is Microsoft's cloud computing platform that provides IT infrastructure and services over the internet.
Instead of purchasing, maintaining, and managing our own datacenters, we can rent the resources we need from Azure and pay only for what we use.

* Azure offers a wide range of services, including:
    1.Virtual Machines (VMs)
    2.Servers
    3.Networking
    4.Storage
    5.Databases
    6.Security services
    7.Analytics and AI services
    8.Application hosting
    9.Backup and disaster recovery

* The big advantages are:

Key Advantages of Azure
1. Security
Azure provides built-in security features, identity management, threat protection, encryption, and compliance with many international and industry standards.
2. High Availability
Azure uses multiple Availability Zones and Regions to ensure services remain available even if a datacenter or an entire region experiences issues.
3. Scalability
Resources can be scaled up or down instantly based on demand, allowing applications to handle varying workloads efficiently.
4. Cost Optimization
Azure follows a pay-as-you-go pricing model, which eliminates large upfront hardware investments and helps organizations pay only for the resources they consume.
5. Speed and Agility
Services can be deployed within minutes, enabling faster development, testing, and deployment without waiting for hardware procurement.
6. Global Reach
Azure has datacenters located around the world, allowing organizations to deploy applications closer to their users for better performance and lower latency.


* Historically, IT moved in stages:
      1.On-premises: Companies owned and managed all hardware.
      2.Virtualization: One physical server could host multiple systems, reducing hardware needs.
      3.Cloud computing: Infrastructure and services delivered online, flexible, scalable, and cost-efficient.
```

##### Types of Cloud:
```
🌩 Types of Cloud
Private Cloud:  
Here we manage everything ourselves — network, firewall rules, and security. It is expensive because responsibility is on us. No public network, only our own private network.

Public Cloud:  
Here Azure (or any provider) is responsible. It’s a public network, like the internet we use on mobile. Less expensive, but security is comparatively less because it’s shared.

Hybrid Cloud:  
Combination of both — some VMs and services on cloud, some on our own datacenter. We can use both together.

Multicloud:  
This means using more than one cloud provider at the same time. For example, Azure + AWS, or two private clouds, or two public clouds. Companies do this for flexibility, avoiding vendor lock-in, or using best features of each provider.

Community Cloud:  
A separate cloud infrastructure built for a specific community — like healthcare, government, or education. Only that community uses it, with rules and services tailored for them.

```


##### Cloud deployement Models:
Deployment model means how we decide to use cloud — whether private, public, hybrid, multicloud, or community.
```
Azure provides services through three main cloud models:

* IaaS (Infrastructure as a Service):
Cloud gives virtualization, storage, networking, servers.
We manage installation,patching, connectivity firewall rules, Database configuration.  azure does not provide these (os,midaleware,runtime,data,application).

* PaaS (Platform as a Service):
Cloud provides virtulization, OS (Linux, Windows), network, storage, servers, Runtime,Midaleware.
Azure handles os,patching,backups,scalling,high availability.
We focus only on building and running applications.

* SaaS (Software as a Service):
Cloud provides everything — Azure will manage everything.
We just use the software (like Office 365, Gmail, Salesforce).

```
##### Azure Global Infrastructure Hierarchy

```
Geographies:  
Large areas that usually align with a country or continent (e.g., India, Europe, US). Geographies are defined to meet data residency and compliance requirements.

Regions:  
Each geography contains multiple regions. A region is a specific location (like Central India, West Europe, East US).
  Each region is made up of one or more datacenters connected with a dedicated low-latency network.

Availability Zones:  
Within a region, there are typically 3 availability zones separated by 100–200 km (when possible).
Each zone has independent power, cooling, and networking.
  If one zone goes down, the others keep services running.

Datacenters:  
Inside each availability zone, there are multiple datacenters.
Each datacenter has racks of servers, storage, and networking equipment.
  Datacenters are connected with private fiber-optic networks for speed and redundancy.

Racks & Servers:  
At the lowest level, racks contain servers.
Each rack has its own power source, and racks are interconnected for resilience.

Corrected Hierarchy
So the full hierarchy looks like this:

Geography (country/continent)  
 → Region (specific location)  
  → Availability Zones (separate power/network zones)  
   → Datacenters (multiple buildings)  
    → Racks (servers, storage, networking)


One-Line Definition for Interviews: 
Microsoft Azure is a cloud computing platform that provides on-demand infrastructure, platforms,
and software services over the internet, enabling organizations to build, deploy, and scale applications without managing physical datacenters.
```
##### Accessing and Managing Azure Datacenters

```
Microsoft Azure has datacenters across the world. To manage these datacenters and cloud resources, Azure provides different management tools such as Azure Portal, Azure CLI, Azure PowerShell, and REST APIs.

The most common way to manage Azure resources is through the Azure Portal (portal.azure.com). We can access it from a desktop, laptop, tablet, or mobile device using an internet connection.

First, we need to create an Azure account and sign in. After creating the account, we get an Azure Subscription. The subscription is the primary unit for managing resources, billing, and costs in Azure.

Once we have a subscription, we can create and manage resources such as Virtual Machines (VMs), Storage Accounts, Databases, Virtual Networks, and many other Azure services.

The subscription is the main boundary for billing, cost management, access control, and resource management. Azure provides different subscription types, such as Free Trial and Pay-As-You-Go.

To create an Azure account, we generally need an email address and a debit or credit card for verification purposes.

In large organizations, a single subscription is usually not enough. Multiple subscriptions are created to separate Production, UAT, and Development environments or to manage resources for different teams and business units. This helps with cost tracking, access control, governance, and resource organization.

For example, one subscription may be dedicated to Production workloads, another for UAT, and another for Development, making the environment easier to manage and monitor.

Company
│
├── Production Subscription
│   ├── VMs
│   ├── Databases
│   └── Storage
│
├── UAT Subscription
│
└── Development Subscription

Each subscription has its own resources, billing, permissions, and policies, which helps organizations manage their cloud environment efficiently.

Resource Group:
A resource group is like a container in Azure.
It holds related resources for an application or project.
Example: For your entertainment app, you can keep VM, database, storage account, and networking inside one resource group.
   It makes management easy: you can monitor, apply policies, or delete everything together.

Resource:
A resource is the actual service or item you create in Azure.
Examples:
VM (Virtual Machine)
SQL Database
Storage Account
Virtual Network
App Service

Each resource belongs to a resource group.

Relationship:
Subscription → Resource Groups → Resources
Subscription is the billing account.
Resource groups organize resources.
Resources are the actual services you use.


```

#### What is a Virtual Machine (VM)?

```
A Virtual Machine (VM) is a software-based computer that runs on physical servers in a datacenter. It behaves like a real computer and has its own:

CPU
Memory (RAM)
Storage (Disk)
Operating System (Windows/Linux)
Network connectivity

Using a VM, we can install applications, databases, runtime environments, and other software just like on a physical server.

Types of Azure Virtual Machines

Azure provides different VM families based on workload requirements:

General Purpose
Balanced CPU and memory.
Suitable for web servers, small databases, and development environments.
Example: B-series, D-series.
Compute Optimized
High CPU compared to memory.
Suitable for application servers, batch processing, and gaming servers.
Example: F-series.
Memory Optimized
High memory compared to CPU.
Suitable for large databases, caching, and in-memory applications.
Example: E-series, M-series.
Storage Optimized
High disk throughput and IOPS.
Suitable for big data, data warehousing, and large transactional databases.
Example: Lsv3-series.
GPU Optimized
Includes GPUs for graphics and AI workloads.
Suitable for machine learning, deep learning, and video rendering.
Example: NC, ND, NV series.
Interview Definition

A Virtual Machine is a software-defined computer running on Azure's physical infrastructure. It provides virtualized CPU, memory, storage, and networking resources, allowing us to run Windows or Linux operating systems and host applications without managing physical hardware. Azure offers different VM families such as General Purpose, Compute Optimized, Memory Optimized, Storage Optimized, and GPU Optimized based on workload requirements


* When creating an Azure Virtual Machine, you go through several configuration screens. Here's a practical explanation of each section and the limitations you should know.

**1. Basics**
This is where you provide the basic information.

Subscription – Select the Azure subscription where the VM will be created.
Resource Group – Logical container for Azure resources.
Virtual Machine Name – Name of the VM.
Region – Azure datacenter location (e.g., Central India, East US).
Availability Options – Availability Zone, Availability Set, or no redundancy.
Image – Operating System template.
    Windows Server
    Ubuntu
    Red Hat Enterprise Linux
    CentOS
    Debian, etc.
Size – VM hardware configuration (CPU, RAM).
Authentication Type
    Password
    SSH Key (recommended for Linux)
Username – Administrator account.

**2. Disks**
Storage configuration for the VM.

OS Disk
Contains:
    Operating System
    System files
    Boot files
Disk Types:
Standard HDD
    Lowest cost
    Lower performance
    Suitable for dev/test
Standard SSD
    Better than HDD
    Moderate performance
Premium SSD
    High performance
    Suitable for production workloads
Ultra Disk
    Highest IOPS and throughput
    Enterprise databases
Data Disks
Additional disks attached to the VM for:
    Database files
    Application data
    Backups

**3. Networking**

Networking defines how the Virtual Machine (VM) communicates with other Azure resources, on-premises systems, and the internet.
a) Virtual Network (VNet)
A Virtual Network (VNet) is a private network in Azure. It allows Azure resources such as VMs, databases, and applications to communicate securely with each other.
Example:
VNet: 10.0.0.0/16

b) Subnet
A subnet is a smaller network created within a VNet to logically separate resources.
Example:
VNet: 10.0.0.0/16

├── Subnet-App : 10.0.1.0/24
└── Subnet-DB  : 10.0.2.0/24
In this example, application servers can be placed in the App subnet and database servers in the DB subnet.

c) Public IP Address
A Public IP address allows a VM to communicate with the internet and enables external users to access the VM.
Examples:
- Accessing a Linux VM using SSH
- Accessing a Windows VM using RDP
- Hosting a public website

d) Private IP Address
A Private IP address is used for communication within the Virtual Network and is not accessible directly from the internet.
Examples:
- Application server connecting to a database server
- Communication between VMs in the same VNet

e) Network Security Group (NSG)
A Network Security Group (NSG) acts as a virtual firewall that controls inbound and outbound network traffic to Azure resources.
Common NSG Rules:
- Allow SSH (Port 22) for Linux VM administration
- Allow RDP (Port 3389) for Windows VM administration
- Allow PostgreSQL (Port 5432) for PostgreSQL database access
- Allow MySQL (Port 3306) for MySQL database access
- Allow HTTP (Port 80) for web traffic
- Allow HTTPS (Port 443) for secure web traffic

Networking Components Flow:
Internet
   │
   ▼
Public IP
   │
   ▼
Network Security Group (NSG)
   │
   ▼
Virtual Network (VNet)
   │
   ├── Subnet-App (10.0.1.0/24)
   │      └── Application VM
   │
   └── Subnet-DB (10.0.2.0/24)
          └── Database VM

This networking architecture provides secure communication, network isolation, and controlled access to Azure Virtual Machines.


**4. Management**

    Additional management features.
Boot Diagnostics
    Captures boot logs and screenshots.
Auto Shutdown
    Automatically shuts down VMs.
Backup
    Enables Azure Backup.
Monitoring
    Integrates with Azure Monitor and Log Analytics.


**5. Monitoring**

Collects performance metrics.
Examples:
CPU usage
Memory utilization
Disk I/O
Network traffic


**6. Advanced**

    Additional customization.
Custom Data
    Startup scripts executed during VM creation.

Extensions:
Install software automatically:
Azure Monitor Agent
Antimalware
Custom Script Extension

**7. Tags**
Key-value pairs for organization.

Example:
    Environment = Production
    Owner = DBA Team
    Project = ERP
Useful for:
    Cost tracking
    Automation
    Reporting
----------------

**Common Limitations of Virtual Machines (VMs)**

1. Cost
   - Larger VM sizes cost more.
   - Premium storage and additional services increase the overall cost.

2. Resource Limits
   Each VM size has fixed resource allocations:
   - CPU (vCPUs)
   - RAM (Memory)
   - Disk Throughput
   - Network Throughput

3. Scaling Limitations
   Scaling may require:
   - VM Resize
   - VM Restart or Downtime
   - Migration to a larger VM size

4. Single VM Failure
   Without high-availability configurations such as:
   - Availability Zones
   - Availability Sets
   - Load Balancers

   A single VM can become a Single Point of Failure (SPOF).

5. Operating System Management
   The customer is responsible for:
   - OS Patching
   - Security Updates
   - Antivirus Installation and Management
   - User and Access Management
   - Application Maintenance

6. Storage Limits
   Each VM size supports a limited number of:
   - Data Disks
   - Disk Capacity
   - Disk Throughput

7. Performance Limits
   Each VM size has maximum limits for:
   - IOPS (Input/Output Operations Per Second)
   - Network Bandwidth
   - Disk Throughput
   - CPU Utilization

8. Backup and Disaster Recovery
   - Backups are not automatically configured.
   - Backup and DR solutions must be planned and managed separately.

9. Security Responsibility
   Users must manage:
   - Firewall Rules
   - NSG Rules
   - OS-Level Security
   - Access Controls
   - Compliance Requirements

10. Maintenance Impact
   - Azure platform maintenance may require VM reboot in some scenarios.
   - Application availability planning is required for critical workloads.

11. Licensing Costs
   Additional licensing costs may apply for:
   - Windows Server
   - SQL Server
   - Third-party software

12. Monitoring and Management
   - Monitoring is not fully configured by default.
   - Azure Monitor, Log Analytics, and alerts should be configured for production workloads.


 Summary:
While creating an Azure VM, we configure the subscription, resource group, region, operating system image, VM size,
authentication method, disks, networking, monitoring, and management settings. We select the VM size based on CPU and memory requirements, choose appropriate disk types based on performance needs, configure networking using VNets and NSGs, and enable monitoring and backup features. Key limitations include cost, resource limits, storage constraints, performance caps,
and the need to manage the operating system and security updates ourselves.

```

#### High Availability

```
1. Availability Set
2. Availability Zone
3. Availability Scale Set

Azure infrastructure is organized as Geography → Region → Availability Zone → Datacenter → Rack → Server.
A Region can contain multiple Availability Zones. Each Availability Zone has independent power, cooling, and networking.

Inside datacenters, servers are organized into racks.
An Availability Set distributes VMs across different Fault Domains and Update Domains, protecting against rack failures and maintenance events within the same datacenter.

If an entire datacenter goes down, Availability Sets cannot help. To protect against datacenter failures, Azure provides Availability Zones, where VMs are deployed across physically separate datacenters in the same region.

VM Scale Sets are used to automatically create, remove, and manage multiple identical VMs based on demand, while also supporting distribution across Fault Domains and Availability Zones for high availability.
Your overall understanding is about 80–85% correct. The main thing to fix is:
"VM assigned to line 1, VM assigned to line 2" = Availability Set (Fault Domains), not Scale Set.


```




