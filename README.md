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
👉 Each region is made up of one or more datacenters connected with a dedicated low-latency network.

Availability Zones:  
Within a region, there are typically 3 availability zones separated by 100–200 km (when possible).
Each zone has independent power, cooling, and networking.
👉 If one zone goes down, the others keep services running.

Datacenters:  
Inside each availability zone, there are multiple datacenters.
Each datacenter has racks of servers, storage, and networking equipment.
👉 Datacenters are connected with private fiber-optic networks for speed and redundancy.

Racks & Servers:  
At the lowest level, racks contain servers.
Each rack has its own power source, and racks are interconnected for resilience.

🔑 Corrected Hierarchy
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







