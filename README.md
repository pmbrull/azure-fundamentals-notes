# Azure Fundamentals Notes

Notes for the course [Azure Fundamentals](https://docs.microsoft.com/en-us/learn/paths/azure-fundamentals/). Both content and images are extracted from there.

## Principles of Cloud Computing

<details>
<summary> 
Show content
</summary>
<p>

### Learning Objectives

* Common cloud computing services
* Benefits of cloud computing
* Cloud deployment model

### What is cloud computing?

It's a resource rental based on a pay per use approach, abstracting the hardware from the users.

### Cloud Computing Services

#### Compute Power

It is the processing capability offered by cloud-based servers. Depending on our needs, we can chose among three different options:

* **Virtual Machines (VM)**: You are provided the hardware and the OS, but have to control and maintain the rest of the software. This VM will run on a physical server based on a datacenter and overall resources will be shared with other VMs in an isolated and secure fashion.

* **Containers**: Such as Docker, offer an independent, consistent and isolated execution environment for applications. They do not require any OS - as they just contain the minimum dependencies to run the app - they are easy and fast to spin up, move to a different machine and scale.

* **Serverless Computing**: Is the ability to run an application without creating, configuring nor maintaining a server. By breaking the whole application into smaller pieces, we can define a workflow and a set of triggers to execute the different parts of the application.

As per **pricing**, with VMs and Containers, we pay for as long the server is up, eventhough the application is idle. With Serverless Computing though, you only pay for the processing time of each function.

![img](./assets/principles-of-cloud-computing/vm-vs-container-vs-serverless.png)

#### Storage

If you either need to store a file or use a database, cloud providers offer the possibility to scale the storage as per your needs.

#### Summary

As requirements vary among all the processes and services business needs to offer, cloud computing is a **flexible** and **cost-efficient** solution to both small or big companies.

### Benefits of Cloud Computing

* **Cost-Effective**: with a pay-as-you-go model you don't need to make huge upfronts investments to start offering your services. Moreover, you don't need to manage any kind of infrastructure, freeing people to focus on other tasks.

* **Scalable**: It's easy to increase / decrease the resources used either manually or automatically.
    * *Vertical Scaling* or *scaling up* can be used to increase the power of an existing machine.
    * *Horizontal Scaling* or *scaling out* adds more servers to function together as a unit.

* **Elastic**: Can automatically adapt to workload changes by adding or removing resources.

* **Current**: By removing the need of managing hardware and other IT tasks, you can focus on just building and deploying your apps.

* **Reliable**: As it offers backups, disaster recovery and data replication services to make sure that your data is always safe. If on top you follow redudancy on your architectures you can avoid single points of failure.

* **Global**: With datacenters all over the globe, you can have presence close to your customers and reduce response time.

* **Secure**: Offering policies, technologies and controls.

### Compliance terms and requirements

Cloud providers should also help when complying with regulations and standards such as GDPR.

### Economies of Scale

The ability to do things at a lower cost per unit when operating at a larger scale.

### Capital expenditure (CapEx) versus operational expenditure (OpEx)

* **Capital Expenditure (CapEx)**: Spending of money on physical infrastructure up front, and then deducting that expense from your tax bill over time. This is the example of on-premise servers, where one needs to pay for server, storage, network, backup, disaster recovery and general infrastructure costs for both software and hardware plus the technical personnel.

* **Operational Expenditure (OpEx)**: Spending money on services or products now and being billed for them now. With cloud computing we can access to more customized features as we're not sharing the same framework for everyone. Charges are scalable based on usage rather than having a fixed capacity and the billing can directly by focused to a user or organization level.

![img](./assets/principles-of-cloud-computing/capexvsopex.png)

### Cloud deployment models

A cloud deployment model defines where the data is stored and how customers interact with it.

* **Public Cloud**: No local hardware - everything runs on the cloud provider. It implies the following **advantadges**:
    * Scalability and agility, as you just rent more hardware when needing it.
    * Pay-as-you-go pricing: no CapEx.
    * No need for hardware maintenance.
    * Minimal technical knowledge to set up and use.

    However, there also are some **disadvantages**:
    * Maybe you are not able to manage the hardware as you'd want.
    * It's possible that some security requirements, policies or standards that cannot be met.
    * Unique business requirements - such as maintaining a legacy application - might be hard to meet.

* **Private Cloud**: You set up the whole datacenter, access policies and resources in the organization. This has some **advantages**:
    * You can configure it so that it's possible to maintain any legacy app.
    * Full control (and responsability) over security.
    * Easier to meet security, policy and standards.

    The **disadvantages** would be:
    * Initial CapEx costs.
    * Limited agility.
    * High IT skills.

* **Hybrid Cloud**: Combination of Public and Private clouds, which brings both worlds advantages which may be benefitial for some applications or configurations but also can end up being more expensive and hard to manage.

### Types of Cloud Services

* **IaaS**: Most flexible category, giving full control on the hardware that runs the app.
    > **Shared repsonsibility model**: Ensuring that a service is running is a shared responsibility between the cloud provider (in charge of the infrastructure) and the customer (who needs to set up the proper configurations).
    This is the usual scenario when migrating workloads - as you can mimic on-premise setup, testing and deployment for new apps and for storage, backup and recovery.

* **PaaS**: Provides an environment for building, testing and deploying software applications, where one does not need to care about the underlying infrastructure. It is useful as it brings a framework that developers can work upon and also for analytics or BI tasks.

* **SaaS**: Software hosted and managed for the customer, who acts as end user.

![img](./assets/principles-of-cloud-computing/responsibility.png)


### Knowledge Check

1. Which term from the list below would be viewed as benefits of using cloud services?

* Unpredictable costs
* Elasticity
* Local reach only

    <details>
    <summary> 
    Answer
    </summary>
    <p>
    Elasticity: Elasticity, Agility and Economies of scale are the correct answers, and would be seen as benefits that you can gain from using cloud services.
    </p>
    </details>


2. Suppose you have two types of applications: legacy applications that require specialized mainframe hardware and newer applications that can run on commodity hardware. Which cloud deployment model would be best for you?


* Public cloud
* Private cloud
* Hybrid cloud

    <details>
    <summary> 
    Answer
    </summary>
    <p>
    Hybrid cloud: A hybrid cloud is a public and private cloud combined. You can run your new applications on commodity hardware you rent from the public cloud and maintain your specialized mainframe hardware on-premises.
    </p>
    </details>

3. You're developing an application and want to focus on building, testing, and deploying. You don't want to worry about managing the underlying hardware or software. Which cloud service type is best for you?

* Infrastructure as a Service (IaaS)
* Platform as a Service (PaaS)
* Software as a Service (SaaS)


    <details>
    <summary> 
    Answer
    </summary>
    <p>
    Platform as a Service (PaaS): Platform as a Service is the best choice here because the PaaS services handle the IT management tasks for you, so you can focus on writing code.
    </p>
    </details>

</p>
</details>

---

## Introduction to Azure

<details>
<summary> 
Show content
</summary>
<p>

### Learning Objectives

* What Microsoft Azure is.
* Deploy and configure a web server.
* Learn how to scale up your server.
* Interact with the web server using Azure Cloud Shell.

### Tour of Azure services

Azure is Microsoft's cloud computing platform.

![img](./assets/introduction-to-azure/azure-services.png)

It offers a lot of services of different nature:

* **Compute**: helping in hosting applications and services.
* **Networking**: for linking resources and providing access to applications.
* Four main types of **storage**: Blob storage, File storage, Queue storage and Table storage (NoSQL store).
* **Mobile**: to create services for iOS, Android an Windows.
* **Databases** with global connectivity.
* Building and hosting **Web** applications.
* **IoT** data gathering and analysis.
* Analytics solutions for **Big Data**.
* **AI**: helping with creating and deploying ML models.
* **DevOps** services for building, testing and releasing your applications.

### Exercise - Create a website hosted in Azure

> In this section, it is useful to directly access Azure course and work with the given [sandbox](https://docs.microsoft.com/en-us/learn/modules/welcome-to-azure/4-exercise-create-website). It does not charge your subscription.

* **App Service**: HTTP-based service that enables you to build many types of web-based solutions without managing the infrastructure. With an App Service Plan we specify the compute resources and location for the web app.

* **Azure Marketplace**: Online store that hosts certified and optimized applications to run in Azure, for example Wordpress in an App Service.

### Exercise - Configure an App Service

> In this section, it is useful to directly access Azure course and work with the given [sandbox](https://docs.microsoft.com/en-us/learn/modules/welcome-to-azure/5-exercise-configure-app-service). It does not charge your subscription.

By looking at the performance graphs we can check if we need to perform any changes on the configuration of our app. When **scaling** a webb app, we could add network bandwidth, memory, storage or compute power.

> **Azure Advisor** and **Azure Cost Management** are two services that help you optimize cloud spend. You can use these services to identify where you're using more than you need, and then scale back to the capacity you're actually using.

Finally, notice that there are three categories of configurations plans to make it easier to define our setup for dev, prod or isolated workloads.

> **Isolated**:	This category is ideal for workloads that require advanced networking and fine-grained scaling.

### Exercise - Access an App Service using Azure Cloud Shell

> In this section, it is useful to directly access Azure course and work with the given [sandbox](https://docs.microsoft.com/en-us/learn/modules/welcome-to-azure/6-exercise-cloud-shell). It does not charge your subscription.

**Azure Cloud Shell** is a browser-based command-line experience for managing and developing Azure resources


### Knowledge Check

1. What is Azure?

* Microsoft's cloud computing platform, which provides compute power, storage, and services over the Internet using a pay-as-you-go pricing model.
* A single data center located in Redmond, Washington.
* A hosting environment specifically for virtual machines

    <details>
    <summary> 
    Answer
    </summary>
    <p>
    Microsoft's cloud computing platform, which provides compute power, storage, and services over the Internet using a pay-as-you-go pricing model: Azure provides raw compute power and storage, as well as services to help you explore new software paradigms such as intelligent bots and mixed reality. 
    </p>
    </details>


2. Which of the following is an example of an Azure application platform?

* Azure App Service
* Azure Load Balancer
* Azure Table Storage
* Azure Cache for Redis

    <details>
    <summary> 
    Answer
    </summary>
    <p>
    Azure App Service: Azure App Service is an HTTP-based service that enables you to build and host many types of web-based solutions without managing infrastructure. 
    </p>
    </details>

3. When should you scale out your deployment?

* When your application or service requires a more powerful CPU or more memory to run faster.
* When you need additional virtual machines to speed up your application.
* When you're using excess capacity that you don't need.

    <details>
    <summary> 
    Answer
    </summary>
    <p>
    When you need additional virtual machines to speed up your application: Scaling out means adding additional systems, such as virtual machines. For example, you might create many virtual machines configured in the same way and use a load balancer to distribute work across them. 
    </p>
    </details>


</p>
</details>

---

## Core Cloud Services - Azure architecture and service guarantees

<details>
<summary> 
Show content
</summary>
<p>

### Learning Content

* Physical infrastructure of Azure.
* Understand the service level agreements provided by Azure.
* Learn how to provide your own service level agreement for your apps.

### Datacenters and Regions

Cloud providers are built upon datacenters around the globe, where the physical hardware is located.

**Regions** are geographical areas on the planet containing +1 datacenter. This partition into regions gives flexibility to provide services which are close - and thus ensure lower latency - to the user.

### Geographies

Azure divides the world into **geographies** that are defined by geopolitical boundaries. Each geography preserve data residency and compliance needs required by those countries. Moreover, they are fault-tolerant to withstand complete region failure. We have the following geographies:

* Americas
* Europe
* Asia Pacific
* Middle East and Africa

Each region belongs to a single geography and has specific service availability, compliance, and data residency/sovereignty rules applied to it

### Availability Zones

To avoid single points of failure, cloud providers can help us create highly available applications through **Availability Zones**, which are separate datancenters within a region isolated from each other. If one zone goes down, the others keep working. The idea is that we can locate the resources in a zone and replicate in another.

There are two types of services that support AZs:
* Zonal Services: where the resource is pinned to a specific zone (e.g., a VM)
* Zone-redundant Services: where the platform automatically replicates services accross zones (e.g., zone-redundant storage or SQL databases)

### Region Pairs

Availability zones are created using 1+ datacenters, and there is a minimum of three zones within a single region. To ensure that services can still be provided even if two datacenters go down, Azure created Region Pairs.

Region Pairs are two region in the same geography but at least 300 miles away, which helps replicating resources accross the same geography and ensuring availabilty even in case of disaster. They are used to provide reliable services and data redudancy (geo-redundant).

### Service-Level Agreements

Formal documents called Service-Level Agreements (SLAs) capture the specific terms that define the performance standards that apply to Azure. These documents are specific for individual services and define what happens if a products fails to perform.

There are three key characteristics of SLAs:

* **Performance Targets**: such as uptime guarantees or connectivity rates.
* **Uptime and Connectivity Guarantees**: which usually specify from 99.9% performance target commitment to 99.999%.
* **Service Credits**: describing how Microsoft will respond if a service fails to perform its governing SLA's specification.

### Compose SLAs accross services

Combining SLAs from different services results in a *Composite SLA*. We can calculate this with probability calculus.

For example having a Web App (99.95%) that redirects trafic to either a DB (99.99%) or a Queue (99.9%) gives us:

* If the probability that both DB and queue are up is `1.0 − (0.0001 × 0.001) = 99.99999%`
* Then, the composite SLA ends up as

```bash
99.95 × 99.99999 = ~99.95%
```

### Improve your app reliability

*Application SLA* is the creation of your own SLA based on the workloads and services. We need to know our business requirements to provide a solution that best suits an overall SLA considering all components.

Although rare, we also need to plan for entire service disruption. Here we have important aspects such as **Resiliency**, the ability of a system to recover from failures and continue to function. High availability and disaster recovery are two crucial components of resiliency. Howeher, the higher availability we want our application to be, the more expensive it will get as it will require more resources. This will also make it more complex in the overall architecture.


### Knowledge Check

1. Deploying an app can be done directly to what level of physical granularity? 

* Region
* Datacenter
* Server rack

    <details>
    <summary> 
    Answer
    </summary>
    <p>
    Region: Azure organizes infrastructure around regions, which include multiple datacenters. You can pick the region you want resources deployed into. You can't select a specific datacenter or location within a datacenter.
    </p>
    </details>


2. To use Azure datacenters that are made available with power, cooling, and networking capabilities independent from other datacenters in a region, choose a region that supports _________?

* Geography distribution
* Service-Level Agreements (SLAs)
* Availability Zones

    <details>
    <summary> 
    Answer
    </summary>
    <p>
    Availability Zones: Availability Zones are datacenters set up to be an isolation boundary from others in the region, with their own power, cooling, and networking. If one zone in a region goes down, other Availability Zones in the region continue to work. 
    </p>
    </details>

3. Application availability refers to what?

* The service level agreement of the associated resource.
* Application support for an availability zone.
* The overall time that a system is functional and working.

    <details>
    <summary> 
    Answer
    </summary>
    <p>
    The time that a system is working is referred to as the application availability.
    </p>
    </details>


</p>
</details>

---

## Create an Azure Account

<details>
<summary> 
Show content
</summary>
<p>


### Accounts and subscriptions

An **Azure account** is an identity in either Azure Active Directory (Azure AD), or a directory that is trusted by Azure AD, such as a work or school organization. It holds information such as:

* Name, email, and contact preferences
* Billing information such as a credit card

You use an Azure account to sign in to the Azure website and administer or deploy services. Every Azure account is associated with one or more subscriptions.

An **Azure subscription** is a logical container used to provision resources in Azure and is associated with Azure AD.

There are four different subcription types:

* Free
* Pay-As-You-Go
* Enterprise Agreement
* Student

### When to use multiple Azure subscriptions

Sometimes it is useful to separate resources at a subcription level, as **billing** and **access control** happen at the subscription. We could use this to separate DEV and PROD environments for billing and security reasons or even to isolate some resources for compliance.

Also, note that one could also transfer a subscription from one billing account to another.

### Authenticate access with Azure Active Directory

Azure AD is a modern identity provider that supports multiple authentication protocols. It is partitioned into separate **tenants**, which are dedicated and isolated instances of the Azure Active Directory service, owned and managed by an organization. A tenant may have multiple subscriptions (in a trust relationship), but a subscription only belongs to one tenant.

![./assets/azure-account/4-azure-ad-tenant.png]

Notice that each Azure AD tenant has an account owner. This is the original Azure account that is responsible for billing. You can add additional users to the tenant, and even invite guests from other Azure AD tenants to access resources in subscriptions.

### Knowledge Check

1. Which of the following defines an Azure subscription correctly?

* Using Azure does not require a subscription
* All Azure subscriptions are always free
* An Azure subscription is a logical unit of Azure services that is linked to an Azure account
* An account cannot have more than one subscription


    <details>
    <summary> 
    Answer
    </summary>
    <p>
     An Azure subscription is a logical unit of Azure services that is linked to an Azure account: Using Azure requires an Azure subscription. Azure offer free and paid subscription options to suit different customer needs and requirements, and an account can have one or more subscriptions, with different billing models and access-management policies applied to each . A subscription provides authenticated and authorized access to Azure products and services, and allows you to provision resources.
    </p>
    </details>


2. True or False. Azure has free services you can use once you have an Azure subscription.

* True - there are several free services available.
* False - services are only free for the first 12 months.


    <details>
    <summary> 
    Answer
    </summary>
    <p>
     True: Azure has several free services you can use including Azure App Services, Functions, and Azure Kubernetes containers.
    </p>
    </details>

3. Billing in Azure is ______________

* Annually for each Azure account based on usage.
* Monthly for each Azure subscription based on usage.
* Monthly for each Azure account based on usage.
* Daily for each Azure subscription based on usage.


    <details>
    <summary> 
    Answer
    </summary>
    <p>
    Billing is performed monthly for each subscription in the account, based on the resource usage.
    </p>
    </details>

</p>
</details>

---

## Core Cloud Services - Manage services with the Azure portal

<details>
<summary> 
Show content
</summary>
<p>

### Azure management options

There is a broad selection of tools that can be used to configure and manage Azure.


* **Azure portal** for interacting with Azure via a Graphical User Interface (GUI). It uses a **blades model** for navigation, where a blade is a slide-out panel containing the UI for a single level in a navigation sequence. The initial dashboard can be configured with a tile system to show the resources or metrics that the user is interested in the most. Dashboards can be created, cloned or deleted and configured using the *dashboard.json* file.
* **Azure PowerShell** and Azure Command-Line Interface (CLI) for command line and automation-based interactions with Azure.
* **Azure Cloud Shell** for a web-based command-line interface.
* **Azure mobile app** for monitoring and managing your resources from your mobile device.

Moreover, it is good to know that one can use preview resources (by searching for "preview") and get notified about General Availability (GA) releases in the "What's new" link.

### Knowledge Check

1. An Azure dashboard is stored as which type of file?

* XML
* JSON
* PNG

    <details>
    <summary> 
    Answer
    </summary>
    <p>
    Azure dashboards are stored as JSON files, which allow them to be uploaded and downloaded to share with other members of the Azure directory.
    </p>
    </details>

2. Azure Advisor provides advice on which of these topics:

* Creating an Azure account
* Best practices and security for your services
* Using the Azure portal effectively

    <details>
    <summary> 
    Answer
    </summary>
    <p>
    Azure Advisor is a free service built into Azure that provides recommendations on high availability, security, performance, and cost.
    </p>
    </details>


3. True or false: Azure Cloud Shell is an interactive, browser-accessible shell for managing Azure resources?

* True
* False

    <details>
    <summary> 
    Answer
    </summary>
    <p>
    Azure Cloud Shell is an interactive shell for managing Azure resources. You can control and administer all of your Azure resources in the current subscription through a command-line interface built right into the portal.
    </p>
    </details>


</p>
</details>

---

## Core Cloud Services - Azure compute options

<details>
<summary> 
Show content
</summary>
<p>

### Learning objectives

* Identify compute options in Azure.
* Select compute options that are appropriate for your business.

### Essential Azure compute concepts

Azure compute is an on-demand computing service for running cloud-based applications in the form of:

* **Virtual Machines**: software emulations of physical computers. They include a virtual processor, memory, storage and networking resources. They need to run on an OS.
* **Containers**: virtualization environment for running applications. They do not need any OS, instead they just include the minimum necessary dependencies to run the application and use the existing host OS running the container.
* **App Service**: PaaS offering in Azure designes to host web-oriented applications.
* **Serverless Computing**: is a cloud-hosted execution environment that runs your code but abstracts the underlying hosting environment.

### Explore Azure Virtual Machines

They are a useful choice when we need
* Total control over the operating system (OS)
* The ability to run custom software, or
* To use custom hosting configurations

Some use examples could be during testing and development, when running applications in the cloud without the need of creating the infrastructure, when extending your datacenter to the cloud or during disaster recovery to being able to run business critical applications.

Moreover, when migrating to the cloud, you could use a full IaaS approach to "lift and shift" your applications, copying your physical server configurations.

#### Scaling VMs

Grouping VMs together can bring the benefits of high availability, scalability and redundancy:
* **Availability sets**: logical grouping of two or more VMs to keep applications up during maintenance. This could mean that some patches or upgrades needed to be done on the machine (planned maintenance) or due to hardware failure in the datacenter (unplanned maintenance). The group of VMs that share common hardware are in the same *fault domain* - rack of servers.

    With an availability set you get up to three fault domains that each have a server rack with dedicated power and network resources and five logical update domains, which indicate the group of VMs that are being rebooted / patched at the same time.

    ![img](./assets/azure-compute-options/availability-sets.png)

* **Scale sets**: let you create and manage a group of identical, load balanced VMs in order to provide high availability apps and increase / decrease the number of VMs depending on demand.

* **Azure Batch**: enables large-scale job scheduling and compute management with the ability to scale to tens, hundreds or thousands of VMs. Batch starts a pool of VMs, installs applications and staging data, runs the jobs, identifies failures and requeues works, scales down the pool as work completes.

### Explore Containers in Azure

Azure supports Docker containers. There are several ways to manage containers in Azure:

* **Azure Container Instances (ACI)**: PaaS offering that allows to upload the containers and execute them directly with automatic elastic scale.
* **Azure Kubernetes Service (AKS)**: Complete orchestration service (automating, managing and interacting) for containers with distributes architectures with multiple containers.

Containers are often used to create solutions using a **microservice architecture**. This architecture is where you break solutions into smaller, independent pieces, which allows to scale and upgrade the differents parts independently.

### Explore Azure App Service

PaaS service that allows you to focus on the website and API logic while Azure handles the infrastructure to run and scale your web applications. You pay for the resources used by processing depending on the App Service Plan chosen, which determines how much hardware is devoted to your host.

There are different types of web apps:

* **Web Apps**: which supports web app hosting.
* **API Apps**: you can build REAS-based Web APIs with Swagger support and the ability to package and publish your API in the Azure Marketplace.
* **Web Jobs**: allow you to run a program or scripts in the same context as a web app,API app or mobile app. They can be scheduled or run by a trigger.
* **Mobile app back-ends**: lets one quickly build the backend for iOS or Android apps. You can store mobile app data in cloud DBs, authenticate customers, send push notifications and execute custom backend logic.

### Explore Serverless computing in Azure

Serverless computing encompasses three ideas:
* **Abstraction of servers**: where you simply deploy your code which then runs with high availability.
* **Event-driven scale**: Which is an excellent fit for workloads that respond to events. The platform automatically scales. Events can be defined by a variety of triggers.
* **Micro-billing**: Where you pay only for the time that your code is running.

Azure has two implementations of serverless compute:

* **Azure Functions**: which can execute code in almost any modern language. Furthermore, Azure Functions can be either stateless (the default) where they behave as if they're restarted every time they respond to an event), or stateful (called "Durable Functions") where a context is passed through the function to track prior activity.
* **Azure Logic Apps**: which execute workflows designed to automate business scenarios based on an event. They can be defined via UI or JSON files. While Azure Functions can run locally, Logic Apps only run in the cloud.

### Kwnowledge Check


1. Suppose you have an existing application running locally on your own server. You need additional capacity but prefer to move to Azure instead of buying upgraded on-premises hardware. Which compute option would likely give you the quickest route to getting your application running in Azure?

* Serverless computing
* Containers
* Virtual machines


    <details>
    <summary> 
    Answer
    </summary>
    <p>
    You have full control over the VM setup, so you can configure it to match your on-premises server. This control will allow your existing application to run on the Azure VM with little or no change.
    </p>
    </details>

2. Imagine that you work on a photo-sharing application that runs on millions of mobile devices. Demand is unpredictable because you see a spike in usage whenever a locally or nationally significant event occurs. Which Azure compute resource is the best match for this workload?

* Serverless computing
* Containers
* Virtual machines

    <details>
    <summary> 
    Answer
    </summary>
    <p>
    The photo-sharing app is event driven and needs to handle unpredictable demand. Serverless computing is a good fit for this situation because it is event-based and can scale instantly to process spikes in traffic. It should also be a cost-effective choice because you will pay for compute time only when processing user data.
    </p>
    </details>


3. The compute options give you different levels of control over the configuration of the environment in which your application runs. Which of the following lists the compute options in order from "most control" to "least control"?

* Serverless computing, containers, virtual machines
* Containers, serverless computing, virtual machines
* Virtual machines, containers, serverless computing


    <details>
    <summary> 
    Answer
    </summary>
    <p>
    Virtual machines give you full control over the environment. Containers give you limited control. Serverless computing does not allow you to do any infrastructure configuration.
    </p>
    </details>

</p>
</details>

---