---
layout: post
title: AZ-900 Microsoft Azure Fundamentals
description: This blog post is a collection of thoughts and materials used in preparation for the AZ-900 Azure Fundamentals Certification offered by Microsoft. It covers the concepts of computing in the cloud in relation to the products offered by Microsoft Azure.
tags: [azure,certification,fundamentals,cloud]
---

# AZ-900 Microsoft Azure Fundamentals

The AZ-900 Azure Fundamentals is a certification from Microsoft that validates the knowledge of basic cloud computing concepts in relation to Microsoft Azure. The test checks on the candidates skills related to the following topics with different score percentages:

1. Describe Cloud Concepts (20-25%)
2. Describe Core Azure Services (15-20%)
3. Describe core solutions and management tools on Azure (10-15%)
4. Describe general security and network security features (10-15%)
5. Describe identity, governance, privacy, and compliance features (20-25%)
6. Describe Azure cost management and Service Level Agreements (10-
15%)

This post is created to serve as a study guide based on the study guideline provided by Microsoft certification updated November 9, 2020. The content in this post contains summarized content from [Microsoft Learn](https://docs.microsoft.com/en-us/learn) or [Microsoft Documentation](https://docs.microsoft.com/en-us/azure/) to allow easier content revision for the certification. It does not contain all the information in the subjects. The [Microsoft Learn](https://docs.microsoft.com/en-us/learn) or [Microsoft Documentation](https://docs.microsoft.com/en-us/azure/) should be use for formal learning into the topics.

The content is a not a comprehensive list and the test might include items that are not listed. The questions asked in the test should center around Azure features that are General Availability (GA). But Preview features might be covered if those features are commonly used at the time of the test.

## Describe Cloud Concepts (20-25%)

### Identify the benefits and considerations of using cloud services

1. identify the benefits of cloud computing, such as High Availability, Scalability, Elasticity, Agility, and Disaster Recovery [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/intro-to-azure-fundamentals/what-is-cloud-computing)

   * High Availability: Depending on the service-level agreement that you choose, your cloud-based applications can provide a continuous user experience with no apparent downtime even when things go wrong. 
   * Scalability: Applications in the cloud can be scaled in two ways, while taking advantage of autoscaling:
     * Vertically: Computing capacity can be increased by adding RAM or CPUs to a virtual machine.
     * Horizontally: Computing capacity can be increased by adding instances of a resource, such as adding more virtual machines to your configuration.
   * Elasticity: Cloud-based applications can be configured to always have the resources they need. Applications can be configured to scale up or down resources based on resource loads
   * Agility: Cloud-based resources can be deployed and configured quickly as your application requirements change. Cloud computing providers have ready made compute resource hardware that can be provisioned without the new to wait for hardware to be purchased when resource demands increased.
   * Geo-distribution: Applications and data can be deployed to regional datacenters around the globe, so your customers always have the best performance in their region.
   * Disaster Recovery:  By taking advantage of cloud-based backup services, data replication, and geo-distribution, you can deploy your applications with the confidence that comes from knowing that your data is safe in the event that disaster should occur.
  
2. identify the differences between Capital Expenditure (CapEx) and Operational Expenditure (OpEx) [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/fundamental-azure-concepts/benefits-of-cloud-computing)
   * Capital Expenditure (CapEx): up-front spending of money on physical infrastructure, and then deducting that up-front expense over time. The up-front cost from CapEx has a value that reduces over time.
   * Operational Expenditure (OpEx): spending money on services or products now, and being billed for them now. You can deduct this expense in the same year you spend it. There is no up-front cost, as you pay for a service or product as you use it.
  
3. describe the consumption-based model [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/fundamental-azure-concepts/benefits-of-cloud-computing)
   Cloud service providers operate on a consumption-based model, which means that end users only pay for the resources that they use. Whatever they use is what they pay for.

   A consumption-based model has many benefits, including:
   * No upfront costs.
   * No need to purchase and manage costly infrastructure that users might not use to its fullest.
   * The ability to pay for additional resources when they are needed.
   * The ability to stop paying for resources that are no longer needed.

### Describe the differences between categories of cloud services 

1. describe the shared responsibility model [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/intro-to-azure-fundamentals/what-is-cloud-computing)
   The shared responsibility model describes the division of responsibilities in the creation and upkeep of a computing system between the owner of the application and the provider of the cloud computing resources based on the category of cloud services selected.
   ![Azure shared responsibility model](/assets/pages/2021-04-07-az-900-azure-fundamentals-preparation/shared-responsibility.png)

2. describe Infrastructure-as-a-Service (IaaS) [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/fundamental-azure-concepts/categories-of-cloud-services)
   IaaS is the most flexible category of cloud services. It aims to give you complete control over the hardware that runs your application. Instead of buying hardware, with IaaS, you rent it.

   **Advantages**
   * No CapEx. Users have no up-front costs.
   * Agility. Applications can be made accessible quickly, and deprovisioned whenever needed.
   * Management. The shared responsibility model applies; the user manages and maintains the services they have provisioned, and the cloud provider manages and maintains the cloud infrastructure.
   * Consumption-based model. Organizations pay only for what they use and operate under an Operational Expenditure (OpEx) model.
   * Skills. No deep technical skills are required to deploy, use, and gain the benefits of a public cloud. Organizations can use the skills and expertise of the cloud provider to ensure workloads are secure, safe, and highly available.
   * Cloud benefits. Organizations can use the skills and expertise of the cloud provider to ensure workloads are made secure and highly available.
   * Flexibility. IaaS is the most flexible cloud service because you have control to configure and manage the hardware running your application.

3. describe Platform-as-a-Service (PaaS) [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/fundamental-azure-concepts/categories-of-cloud-services)
   This cloud service model is a managed hosting environment. The cloud provider manages the virtual machines and networking resources, and the cloud tenant deploys their applications into the managed hosting environment.

   **Advantages**
   * No CapEx. Users have no up-front costs.
   * Agility. PaaS is more agile than IaaS, and users don't need to configure servers for running applications.
   * Consumption-based model. Users pay only for what they use, and operate under an OpEx model.
   * Skills. No deep technical skills are required to deploy, use, and gain the benefits of PaaS.
   * Cloud benefits. Users can take advantage of the skills and expertise of the cloud provider to ensure that their workloads are made secure and highly available. In addition, users can gain access to more cutting-edge development tools. They can then apply these tools across an application's lifecycle.
   * Productivity. Users can focus on application development only, because the cloud provider handles all platform management. Working with distributed teams as services is easier because the platform is accessed over the internet. You can make the platform available globally more easily.

   **Disadvantage**
   * Platform limitations. There can be some limitations to a cloud platform that might affect how an application runs. When you're evaluating which PaaS platform is best suited for a workload, be sure to consider any limitations in this area.

4. describe serverless computing [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/fundamental-azure-concepts/categories-of-cloud-services)
   Like PaaS, serverless computing enables developers to build applications faster by eliminating the need for them to manage infrastructure. With serverless applications, the cloud service provider automatically provisions, scales, and manages the infrastructure required to run the code. Serverless architectures are highly scalable and event-driven, only using resources when a specific function or trigger occurs.

   It's important to note that servers are still running the code. The "serverless" name comes from the fact that the tasks associated with infrastructure provisioning and management are invisible to the developer. This approach enables developers to increase their focus on the business logic, and deliver more value to the core of the business. Serverless computing helps teams increase their productivity and bring products to market faster, and it allows organizations to better optimize resources and stay focused on innovation.

5. describe Software-as-a-Service (SaaS) [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/fundamental-azure-concepts/categories-of-cloud-services)
   In this cloud service model, the cloud provider manages all aspects of the application environment, such as virtual machines, networking resources, data storage, and applications. The cloud tenant only needs to provide their data to the application managed by the cloud provider.

   **Advantages**
   * No CapEx. Users have no up-front costs.
   * Agility. Users can provide staff with access to the latest software quickly and easily.
   * Pay-as-you-go pricing model. Users pay for the software they use on a subscription model, typically monthly or yearly, regardless of how much they use the software.
   * Skills. No deep technical skills are required to deploy, use, and gain the benefits of SaaS.
   * Flexibility. Users can access the same application data from anywhere.
   
   **Disadvantage**
   * Software limitations. There can be some limitations to a software application that might affect how users work. Because you're using as-is software, you don't have direct control of features. When you're evaluating which SaaS platform is best suited for a workload, be sure to consider any business needs and software limitations.

1. identify a service type based on a use case
   * Infrastructure-as-a-Service (IaaS): Azure Virtual machines
   * Platform-as-a-Service (PaaS): Azure App Service
   * Software-as-a-Service (SaaS): Office 365

### Describe the differences between types of cloud computing

1. define cloud computing [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/intro-to-azure-fundamentals/what-is-cloud-computing)
   It's the delivery of computing services over the internet, which is otherwise known as the cloud. These services include servers, storage, databases, networking, software, analytics, and intelligence. Cloud computing offers faster innovation, flexible resources, and economies of scale.

2. describe Public cloud [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/intro-to-azure-fundamentals/what-is-cloud-computing)
   Services are offered over the public internet and available to anyone who wants to purchase them. Cloud resources like servers and storage are owned and operated by a third-party cloud service provider and delivered over the internet. (Example: Azure, AWS, GCP)

3. describe Private cloud [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/intro-to-azure-fundamentals/what-is-cloud-computing)
   Computing resources are used exclusively by users from one business or organization. A private cloud can be physically located at your organization's on-site datacenter. It also can be hosted by a third-party service provider.(Example: On-premises or 3rd Party Data datacenter)

4. describe Hybrid cloud [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/intro-to-azure-fundamentals/what-is-cloud-computing)
   This computing environment combines a public cloud and a private cloud by allowing data and applications to be shared between them.

5. compare and contrast the three types of cloud computing
   * Public cloud: Shared lower cost and lower adminstration
   * Private cloud: Dedicated Higher cost and higher administration
   * Hybrid: Combination of Public and Private Cloud

## Describe Core Azure Services (15-20%)

### Describe the core Azure architectural components [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/azure-architecture-fundamentals/regions-availability-zones)

1. describe the benefits and usage of Regions and Region Pairs
   A region is a geographical area on the planet that contains at least one but potentially multiple datacenters that are nearby and networked together with a low-latency network. Azure intelligently assigns and controls the resources within each region to ensure workloads are appropriately balanced. Regions give you the flexibility to bring applications closer to your users no matter where they are. Global regions provide better scalability and redundancy. They also preserve data residency for your services

   Each Azure region is always paired with another region within the same geography (such as US, Europe, or Asia) at least 300 miles away. This is know as Region Pairs. This approach allows for the replication of resources (such as VM storage) across a geography that helps reduce the likelihood of interruptions because of events such as natural disasters, civil unrest, power outages, or physical network outages that affect both regions at once. If a region in a pair was affected by a natural disaster, for instance, services would automatically failover to the other region in its region pair.

2. describe the benefits and usage of Availability Zones [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/azure-architecture-fundamentals/regions-availability-zones)
   Availability zones are physically separate datacenters within an Azure region. Each availability zone is made up of one or more datacenters equipped with independent power, cooling, and networking. An availability zone is set up to be an isolation boundary. If one zone goes down, the other continues working. Availability zones are connected through high-speed, private fiber-optic networks.

   You can use availability zones to run mission-critical applications and build high-availability into your application architecture by co-locating your compute, storage, networking, and data resources within a zone and replicating in other zones. Keep in mind that there could be a cost to duplicating your services and transferring data between zones.

   Availability zones are primarily for VMs, managed disks, load balancers, and SQL databases. Azure services that support availability zones fall into two categories:
   * Zonal services: You pin the resource to a specific zone (for example, VMs, managed disks, IP addresses).
   * Zone-redundant services: The platform replicates automatically across zones (for example, zone-redundant storage, SQL Database).

3. describe the benefits and usage of Resource Groups
   Resource groups are a fundamental element of the Azure platform. A resource group is a logical container for resources deployed on Azure. These resources are anything you create in an Azure subscription like VMs, Azure Application Gateway instances, and Azure Cosmos DB instances. All resources must be in a resource group, and a resource can only be a member of a single resource group. Many resources can be moved between resource groups with some services having specific limitations or requirements to move. Resource groups can't be nested. Before any resource can be provisioned, you need a resource group for it to be placed in.
   * Logical grouping: Resource groups exist to help manage and organize your Azure resources. By placing resources of similar usage, type, or location in a resource group, you can provide order and organization to resources you create in Azure. Logical grouping is the aspect that you're most interested in here, because there's a lot of disorder among our resources.
   * Life cycle: If you delete a resource group, all resources contained within it are also deleted. Organizing resources by life cycle can be useful in nonproduction environments, where you might try an experiment and then dispose of it. Resource groups make it easy to remove a set of resources all at once.
   * Authorization: Resource groups are also a scope for applying role-based access control (RBAC) permissions. By applying RBAC permissions to a resource group, you can ease administration and limit access to allow only what's needed.

4. describe the benefits and usage of Subscriptions [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/azure-architecture-fundamentals/management-groups-subscriptions)
   Using Azure requires an Azure subscription. A subscription provides you with authenticated and authorized access to Azure products and services. It also allows you to provision resources. An Azure subscription is a logical unit of Azure services that links to an Azure account, which is an identity in Azure Active Directory (Azure AD) or in a directory that Azure AD trusts.

   An account can have one subscription or multiple subscriptions that have different billing models and to which you apply different access-management policies. You can use Azure subscriptions to define boundaries around Azure products, services, and resources. There are two types of subscription boundaries that you can use:

   * Billing boundary: This subscription type determines how an Azure account is billed for using Azure. You can create multiple subscriptions for different types of billing requirements. Azure generates separate billing reports and invoices for each subscription so that you can organize and manage costs.
   * Access control boundary: Azure applies access-management policies at the subscription level, and you can create separate subscriptions to reflect different organizational structures. An example is that within a business, you have different departments to which you apply distinct Azure subscription policies. This billing model allows you to manage and control access to the resources that users provision with specific subscriptions.

5. describe the benefits and usage of Management Groups [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/azure-architecture-fundamentals/management-groups-subscriptions)
   If your organization has many subscriptions, you might need a way to efficiently manage access, policies, and compliance for those subscriptions. Azure management groups provide a level of scope above subscriptions. You organize subscriptions into containers called management groups and apply your governance conditions to the management groups. All subscriptions within a management group automatically inherit the conditions applied to the management group. Management groups give you enterprise-grade management at a large scale no matter what type of subscriptions you might have. All subscriptions within a single management group must trust the same Azure AD tenant.

   For example, you can apply policies to a management group that limits the regions available for VM creation. This policy would be applied to all management groups, subscriptions, and resources under that management group by only allowing VMs to be created in that region.

   A flexible structure of management groups and subscriptions can be use to organize your resources into a hierarchy for unified policy and access management.

6. describe the benefits and usage of Azure Resource Manager [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/azure-architecture-fundamentals/resources-resource-manager)
   Azure Resource Manager is the deployment and management service for Azure. It provides a management layer that enables you to create, update, and delete resources in your Azure account. You use management features like access control, locks, and tags to secure and organize your resources after deployment.

   When a user sends a request from any of the Azure tools, APIs, or SDKs, Resource Manager receives the request. It authenticates and authorizes the request. Resource Manager sends the request to the Azure service, which takes the requested action. Because all requests are handled through the same API, you see consistent results and capabilities in all the different tools.

   **Benefits**
   * Manage your infrastructure through declarative templates rather than scripts. A Resource Manager template is a JSON file that defines what you want to deploy to Azure.
   * Deploy, manage, and monitor all the resources for your solution as a group, rather than handling these resources individually.
   * Redeploy your solution throughout the development life cycle and have confidence your resources are deployed in a consistent state.
   * Define the dependencies between resources so they're deployed in the correct order.
   * Apply access control to all services because RBAC is natively integrated into the management platform.
   * Apply tags to resources to logically organize all the resources in your subscription.
   * Clarify your organization's billing by viewing costs for a group of resources that share the same tag.

7. explain Azure resources
   A manageable item that's available through Azure. Virtual machines (VMs), storage accounts, web apps, databases, and virtual networks are examples of resources.

### Describe core resources available in Azure

1. describe the benefits and usage of Virtual Machines [Microsoft Learn](https://docs.microsoft.com/en-us/learn/modules/azure-compute-fundamentals/azure-virtual-machines)

   With Azure Virtual Machines, you can create and use VMs in the cloud. VMs provide infrastructure as a service (IaaS) in the form of a virtualized server and can be used in many ways. Just like a physical computer, you can customize all of the software running on the VM. An Azure VM gives you the flexibility of virtualization without having to buy and maintain the physical hardware that runs the VM. You still need to configure, update, and maintain the software that runs on the VM. VMs are an ideal choice when you need:
     * Total control over the operating system (OS).
     * The ability to run custom software.
     * To use custom hosting configurations.

   You can create and provision a VM in minutes when you select a preconfigured VM image. Selecting an image is one of the most important decisions you'll make when you create a VM. An image is a template used to create a VM. These templates already include an OS and often other software, like development tools or web hosting environments.

   **Examples of when to use VMs**

   * During testing and development. VMs provide a quick and easy way to create different OS and application configurations. Test and development personnel can then easily delete the VMs when they no longer need them.
   * When running applications in the cloud. The ability to run certain applications in the public cloud as opposed to creating a traditional infrastructure to run them can provide substantial economic benefits. For example, an application might need to handle fluctuations in demand. Shutting down VMs when you don't need them or quickly starting them up to meet a sudden increase in demand means you pay only for the resources you use.
   * When extending your datacenter to the cloud. An organization can extend the capabilities of its own on-premises network by creating a virtual network in Azure and adding VMs to that virtual network. Applications like SharePoint can then run on an Azure VM instead of running locally. This arrangement makes it easier or less expensive to deploy than in an on-premises environment.
   * During disaster recovery. As with running certain types of applications in the cloud and extending an on-premises network to the cloud, you can get significant cost savings by using an IaaS-based approach to disaster recovery. If a primary datacenter fails, you can create VMs running on Azure to run your critical applications and then shut them down when the primary datacenter becomes operational again.
  
   **Move to the cloud with VMs**

   VMs are also an excellent choice when you move from a physical server to the cloud (also known as lift and shift). You can create an image of the physical server and host it within a VM with little or no changes. Just like a physical on-premises server, you must maintain the VM. You update the installed OS and the software it runs.

   **Scale VMs in Azure**

   You can run single VMs for testing, development, or minor tasks. Or you can group VMs together to provide high availability, scalability, and redundancy. No matter what your uptime requirements are, Azure has several features that can meet them. These features include:
   * Virtual machine scale sets
   * Azure Batch
  
   **What are virtual machine scale sets?**

   Virtual machine scale sets let you create and manage a group of identical, load-balanced VMs. Imagine you're running a website that enables scientists to upload astronomy images that need to be processed. If you duplicated the VM, you'd normally need to configure an additional service to route requests between multiple instances of the website. Virtual machine scale sets could do that work for you.

   Scale sets allow you to centrally manage, configure, and update a large number of VMs in minutes to provide highly available applications. The number of VM instances can automatically increase or decrease in response to demand or a defined schedule. With virtual machine scale sets, you can build large-scale services for areas such as compute, big data, and container workloads.

2. describe the benefits and usage of Azure App Services [Microsoft Learn](https://docs.microsoft.com/en-us/learn/modules/azure-compute-fundamentals/azure-app-services)

   App Service enables you to build and host web apps, background jobs, mobile back-ends, and RESTful APIs in the programming language of your choice without managing infrastructure. It offers automatic scaling and high availability. App Service supports Windows and Linux and enables automated deployments from GitHub, Azure DevOps, or any Git repo to support a continuous deployment model.

   This platform as a service (PaaS) environment allows you to focus on the website and API logic while Azure handles the infrastructure to run and scale your web applications.

   **Azure App Service costs**

   You pay for the Azure compute resources your app uses while it processes requests based on the App Service plan you choose. The App Service plan determines how much hardware is devoted to your host. For example, the plan determines whether it's dedicated or shared hardware and how much memory is reserved for it. There's even a free tier you can use to host small, low-traffic sites.

   **Types of app services**

   With App Service, you can host most common app service styles like:
   * Web apps
   * API apps
   * WebJobs
   * Mobile apps

   App Service handles most of the infrastructure decisions you deal with in hosting web-accessible apps:

    * Deployment and management are integrated into the platform.
    * Endpoints can be secured.
    * Sites can be scaled quickly to handle high traffic loads.
    * The built-in load balancing and traffic manager provide high availability.

   All of these app styles are hosted in the same infrastructure and share these benefits. This flexibility makes App Service the ideal choice to host web-oriented applications.

   **Web apps**

   App Service includes full support for hosting web apps by using ASP.NET, ASP.NET Core, Java, Ruby, Node.js, PHP, or Python. You can choose either Windows or Linux as the host operating system.

   **API apps**

   Much like hosting a website, you can build REST-based web APIs by using your choice of language and framework. You get full Swagger support and the ability to package and publish your API in Azure Marketplace. The produced apps can be consumed from any HTTP- or HTTPS-based client.

   **WebJobs**

   You can use the WebJobs feature to run a program (.exe, Java, PHP, Python, or Node.js) or script (.cmd, .bat, PowerShell, or Bash) in the same context as a web app, API app, or mobile app. They can be scheduled or run by a trigger. WebJobs are often used to run background tasks as part of your application logic.

   **Mobile apps**

   Use the Mobile Apps feature of App Service to quickly build a back end for iOS and Android apps. With just a few clicks in the Azure portal, you can:
   * Store mobile app data in a cloud-based SQL database.
   * Authenticate customers against common social providers, such as MSA, Google, Twitter, and Facebook.
   * Send push notifications.
   * Execute custom back-end logic in C# or Node.js.

   On the mobile app side, there's SDK support for native iOS and Android, Xamarin, and React native apps.

3. describe the benefits and usage of Azure Container Instances (ACI) [Microsoft Learn](https://docs.microsoft.com/en-us/learn/modules/azure-compute-fundamentals/azure-container-services)

   Offers the fastest and simplest way to run a container in Azure without having to manage any virtual machines or adopt any additional services. It's a platform as a service (PaaS) offering that allows you to upload your containers, which it runs for you

4. describe the benefits and usage of Azure Kubernetes Service (AKS)[Microsoft Learn](https://docs.microsoft.com/en-us/learn/modules/azure-compute-fundamentals/azure-container-services)
   
   The task of automating, managing, and interacting with a large number of containers is known as orchestration. Azure Kubernetes Service is a complete orchestration service for containers with distributed architectures and large volumes of containers. Orchestration is the task of automating and managing a large number of containers and how they interact.

5. describe the benefits and usage of Windows Virtual Desktop [Microsoft Learn](https://docs.microsoft.com/en-us/learn/modules/azure-compute-fundamentals/azure-virtual-machines)

   Windows Virtual Desktop on Azure is a desktop and application virtualization service that runs on the cloud. It enables your users to use a cloud-hosted version of Windows from any location. Windows Virtual Desktop works across devices like Windows, Mac, iOS, Android, and Linux. It works with apps that you can use to access remote desktops and apps. You can also use most modern browsers to access Windows Virtual Desktop-hosted experiences.

   **Provide the best user experience**

   Users have the freedom to connect to Windows Virtual Desktop with any device over the internet. They use a Windows Virtual Desktop client to connect to their published Windows desktop and applications. This client could either be a native application on the device or the Windows Virtual Desktop HTML5 web client.

   You can make sure your session host virtual machines (VMs) run near apps and services that connect to your datacenter or the cloud. This way your users stay productive and don't encounter long load times.

   User sign-in to Windows Virtual Desktop is fast because user profiles are containerized by using FSLogix. At sign-in, the user profile container is dynamically attached to the computing environment. The user profile is immediately available and appears in the system exactly like a native user profile.

   You can provide individual ownership through personal (persistent) desktops. For example, you might want to provide personal remote desktops for members of an engineering team. Then they can add or remove programs without impacting other users on that remote desktop.

   **Enhance security**

   Windows Virtual Desktop provides centralized security management for users' desktops with Azure Active Directory (Azure AD). You can enable multifactor authentication to secure user sign-ins. You can also secure access to data by assigning granular role-based access controls (RBACs) to users.

   With Windows Virtual Desktop, the data and apps are separated from the local hardware. Windows Virtual Desktop runs them instead on a remote server. The risk of confidential data being left on a personal device is reduced.

   User sessions are isolated in both single and multi-session environments.

   Windows Virtual Desktop also improves security by using reverse connect technology. This connection type is more secure than the Remote Desktop Protocol. We don't open inbound ports to the session host VMs.

   **Simplified management**

   Windows Virtual Desktop is an Azure service, so it will be familiar to Azure administrators. You use Azure AD and RBACs to manage access to resources. With Azure, you also get tools to automate VM deployments, manage VM updates, and provide disaster recovery. As with other Azure services, Windows Virtual Desktop uses Azure Monitor for monitoring and alerts. This standardization lets admins identify issues through a single interface.

   **Performance management**

   Windows Virtual Desktop gives you options to load balance users on your VM host pools. Host pools are collections of VMs with the same configuration assigned to multiple users. For the best performance, you can configure load balancing to occur as users sign in (breadth mode). With breadth mode, users are sequentially allocated across the host pool for your workload. To save costs, you can configure your VMs for depth mode load balancing where users are fully allocated on one VM before moving to the next. Windows Virtual Desktop provides tools to automatically provision additional VMs when incoming demand exceeds a specified threshold.

   **Multi-session Windows 10 deployment**

   Windows Virtual Desktop lets you use Windows 10 Enterprise multi-session, the only Windows client-based operating system that enables multiple concurrent users on a single VM. Windows Virtual Desktop also provides a more consistent experience with broader application support compared to Windows Server-based operating systems.

6. describe the benefits and usage of Virtual Networks [Microsoft Learn](https://docs.microsoft.com/en-us/learn/modules/azure-networking-fundamentals/azure-virtual-network-fundamentals)

   Azure virtual networks enable Azure resources, such as VMs, web apps, and databases, to communicate with each other, with users on the internet, and with your on-premises client computers. You can think of an Azure network as a set of resources that links other Azure resources.

   Azure virtual networks provide the following key networking capabilities:

   **Isolation and segmentation**

   Virtual Network allows you to create multiple isolated virtual networks. When you set up a virtual network, you define a private IP address space by using either public or private IP address ranges. You can divide that IP address space into subnets and allocate part of the defined address space to each named subnet.
  
   For name resolution, you can use the name resolution service that's built in to Azure. You also can configure the virtual network to use either an internal or an external DNS server.

   **Internet communications**

   A VM in Azure can connect to the internet by default. You can enable incoming connections from the internet by defining a public IP address or a public load balancer. For VM management, you can connect via the Azure CLI, Remote Desktop Protocol, or Secure Shell.

   **Communicate between Azure resources**
   You'll want to enable Azure resources to communicate securely with each other. You can do that in one of two ways:

   * Virtual networks

     Virtual networks can connect not only VMs but other Azure resources, such as the App Service Environment for Power Apps, Azure Kubernetes Service, and Azure virtual machine scale sets.

   * Service endpoints

     You can use service endpoints to connect to other Azure resource types, such as Azure SQL databases and storage accounts. This approach enables you to link multiple Azure resources to virtual networks to improve security and provide optimal routing between resources.

   **Communicate with on-premises resources**

   You'll want to enable Azure resources to communicate securely with each other. You can do that in one of two ways:

   *Virtual networks*

   Virtual networks can connect not only VMs but other Azure resources, such as the App Service Environment for Power Apps, Azure Kubernetes Service, and Azure virtual machine scale sets

   *Service endpoints*

   You can use service endpoints to connect to other Azure resource types, such as Azure SQL databases and storage accounts. This approach enables you to link multiple Azure resources to virtual networks to improve security and provide optimal routing between resources.

   **Route network traffic**

   By default, Azure routes traffic between subnets on any connected virtual networks, on-premises networks, and the internet. You also can control routing and override those settings, as follows:

   *Route tables*

   A route table allows you to define rules about how traffic should be directed. You can create custom route tables that control how packets are routed between subnets.

   *Border Gateway Protocol*

   Border Gateway Protocol (BGP) works with Azure VPN gateways or ExpressRoute to propagate on-premises BGP routes to Azure virtual networks.

   **Filter network traffic**

   Azure virtual networks enable you to filter traffic between subnets by using the following approaches:

   *Network security groups*

   A network security group is an Azure resource that can contain multiple inbound and outbound security rules. You can define these rules to allow or block traffic, based on factors such as source and destination IP address, port, and protocol.

   *Network virtual appliances*

   A network virtual appliance is a specialized VM that can be compared to a hardened network appliance. A network virtual appliance carries out a particular network function, such as running a firewall or performing wide area network (WAN) optimization.

   **Connect virtual networks**

   You can link virtual networks together by using virtual network peering. Peering enables resources in each virtual network to communicate with each other. These virtual networks can be in separate regions, which allows you to create a global interconnected network through Azure.

   UDR is user-defined Routing. UDR is a significant update to Azure’s Virtual Networks as this allows network admins to control the routing tables between subnets within a VNet, as well as between VNets, thereby allowing for greater control over network traffic flow.

7. describe the benefits and usage of VPN Gateway [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/azure-networking-fundamentals/azure-vpn-gateway-fundamentals)

   A VPN gateway is a type of virtual network gateway. Azure VPN Gateway instances are deployed in Azure Virtual Network instances and enable the following connectivity:

   * Connect on-premises datacenters to virtual networks through a site-to-site connection.
   * Connect individual devices to virtual networks through a point-to-site connection.
   * Connect virtual networks to other virtual networks through a network-to-network connection.
  
   All transferred data is encrypted in a private tunnel as it crosses the internet. You can deploy only one VPN gateway in each virtual network, but you can use one gateway to connect to multiple locations, which includes other virtual networks or on-premises datacenters.
  
   When you deploy a VPN gateway, you specify the VPN type: either policy-based or route-based. The main difference between these two types of VPNs is how traffic to be encrypted is specified. In Azure, both types of VPN gateways use a pre-shared key as the only method of authentication. Both types also rely on Internet Key Exchange (IKE) in either version 1 or version 2 and Internet Protocol Security (IPSec). IKE is used to set up a security association (an agreement of the encryption) between two endpoints. This association is then passed to the IPSec suite, which encrypts and decrypts data packets encapsulated in the VPN tunnel.
  
   **Policy-based VPNs**
  
   Policy-based VPN gateways specify statically the IP address of packets that should be encrypted through each tunnel. This type of device evaluates every data packet against those sets of IP addresses to choose the tunnel where that packet is going to be sent through.
  
   Key features of policy-based VPN gateways in Azure include:
  
   * Support for IKEv1 only.
   * Use of static routing, where combinations of address prefixes from both networks control how traffic is encrypted and decrypted through the VPN tunnel. The source and destination of the tunneled networks are declared in the policy and don't need to be declared in routing tables.
   * Policy-based VPNs must be used in specific scenarios that require them, such as for compatibility with legacy on-premises VPN devices.

   **Route-based VPNs**

   If defining which IP addresses are behind each tunnel is too cumbersome, route-based gateways can be used. With route-based gateways, IPSec tunnels are modeled as a network interface or virtual tunnel interface. IP routing (either static routes or dynamic routing protocols) decides which one of these tunnel interfaces to use when sending each packet. Route-based VPNs are the preferred connection method for on-premises devices. They're more resilient to topology changes such as the creation of new subnets.

   Use a route-based VPN gateway if you need any of the following types of connectivity:

   * Connections between virtual networks
   * Point-to-site connections
   * Multisite connections
   * Coexistence with an Azure ExpressRoute gateway
  
   Key features of route-based VPN gateways in Azure include:

   * Supports IKEv2
   * Uses any-to-any (wildcard) traffic selectors
   * Can use dynamic routing protocols, where routing/forwarding tables direct traffic to different IPSec tunnels

   In this case, the source and destination networks aren't statically defined as they are in policy-based VPNs or even in route-based VPNs with static routing. Instead, data packets are encrypted based on network routing tables that are created dynamically using routing protocols such as Border Gateway Protocol (BGP).

   **Deploy VPN gateways**
   
   Before you can deploy a VPN gateway, you'll need some Azure and on-premises resources.

   *Required Azure resources*

   You'll need these Azure resources before you can deploy an operational VPN gateway:

   * Virtual network. Deploy a virtual network with enough address space for the additional subnet that you'll need for the VPN gateway. The address space for this virtual network must not overlap with the on-premises network that you'll be connecting to. You can deploy only one VPN gateway within a virtual network.

   * GatewaySubnet. Deploy a subnet called GatewaySubnet for the VPN gateway. Use at least a /27 address mask to make sure you have enough IP addresses in the subnet for future growth. You can't use this subnet for any other services.

   * Public IP address. Create a Basic-SKU dynamic public IP address if you're using a non-zone-aware gateway. This address provides a public-routable IP address as the target for your on-premises VPN device. This IP address is dynamic, but it won't change unless you delete and re-create the VPN gateway.

   * Local network gateway. Create a local network gateway to define the on-premises network's configuration, such as where the VPN gateway will connect and what it will connect to. This configuration includes the on-premises VPN device's public IPv4 address and the on-premises routable networks. This information is used by the VPN gateway to route packets that are destined for on-premises networks through the IPSec tunnel.

   * Virtual network gateway. Create the virtual network gateway to route traffic between the virtual network and the on-premises datacenter or other virtual networks. The virtual network gateway can be either a VPN or ExpressRoute gateway, but this unit only deals with VPN virtual network gateways. (You'll learn more about ExpressRoute in a separate unit later in this module.)

   * Connection. Create a connection resource to create a logical connection between the VPN gateway and the local network gateway
     * The connection is made to the on-premises VPN device's IPv4 address as defined by the local network gateway.
     * The connection is made from the virtual network gateway and its associated public IP address.

   *Required on-premises resources*

   To connect your datacenter to a VPN gateway, you'll need these on-premises resources:

   * A VPN device that supports policy-based or route-based VPN gateways
   * A public-facing (internet-routable) IPv4 address

   **High-availability scenarios**

   There are several ways to ensure you have a fault-tolerant configuration.

   *Active/standby*

   By default, VPN gateways are deployed as two instances in an active/standby configuration, even if you only see one VPN gateway resource in Azure. When planned maintenance or unplanned disruption affects the active instance, the standby instance automatically assumes responsibility for connections without any user intervention. Connections are interrupted during this failover, but they're typically restored within a few seconds for planned maintenance and within 90 seconds for unplanned disruptions.

   *Active/active*

   With the introduction of support for the BGP routing protocol, you can also deploy VPN gateways in an active/active configuration. In this configuration, you assign a unique public IP address to each instance. You then create separate tunnels from the on-premises device to each IP address. You can extend the high availability by deploying an additional VPN device on-premises.

   **ExpressRoute failover**

   Another high-availability option is to configure a VPN gateway as a secure failover path for ExpressRoute connections. ExpressRoute circuits have resiliency built in. But they aren't immune to physical problems that affect the cables delivering connectivity or outages that affect the complete ExpressRoute location. In high-availability scenarios, where there's risk associated with an outage of an ExpressRoute circuit, you can also provision a VPN gateway that uses the internet as an alternative method of connectivity. In this way, you can ensure there's always a connection to the virtual networks.

   **Zone-redundant gateways**

   In regions that support availability zones, VPN gateways and ExpressRoute gateways can be deployed in a zone-redundant configuration. This configuration brings resiliency, scalability, and higher availability to virtual network gateways. Deploying gateways in Azure availability zones physically and logically separates gateways within a region while protecting your on-premises network connectivity to Azure from zone-level failures. These gateways require different gateway SKUs and use Standard public IP addresses instead of Basic public IP addresses.

8. describe the benefits and usage of Virtual Network peering [Microsoft Documentation Reference](https://docs.microsoft.com/en-us/azure/virtual-network/virtual-network-peering-overview)

   Virtual network peering enables you to seamlessly connect two or more Virtual Networks in Azure. The virtual networks appear as one for connectivity purposes. The traffic between virtual machines in peered virtual networks uses the Microsoft backbone infrastructure. Like traffic between virtual machines in the same network, traffic is routed through Microsoft's private network only.

   Azure supports the following types of peering:
   * Virtual network peering: Connect virtual networks within the same Azure region.
   * Global virtual network peering: Connecting virtual networks across Azure regions.
  
   The benefits of using virtual network peering, whether local or global, include:

   * A low-latency, high-bandwidth connection between resources in different virtual networks.
   * The ability for resources in one virtual network to communicate with resources in a different virtual network.
   * The ability to transfer data between virtual networks across Azure subscriptions, Azure Active Directory tenants, deployment models, and Azure regions.
   * The ability to peer virtual networks created through the Azure Resource Manager.
   * The ability to peer a virtual network created through Resource Manager to one created through the classic deployment model. To learn more about Azure deployment models, see Understand Azure deployment models.
   * No downtime to resources in either virtual network when creating the peering, or after the peering is created.
   * Network traffic between peered virtual networks is private. Traffic between the virtual networks is kept on the Microsoft backbone network. No public Internet, gateways, or encryption is required in the communication between the virtual networks.

9. describe the benefits and usage of ExpressRoute [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/azure-networking-fundamentals/express-route-fundamentals)

    ExpressRoute lets you extend your on-premises networks into the Microsoft cloud over a private connection with the help of a connectivity provider. With ExpressRoute, you can establish connections to Microsoft cloud services, such as Microsoft Azure and Microsoft 365.

    Connectivity can be from an any-to-any (IP VPN) network, a point-to-point Ethernet network, or a virtual cross-connection through a connectivity provider at a colocation facility. ExpressRoute connections don't go over the public Internet. This allows ExpressRoute connections to offer more reliability, faster speeds, consistent latencies, and higher security than typical connections over the Internet. For information on how to connect your network to Microsoft using ExpressRoute, see ExpressRoute connectivity models.

    **Features and benefits of ExpressRoute**

    There are several benefits to using ExpressRoute as the connection service between Azure and on-premises networks.

    * Layer 3 connectivity between your on-premises network and the Microsoft Cloud through a connectivity provider. Connectivity can be from an any-to-any (IPVPN) network, a point-to-point Ethernet connection, or through a virtual cross-connection via an Ethernet exchange.
    * Connectivity to Microsoft cloud services across all regions in the geopolitical region.
    * Global connectivity to Microsoft services across all regions with the ExpressRoute premium add-on.
    * Dynamic routing between your network and Microsoft via BGP.
    * Built-in redundancy in every peering location for higher reliability.
    * Connection uptime SLA.
    * QoS support for Skype for Business.

    **Layer 3 connectivity**

    ExpressRoute provides Layer 3 (address-level) connectivity between your on-premises network and the Microsoft cloud through connectivity partners. These connections can be from a point-to-point or any-to-any network. They can also be virtual cross-connections through an exchange.

    **Built-in redundancy**

    Each connectivity provider uses redundant devices to ensure that connections established with Microsoft are highly available. You can configure multiple circuits to complement this feature. All redundant connections are configured with Layer 3 connectivity to meet service-level agreements.

    **Connectivity to Microsoft cloud services**

    ExpressRoute enables direct access to the following services in all regions:

    * Microsoft Office 365
    * Microsoft Dynamics 365
    * Azure compute services, such as Azure Virtual Machines
    * Azure cloud services, such as Azure Cosmos DB and Azure Storage
  
    Office 365 was created to be accessed securely and reliably via the internet. For this reason, we recommend the use of ExpressRoute for specific scenarios. The "Learn more" section at the end of this module includes a link about using ExpressRoute to access Office 365.

    **Across on-premises connectivity with ExpressRoute Global Reach**

    You can enable ExpressRoute Global Reach to exchange data across your on-premises sites by connecting your ExpressRoute circuits. For example, assume that you have a private datacenter in California connected to ExpressRoute in Silicon Valley. You have another private datacenter in Texas connected to ExpressRoute in Dallas. With ExpressRoute Global Reach, you can connect your private datacenters through two ExpressRoute circuits. Your cross-datacenter traffic will travel through the Microsoft network.

    **Dynamic routing**

    ExpressRoute uses the Border Gateway Protocol (BGP) routing protocol. BGP is used to exchange routes between on-premises networks and resources running in Azure. This protocol enables dynamic routing between your on-premises network and services running in the Microsoft cloud.

    **ExpressRoute connectivity models**

    ExpressRoute supports three models that you can use to connect your on-premises network to the Microsoft cloud:

    * CloudExchange colocation

      Colocated providers can normally offer both Layer 2 and Layer 3 connections between your infrastructure, which might be located in the colocation facility, and the Microsoft cloud. For example, if your datacenter is colocated at a cloud exchange such as an ISP, you can request a virtual cross-connection to the Microsoft cloud.

    * Point-to-point Ethernet connection

      Point-to-point connections provide Layer 2 and Layer 3 connectivity between your on-premises site and Azure. You can connect your offices or datacenters to Azure by using the point-to-point links. For example, if you have an on-premises datacenter, you can use a point-to-point Ethernet link to connect to Microsoft.

    * Any-to-any connection

      With any-to-any connectivity, you can integrate your wide area network (WAN) with Azure by providing connections to your offices and datacenters. Azure integrates with your WAN connection to provide a connection like you would have between your datacenter and any branch offices.

      With any-to-any connections, all WAN providers offer Layer 3 connectivity. For example, if you already use Multiprotocol Label Switching to connect to your branch offices or other sites in your organization, an ExpressRoute connection to Microsoft behaves like any other location on your private WAN.

    **Security considerations**

    With ExpressRoute, your data doesn't travel over the public internet, so it's not exposed to the potential risks associated with internet communications. ExpressRoute is a private connection from your on-premises infrastructure to your Azure infrastructure. Even if you have an ExpressRoute connection, DNS queries, certificate revocation list checking, and Azure Content Delivery Network requests are still sent over the public internet.

10. describe the benefits and usage of Container (Blob) Storage

    Azure Blob Storage is an object storage solution for the cloud. It can store massive amounts of data, such as text or binary data. Azure Blob Storage is unstructured, meaning that there are no restrictions on the kinds of data it can hold. Blob Storage can manage thousands of simultaneous uploads, massive amounts of video data, constantly growing log files, and can be reached from anywhere with an internet connection.

    Blobs aren't limited to common file formats. A blob could contain gigabytes of binary data streamed from a scientific instrument, an encrypted message for another application, or data in a custom format for an app you're developing. One advantage of blob storage over disk storage is that it does not require developers to think about or manage disks; data is uploaded as blobs, and Azure takes care of the physical storage needs.

    Blob Storage is ideal for:

    * Serving images or documents directly to a browser.
    * Storing files for distributed access.
    * Streaming video and audio.
    * Storing data for backup and restore, disaster recovery, and archiving.
    * Storing data for analysis by an on-premises or Azure-hosted service.
    * Storing up to 8 TB of data for virtual machines.

11. describe the benefits and usage of Disk Storage [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/azure-storage-fundamentals/azure-disk-storage)

    Disk Storage provides disks for Azure virtual machines. Applications and other services can access and use these disks as needed, similar to how they would in on-premises scenarios. Disk Storage allows data to be persistently stored and accessed from an attached virtual hard disk.

    Disks come in many different sizes and performance levels, from solid-state drives (SSDs) to traditional spinning hard disk drives (HDDs), with varying performance tiers. You can use standard SSD and HDD disks for less critical workloads, premium SSD disks for mission-critical production applications, and ultra disks for data-intensive workloads such as SAP HANA, top tier databases, and transaction-heavy workloads. Azure has consistently delivered enterprise-grade durability for infrastructure as a service (Iaas) disks, with an industry-leading ZERO% annualized failure rate.

12. describe the benefits and usage of File Storage [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/azure-storage-fundamentals/azure-file-storage)

    Azure Files offers fully managed file shares in the cloud that are accessible via the industry standard Server Message Block and Network File System (preview) protocols. Azure file shares can be mounted concurrently by cloud or on-premises deployments of Windows, Linux, and macOS. Applications running in Azure virtual machines or cloud services can mount a file storage share to access file data, just as a desktop application would mount a typical SMB share. Any number of Azure virtual machines or roles can mount and access the file storage share simultaneously. Typical usage scenarios would be to share files anywhere in the world, diagnostic data, or application data sharing.

    Use Azure Files for the following situations:

    * Many on-premises applications use file shares. Azure Files makes it easier to migrate those applications that share data to Azure. If you mount the Azure file share to the same drive letter that the on-premises application uses, the part of your application that accesses the file share should work with minimal changes, if any.
    * Store configuration files on a file share and access them from multiple VMs. Tools and utilities used by multiple developers in a group can be stored on a file share, ensuring that everybody can find them, and that they use the same version.
    * Write data to a file share, and process or analyze the data later. For example, you might want to do this with diagnostic logs, metrics, and crash dumps.

    One thing that distinguishes Azure Files from files on a corporate file share is that you can access the files from anywhere in the world, by using a URL that points to the file. You can also use Shared Access Signature (SAS) tokens to allow access to a private asset for a specific amount of time.

13. describe the benefits and usage of storage tiers [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/azure-storage-fundamentals/azure-storage-tiers)

    Data stored in the cloud can grow at an exponential pace. To manage costs for your expanding storage needs, it's helpful to organize your data based on attributes like frequency of access and planned retention period. Data stored in the cloud can be different based on how it's generated, processed, and accessed over its lifetime. Some data is actively accessed and modified throughout its lifetime. Some data is accessed frequently early in its lifetime, with access dropping drastically as the data ages. Some data remains idle in the cloud and is rarely, if ever, accessed after it's stored. To accommodate these different access needs, Azure provides several access tiers, which you can use to balance your storage costs with your access needs.

    Azure Storage offers different access tiers for your blob storage, helping you store object data in the most cost-effective manner. The available access tiers include:

    * Hot access tier: Optimized for storing data that is accessed frequently (for example, images for your website).
    * Cool access tier: Optimized for data that is infrequently accessed and stored for at least 30 days (for example, invoices for your customers).
    * Archive access tier: Appropriate for data that is rarely accessed and stored for at least 180 days, with flexible latency requirements (for example, long-term backups).
  
    The following considerations apply to the different access tiers:
  
    * Only the hot and cool access tiers can be set at the account level. The archive access tier isn't available at the account level.
    * Hot, cool, and archive tiers can be set at the blob level, during upload or after upload.
    * Data in the cool access tier can tolerate slightly lower availability, but still requires high durability, retrieval latency, and throughput characteristics similar to hot data. For cool data, a slightly lower availability service-level agreement (SLA) and higher access costs compared to hot data are acceptable trade-offs for lower storage costs.
    * Archive storage stores data offline and offers the lowest storage costs, but also the highest costs to rehydrate and access data

14. describe the benefits and usage of Cosmos DB [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/azure-database-fundamentals/azure-cosmos-db)

    Azure Cosmos DB is a globally distributed, multi-model database service. You can elastically and independently scale throughput and storage across any number of Azure regions worldwide. You can take advantage of fast, single-digit-millisecond data access by using any one of several popular APIs. Azure Cosmos DB provides comprehensive service level agreements for throughput, latency, availability, and consistency guarantees.

    Azure Cosmos DB supports schema-less data, which lets you build highly responsive and "Always On" applications to support constantly changing data. You can use this feature to store data that's updated and maintained by users around the world.

    Azure Cosmos DB is flexible. At the lowest level, Azure Cosmos DB stores data in atom-record-sequence (ARS) format. The data is then abstracted and projected as an API, which you specify when you're creating your database. Your choices include SQL, MongoDB, Cassandra, Tables, and Gremlin. This level of flexibility means that as you migrate your company's databases to Azure Cosmos DB, your developers can stick with the API that they're the most comfortable with.

15. describe the benefits and usage of Azure SQL Database [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/azure-database-fundamentals/azure-sql-database)

    Azure SQL Database is a relational database based on the latest stable version of the Microsoft SQL Server database engine. SQL Database is a high-performance, reliable, fully managed, and secure database. You can use it to build data-driven applications and websites in the programming language of your choice, without needing to manage infrastructure.

    **Features**

    Azure SQL Database is a platform as a service (PaaS) database engine. It handles most of the database management functions, such as upgrading, patching, backups, and monitoring, without user involvement. SQL Database provides 99.99 percent availability. PaaS capabilities that are built into SQL Database enable you to focus on the domain-specific database administration and optimization activities that are critical for your business. SQL Database is a fully managed service that has built-in high availability, backups, and other common maintenance operations. Microsoft handles all updates to the SQL and operating system code. You don't have to manage the underlying infrastructure.

    You can create a highly available and high-performance data storage layer for the applications and solutions in Azure. SQL Database can be the right choice for a variety of modern cloud applications because it enables you to process both relational data and non-relational structures, such as graphs, JSON, spatial, and XML.

    You can use advanced query processing features, such as high-performance, in-memory technologies and intelligent query processing. In fact, the newest capabilities of SQL Server are released first to SQL Database, and then to SQL Server itself. You get the newest SQL Server capabilities, with no overhead for updates or upgrades, tested across millions of databases.

    **Migration**

    You can migrate your existing SQL Server databases with minimal downtime by using the Azure Database Migration Service. The Microsoft Data Migration Assistant can generate assessment reports that provide recommendations to help guide you through required changes prior to performing a migration. After you assess and resolve any remediation required, you're ready to begin the migration process. The Azure Database Migration Service performs all of the required steps. You just change the connection string in your apps.

16. describe the benefits and usage of Azure Database for MySQL [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/azure-database-fundamentals/azure-mysql-database)

    Azure Database for MySQL is a relational database service in the cloud, and it's based on the MySQL Community Edition database engine, versions 5.6, 5.7, and 8.0. With it, you have a 99.99 percent availability service level agreement from Azure, powered by a global network of Microsoft-managed datacenters. This helps keep your app running 24/7. With every Azure Database for MySQL server, you take advantage of built-in security, fault tolerance, and data protection that you would otherwise have to buy or design, build, and manage. With Azure Database for MySQL, you can use point-in-time restore to recover a server to an earlier state, as far back as 35 days.

    Azure Database for MySQL delivers:

    * Built-in high availability with no additional cost.
    * Predictable performance and inclusive, pay-as-you-go pricing.
    * Scale as needed, within seconds.
    * Ability to protect sensitive data at-rest and in-motion.
    * Automatic backups.
    * Enterprise-grade security and compliance.

    These capabilities require almost no administration, and all are provided at no additional cost. They allow you to focus on rapid app development and accelerating your time-to-market, rather than having to manage virtual machines and infrastructure. In addition, you can migrate your existing MySQL databases with minimal downtime by using the Azure Database Migration Service. After you have completed your migration, you can continue to develop your application with the open-source tools and platform of your choice. You don't have to learn new skills.

    Azure Database for MySQL offers several service tiers, and each tier provides different performance and capabilities to support lightweight to heavyweight database workloads. You can build your first app on a small database for a few dollars a month, and then adjust the scale to meet the needs of your solution. Dynamic scalability enables your database to transparently respond to rapidly changing resource requirements. You only pay for the resources you need, and only when you need them.

17. describe the benefits and usage of Azure Database for PostgreSQL [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/azure-database-fundamentals/azure-postgresql-database)

    Azure Database for PostgreSQL is a relational database service in the cloud. The server software is based on the community version of the open-source PostgreSQL database engine. Your familiarity with tools and expertise with PostgreSQL is applicable when you're using Azure Database for PostgreSQL.

    Moreover, Azure Database for PostgreSQL delivers the following benefits:

    * Built-in high availability compared to on-premises resources. There's no additional configuration, replication, or cost required to make sure your applications are always available.
    * Simple and flexible pricing. You have predictable performance based on a selected pricing tier choice that includes software patching, automatic backups, monitoring, and security.
    * Scale up or down as needed, within seconds. You can scale compute or storage independently as needed, to make sure you adapt your service to match usage.
    * Adjustable automatic backups and point-in-time-restore for up to 35 days.
    * Enterprise-grade security and compliance to protect sensitive data at-rest and in-motion. This security covers data encryption on disk and SSL encryption between client and server communication.

    Azure Database for PostgreSQL is available in two deployment options: Single Server and Hyperscale (Citus).

    **Single Server**

    The Single Server deployment option delivers:

    * Built-in high availability with no additional cost (99.99 percent SLA).
    * Predictable performance and inclusive, pay-as-you-go pricing.
    * Vertical scale as needed, within seconds.
    * Monitoring and alerting to assess your server.
    * Enterprise-grade security and compliance.
    * Ability to protect sensitive data at-rest and in-motion.
    * Automatic backups and point-in-time-restore for up to 35 days.

    All those capabilities require almost no administration, and all are provided at no additional cost. You can focus on rapid application development and accelerating your time to market, rather than having to manage virtual machines and infrastructure. You can continue to develop your application with the open-source tools and platform of your choice, without having to learn new skills.

    The Single Server deployment option offers three pricing tiers: Basic, General Purpose, and Memory Optimized. Each tier offers different resource capabilities to support your database workloads. You can build your first app on a small database for a few dollars a month, and then adjust the scale to meet the needs of your solution. Dynamic scalability enables your database to transparently respond to rapidly changing resource requirements. You only pay for the resources you need, and only when you need them

    **Hyperscale (Citus)**

    The Hyperscale (Citus) option horizontally scales queries across multiple machines by using sharding. Its query engine parallelizes incoming SQL queries across these servers for faster responses on large datasets. It serves applications that require greater scale and performance, generally workloads that are approaching, or already exceed, 100 GB of data.

    The Hyperscale (Citus) deployment option supports multi-tenant applications, real-time operational analytics, and high throughput transactional workloads. Applications built for PostgreSQL can run distributed queries on Hyperscale (Citus) with standard connection libraries and minimal changes.

18. describe the benefits and usage of SQL Managed Instance [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/azure-database-fundamentals/azure-sql-managed-instance)

    Azure SQL Managed Instance is a scalable cloud data service that provides the broadest SQL Server database engine compatibility with all the benefits of a fully managed platform as a service. Depending on your scenario, Azure SQL Managed Instance might offer more options for your database needs.

    **Features**

    Like Azure SQL Database, Azure SQL Managed Instance is a platform as a service (PaaS) database engine, which means that your company will be able to take advantage of the best features of moving your data to the cloud in a fully-managed environment. For example, your company will no longer need to purchase and manage expensive hardware, and you won't have to maintain the additional overhead of managing your on-premises infrastructure. On the other hand, your company will benefit from the quick provisioning and service scaling features of Azure, together with automated patching and version upgrades. In addition, you'll be able to rest assured that your data will always be there when you need it through built-in high availability features and a 99.99% uptime service level agreement (SLA). You'll also be able to protect your data with automated backups and a configurable backup retention period.

    Azure SQL Database and Azure SQL Managed Instance offer many of the same features; however, Azure SQL Managed Instance provides several options that might not be available to Azure SQL Database. For example, Tailwind Traders currently uses several on-premises servers running SQL Server, and they would like to migrate their existing databases to a SQL database running in the cloud. However, several of their databases use Cyrillic characters for collation. In this scenario, Tailwind Traders should migrate their databases to an Azure SQL Managed Instance, since Azure SQL Database only uses the default SQL_Latin1_General_CP1_CI_AS server collation.

    **Migration**

    Azure SQL Managed Instance makes it easy to migrate your on-premises data on SQL Server to the cloud using the Azure Database Migration Service (DMS) or native backup and restore. After you have discovered all of the features that your company uses, you need to assess which on-premises SQL Server instances you can migrate to Azure SQL Managed Instance to see if you have any blocking issues. Once you have resolved any issues, you can migrate your data, then cutover from your on-premises SQL Server to your Azure SQL Managed Instance by changing the connection string in your applications.

19. describe the benefits and usage of Azure Marketplace [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/intro-to-azure-fundamentals/what-is-microsoft-azure)

Azure Marketplace helps connect users with Microsoft partners, independent software vendors, and startups that are offering their solutions and services, which are optimized to run on Azure. Azure Marketplace customers can find, try, purchase, and provision applications and services from hundreds of leading service providers. All solutions and services are certified to run on Azure.

## Describe core solutions and management tools on Azure (10-15%)

### Describe core solutions available in Azure

1. describe the benefits and usage of Azure Internet of Things (IoT) Hub [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/iot-fundamentals/2-identify-product-options)

   Azure IoT Hub is a managed service that's hosted in the cloud and that acts as a central message hub for bi-directional communication between your IoT application and the devices it manages. You can use Azure IoT Hub to build IoT solutions with reliable and secure communications between millions of IoT devices and a cloud-hosted solution back end. You can connect virtually any device to your IoT hub.

   The IoT Hub service supports communications both from the device to the cloud and from the cloud to the device. It also supports multiple messaging patterns, such as device-to-cloud telemetry, file upload from devices, and request-reply methods to control your devices from the cloud. After an IoT hub receives messages from a device, it can route that message to other Azure services.

   From a cloud-to-device perspective, IoT Hub allows for command and control. That is, you can have either manual or automated remote control of connected devices, so you can instruct the device to open valves, set target temperatures, restart stuck devices, and so on.

   IoT Hub monitoring helps you maintain the health of your solution by tracking events such as device creation, device failures, and device connections.

2. describe the benefits and usage of Azure Internet of IoT Central [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/iot-fundamentals/2-identify-product-options)

   Azure IoT Central builds on top of IoT Hub by adding a dashboard that allows you to connect, monitor, and manage your IoT devices. The visual user interface (UI) makes it easy to quickly connect new devices and watch as they begin sending telemetry or error messages. You can watch the overall performance across all devices in aggregate, and you can set up alerts that send notifications when a specific device needs maintenance. Finally, you can push firmware updates to the device.

   To help you get up and running quickly, IoT Central provides starter templates for common scenarios across various industries, such as retail, energy, healthcare, and government. You then customize the design starter templates directly in the UI by choosing from existing themes or creating your own custom theme, setting the logo, and so on. With IoT Central, you can tailor the starter templates for the specific data that's sent from your devices, the reports you want to see, and the alerts you want to send.

   You can use the UI to control your devices remotely. This feature allows you to push a software update or modify a property of the device. You can adjust the desired temperature for one or all of your refrigerated vending machines from directly inside of IoT Central.

   A key part of IoT Central is the use of device templates. By using a device template, you can connect a device without any service-side coding. IoT Central uses the templates to construct the dashboards, alerts, and so on. Device developers still need to create code to run on the devices, and that code must match the device template specification.

3. describe the benefits and usage of Azure Sphere [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/iot-fundamentals/2-identify-product-options)
  
   Azure Sphere creates an end-to-end, highly secure IoT solution for customers that encompasses everything from the hardware and operating system on the device to the secure method of sending messages from the device to the message hub. Azure Sphere has built-in communication and security features for internet-connected devices.

   Azure Sphere comes in three parts:

   * The first part is the Azure Sphere micro-controller unit (MCU), which is responsible for processing the operating system and signals from attached sensors. The following image displays the Seeed Azure Sphere MT3620 Development Kit MCU, one of several different starter kits that are available for prototyping and developing Azure Sphere applications.
   * The second part is a customized Linux operating system (OS) that handles communication with the security service and can run the vendor's software.
   * The third part is Azure Sphere Security Service, also known as AS3. Its job is to make sure that the device has not been maliciously compromised. When the device attempts to connect to Azure, it first must authenticate itself, per device, which it does by using certificate-based authentication. If it authenticates successfully, AS3 checks to ensure that the device hasn't been tampered with. After it has established a secure channel of communication, AS3 pushes any OS or approved customer-developed software updates to the device.
  
  After the Azure Sphere system has validated the authenticity of the device and authenticated it, the device can interact with other Azure IoT services by sending telemetry and error information.

4. describe the benefits and usage of Azure Synapse Analytics [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/azure-database-fundamentals/azure-big-data-analytics)

   Azure Synapse Analytics (formerly Azure SQL Data Warehouse) is a limitless analytics service that brings together enterprise data warehousing and big data analytics. You can query data on your terms by using either serverless or provisioned resources at scale. You have a unified experience to ingest, prepare, manage, and serve data for immediate BI and machine learning needs.

5. describe the benefits and usage of HDInsight [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/azure-database-fundamentals/azure-big-data-analytics)

   Azure HDInsight is a fully managed, open-source analytics service for enterprises. It's a cloud service that makes it easier, faster, and more cost-effective to process massive amounts of data. You can run popular open-source frameworks and create cluster types such as Apache Spark, Apache Hadoop, Apache Kafka, Apache HBase, Apache Storm, and Machine Learning Services. HDInsight also supports a broad range of scenarios such as extraction, transformation, and loading (ETL), data warehousing, machine learning, and IoT.

6. describe the benefits and usage of Azure Databricks [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/azure-database-fundamentals/azure-big-data-analytics)
   
   Azure HDInsight is a fully managed, open-source analytics service for enterprises. It's a cloud service that makes it easier, faster, and more cost-effective to process massive amounts of data. You can run popular open-source frameworks and create cluster types such as Apache Spark, Apache Hadoop, Apache Kafka, Apache HBase, Apache Storm, and Machine Learning Services. HDInsight also supports a broad range of scenarios such as extraction, transformation, and loading (ETL), data warehousing, machine learning, and IoT.
   
7. describe the benefits and usage of Azure Machine Learning [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/ai-machine-learning-fundamentals/2-identify-product-options)

   Azure Machine Learning is a platform for making predictions. It consists of tools and services that allow you to connect to data to train and test models to find one that will most accurately predict a future result. After you've run experiments to test the model, you can deploy and use it in real time via a web API endpoint.

   With Azure Machine Learning, you can:
   * Create a process that defines how to obtain data, how to handle missing or bad data, how to split the data into either a training set or test set, and deliver the data to the training process.
   * Train and evaluate predictive models by using tools and programming languages familiar to data scientists.
   * Create pipelines that define where and when to run the compute-intensive experiments that are required to score the algorithms based on the training and test data.
   * Deploy the best-performing algorithm as an API to an endpoint so it can be consumed in real time by other applications.

    Choose Azure Machine Learning when your data scientists need complete control over the design and training of an algorithm using your own data. The following video discusses the basic steps required to set up a machine learning system.

8.  describe the benefits and usage of Azure Cognitive Services [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/ai-machine-learning-fundamentals/2-identify-product-options)

   Azure Cognitive Services provides prebuilt machine learning models that enable applications to see, hear, speak, understand, and even begin to reason. Use Azure Cognitive Services to solve general problems, such as analyzing text for emotional sentiment or analyzing images to recognize objects or faces. You don't need special machine learning or data science knowledge to use these services. Developers access Azure Cognitive Services via APIs and can easily include these features in just a few lines of code.

   While Azure Machine Learning requires you to bring your own data and train models over that data, Azure Cognitive Services, for the most part, provides pretrained models so that you can bring in your live data to get predictions on.

   Azure Cognitive Services can be divided into the following categories:

   * Language services: Allow your apps to process natural language with prebuilt scripts, evaluate sentiment, and learn how to recognize what users want.
   * Speech services: Convert speech into text and text into natural-sounding speech. Translate from one language to another and enable speaker verification and recognition.
   * Vision services: Add recognition and identification capabilities when you're analyzing pictures, videos, and other visual content.
   * Decision services: Add personalized recommendations for each user that automatically improve each time they're used, moderate content to monitor and remove offensive or risky content, and detect abnormalities in your time series data.

11. describe the benefits and usage of Azure Bot Service [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/ai-machine-learning-fundamentals/2-identify-product-options)

    Azure Bot Service and Bot Framework are platforms for creating virtual agents that understand and reply to questions just like a human. Azure Bot Service is a bit different from Azure Machine Learning and Azure Cognitive Services in that it has a specific use case. Namely, it creates a virtual agent that can intelligently communicate with humans. Behind the scenes, the bot you build uses other Azure services, such as Azure Cognitive Services, to understand what their human counterparts are asking for.

    Bots can be used to shift simple, repetitive tasks, such as taking a dinner reservation or gathering profile information, on to automated systems that might no longer require direct human intervention. Users converse with a bot by using text, interactive cards, and speech. A bot interaction can be a quick question and answer, or it can be a sophisticated conversation that intelligently provides access to services.

12. describe the benefits and usage of serverless computing solutions that include Azure Functions [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/serverless-fundamentals/2-identify-product-options)

    With the Azure Functions service, you can host a single method or function by using a popular programming language in the cloud that runs in response to an event. An example of an event might be an HTTP request, a new message on a queue, or a message on a timer.

    Because of its atomic nature, Azure Functions can serve many purposes in an application's design. Functions can be written in many common programming languages, such as C#, Python, JavaScript, Typescript, Java, and PowerShell.

    Azure Functions scales automatically, and charges accrue only when a function is triggered. These qualities make Azure Functions a solid choice when demand is variable. For example, you might be receiving messages from an IoT solution that monitors a fleet of delivery vehicles. You'll likely have more data arriving during business hours. Azure Functions can scale out to accommodate these busier times.

    An Azure function is a stateless environment. A function behaves as if it's restarted every time it responds to an event. This feature is ideal for processing incoming data. And if state is required, the function can be connected to an Azure storage account.

    Azure Functions can perform orchestration tasks by using an extension called Durable Functions, which allow developers to chain functions together while maintaining state.

    The Azure Functions solution is ideal when you're concerned only with the code that's running your service and not the underlying platform or infrastructure. You use Azure Functions most commonly when you need to perform work in response to an event. You do this often via a REST request, timer, or message from another Azure service, and when that work can be completed quickly, within seconds or less.

13. describe the benefits and usage of serverless computing solutions that include Azure Logic Apps [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/serverless-fundamentals/2-identify-product-options)

    Logic Apps is a low-code/no-code development platform hosted as a cloud service. The service helps you automate and orchestrate tasks, business processes, and workflows when you need to integrate apps, data, systems, and services across enterprises or organizations. Logic Apps simplifies how you design and build scalable solutions, whether in the cloud, on-premises, or both. This solution covers app integration, data integration, system integration, enterprise application integration (EAI), and business-to-business (B2B) integration.

    Azure Logic Apps is designed in a web-based designer and can execute logic that's triggered by Azure services without writing any code. You build an app by linking triggers to actions with connectors. A trigger is an event (such as a timer) that causes an app to execute, then a new message to be sent to a queue, or an HTTP request. An action is a task or step that can execute. There are logic actions such as those you would find in most programming languages. Examples of actions include working with variables, decision statements and loops, and tasks that parse and modify data.

    To build enterprise integration solutions with Azure Logic Apps, you can choose from a growing gallery of over 200 connectors. The gallery includes services such as Salesforce, SAP, Oracle DB, and file shares.

    If you can't find the action or connector you need, you can build your own by using custom code.

14. describe the benefits and usage of Azure DevOps [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/azure-devops-devtest-labs/2-identify-product-options)

    Azure DevOps Services is a suite of services that address every stage of the software development lifecycle.

    * Azure Repos is a centralized source-code repository where software development, DevOps engineering, and documentation professionals can publish their code for review and collaboration.
    * Azure Boards is an agile project management suite that includes Kanban boards, reporting, and tracking ideas and work from high-level epics to work items and issues.
    * Azure Pipelines is a CI/CD pipeline automation tool.
    * Azure Artifacts is a repository for hosting artifacts, such as compiled source code, which can be fed into testing or deployment pipeline steps.
    * Azure Test Plans is an automated test tool that can be used in a CI/CD pipeline to ensure quality before a software release.
    * Azure DevOps is a mature tool with a large feature set that began as on-premises server software and evolved into a software as a service (SaaS) offering from Microsoft.
  
15. describe the benefits and usage of GitHub [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/ai-machine-learning-fundamentals/2-identify-product-options)

    GitHub is arguably the world's most popular code repository for open-source software. Git is a decentralized source-code management tool, and GitHub is a hosted version of Git that serves as the primary remote. GitHub builds on top of Git to provide related services for coordinating work, reporting and discussing issues, providing documentation, and more. It offers the following functionality:

    * It's a shared source-code repository, including tools that enable developers to perform code reviews by adding comments and questions in a web view of the source code before it can be merged into the main code base.
    * It facilitates project management, including Kanban boards.
    * It supports issue reporting, discussion, and tracking.
    * It features CI/CD pipeline automation tooling.
    * It includes a wiki for collaborative documentation.
    * It can be run from the cloud or on-premises

With such similarity between many GitHub and Azure DevOps features, you might wonder which product to choose for your organization. Unfortunately, the answer might not be straightforward.

Although both Azure DevOps and GitHub allow public and private code repositories, GitHub has a long history with public repositories and is trusted by tens of thousands of open-source project owners. GitHub is a lighter-weight tool than Azure DevOps, with a focus on individual developers contributing to the open-source code. Azure DevOps, on the other hand, is more focused on enterprise development, with heavier project-management and planning tools, and finer-grained access control.

16. describe the benefits and usage of GitHub Actions [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/ai-machine-learning-fundamentals/2-identify-product-options)

    GitHub Actions enables workflow automation with triggers for many lifecycle events. One such example would be automating a CI/CD toolchain.

    A toolchain is a combination of software tools that aid in the delivery, development, and management of software applications throughout a system's development lifecycle. The output of one tool in the toolchain is the input of the next tool in the toolchain. Typical tool functions range from performing automated dependency updates to building and configuring the software, delivering the build artifacts to various locations, testing, and so on.

17. describe the benefits and usage of Azure DevTest Labs [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/ai-machine-learning-fundamentals/2-identify-product-options)

    Azure DevTest Labs provides an automated means of managing the process of building, setting up, and tearing down virtual machines (VMs) that contain builds of your software projects. This way, developers and testers can perform tests across a variety of environments and builds. And this capability isn't limited to VMs. Anything you can deploy in Azure via an ARM template can be provisioned through DevTest Labs. Provisioning pre-created lab environments with their required configurations and tools already installed is a huge time saver for quality assurance professionals and developers.

    Suppose you need to test a new feature on an old version of an operating system. Azure DevTest Labs can set up everything automatically upon request. After the testing is complete, DevTest Labs can shut down and deprovision the VM, which saves money when it's not in use. To control costs, the management team can restrict how many labs can be created, how long they run, and so on.

### Describe Azure management tools

1. describe the functionality and usage of the Azure Portal [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/management-fundamentals/2-identify-product-options)
   The Azure portal is a web-based user interface that allows access to virtually every feature of Azure. The Azure portal provides a friendly, graphical UI to view all the services you're using, create new services, configure your services, and view reports. The Azure portal is how most users first experience Azure. But, as your Azure usage grows, you'll likely choose a more repeatable code-centric approach to managing your Azure resources.

2. describe the functionality and usage of the Azure PowerShell [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/management-fundamentals/2-identify-product-options)

   Azure PowerShell is a shell with which developers and DevOps and IT professionals can execute commands called cmdlets (pronounced command-lets). These commands call the Azure Rest API to perform every possible management task in Azure. Cmdlets can be executed independently or combined into a script file and executed together to orchestrate:

   * The routine setup, teardown, and maintenance of a single resource or multiple connected resources.
   * The deployment of an entire infrastructure, which might contain dozens or hundreds of resources, from imperative code.

  Capturing the commands in a script makes the process repeatable and automatable.

  Azure PowerShell is available for Windows, Linux, and Mac, and you can access it in a web browser via Azure Cloud Shell.

  Windows PowerShell has helped Windows-centric IT organizations automate many of their on-premises operations for years, and these organizations have built up a large catalog of custom scripts and cmdlets, as well as expertise.

3. describe the functionality and usage of the Azure CLI [Microsoft Learn Reference] [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/management-fundamentals/2-identify-product-options)

   The Azure CLI command-line interface is an executable program with which a developer, DevOps professional, or IT professional can execute commands in Bash. The commands call the Azure Rest API to perform every possible management task in Azure. You can run the commands independently or combined into a script and executed together for the routine setup, teardown, and maintenance of a single resource or an entire environment.

   In many respects, the Azure CLI is almost identical to Azure PowerShell in what you can do with it. Both run on Windows, Linux, and Mac, and can be accessed in a web browser via Cloud Shell. The primary difference is the syntax you use. If you're already proficient in PowerShell or Bash, you can use the tool you prefer.

4. describe the functionality and usage of the Azure Cloud Shell [Microsoft Documentation Reference](https://docs.microsoft.com/en-us/azure/cloud-shell/overview)

   Azure Cloud Shell is an interactive, authenticated, browser-accessible shell for managing Azure resources. It provides the flexibility of choosing the shell experience that best suits the way you work, either Bash or PowerShell.

   **Browser-based shell experience**

   Cloud Shell enables access to a browser-based command-line experience built with Azure management tasks in mind. Leverage Cloud Shell to work untethered from a local machine in a way only the cloud can provide.

   **Authenticated and configured Azure workstation**

   Cloud Shell is managed by Microsoft so it comes with popular command-line tools and language support. Cloud Shell also securely authenticates automatically for instant access to your resources through the Azure CLI or Azure PowerShell cmdlets.

   **Integrated Cloud Shell editor**

   Cloud Shell offers an integrated graphical text editor based on the open-source Monaco Editor. Simply create and edit configuration files by running code . for seamless deployment through Azure CLI or Azure PowerShell.

5. describe the functionality and usage of the Azure Mobile App [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/management-fundamentals/2-identify-product-options)

   The Azure mobile app provides iOS and Android access to your Azure resources when you're away from your computer. With it, you can:

   * Monitor the health and status of your Azure resources.
   * Check for alerts, quickly diagnose and fix issues, and restart a web app or virtual machine (VM).
   * Run the Azure CLI or Azure PowerShell commands to manage your Azure resources.

6. describe the functionality and usage of Azure Advisor [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/monitoring-fundamentals/2-identify-product-options)
   Azure Advisor evaluates your Azure resources and makes recommendations to help improve reliability, security, and performance, achieve operational excellence, and reduce costs. Advisor is designed to help you save time on cloud optimization. The recommendation service includes suggested actions you can take right away, postpone, or dismiss.

   The recommendations are available via the Azure portal and the API, and you can set up notifications to alert you to new recommendations.

   When you're in the Azure portal, the Advisor dashboard displays personalized recommendations for all your subscriptions, and you can use filters to select recommendations for specific subscriptions, resource groups, or services. The recommendations are divided into five categories:

   * Reliability: Used to ensure and improve the continuity of your business-critical applications.
   * Security: Used to detect threats and vulnerabilities that might lead to security breaches.
   * Performance: Used to improve the speed of your applications.
   * Cost: Used to optimize and reduce your overall Azure spending.
   * Operational Excellence: Used to help you achieve process and workflow efficiency, resource manageability, and deployment best practices.

7. describe the functionality and usage of Azure Resource Manager (ARM) templates [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/management-fundamentals/2-identify-product-options)

   Although it's possible to write imperative code in Azure PowerShell or the Azure CLI to set up and tear down one Azure resource or orchestrate an infrastructure comprising hundreds of resources, there's a better way to implement this functionality.

   By using Azure Resource Manager templates (ARM templates), you can describe the resources you want to use in a declarative JSON format. The benefit is that the entire ARM template is verified before any code is executed to ensure that the resources will be created and connected correctly. The template then orchestrates the creation of those resources in parallel. That is, if you need 50 instances of the same resource, all 50 instances are created at the same time.

   Ultimately, the developer, DevOps professional, or IT professional needs only to define the desired state and configuration of each resource in the ARM template, and the template does the rest. Templates can even execute PowerShell and Bash scripts before or after the resource has been set up.

8. describe the functionality and usage of Azure Monitor [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/monitoring-fundamentals/2-identify-product-options)

   Azure Monitor is a platform for collecting, analyzing, visualizing, and potentially taking action based on the metric and logging data from your entire Azure and on-premises environment.

   The following diagram illustrates just how comprehensive Azure Monitor is.
   ![Azure shared responsibility model](/assets/pages/2021-04-07-az-900-azure-fundamentals-preparation/2-identify-product-options-01.png)

   * On the left is a list of the sources of logging and metric data that can be collected at every layer in your application architecture, from application to operating system and network.
   * In the center, you can see how the logging and metric data is stored in central repositories.
   * On the right, the data is used in a number of ways. You can view real-time and historical performance across each layer of your architecture, or aggregated and detailed information. The data is displayed at different levels for different audiences. You can view high-level reports on the Azure Monitor Dashboard or create custom views by using Power BI and Kusto queries.

    Additionally, you can use the data to help you react to critical events in real time, through alerts delivered to teams via SMS, email, and so on. Or you can use thresholds to trigger autoscaling functionality to scale up or down to meet the demand.

    Some popular products such as Azure Application Insights, a service for sending telemetry information from application source code to Azure, uses Azure Monitor under the hood. With Application Insights, your application developers can take advantage of the powerful data-analysis platform in Azure Monitor to gain deep insights into an application's operations and diagnose errors without having to wait for users to report them.

9.  describe the functionality and usage of Azure Service Health [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/monitoring-fundamentals/2-identify-product-options)

    Azure Service Health provides a personalized view of the health of the Azure services, regions, and resources you rely on. The status.azure.com website, which displays only major issues that broadly affect Azure customers, doesn't provide the full picture. But Azure Service Health displays both major and smaller, localized issues that affect you. Service issues are rare, but it's important to be prepared for the unexpected. You can set up alerts that help you triage outages and planned maintenance. After an outage, Service Health provides official incident reports, called root cause analyses (RCAs), which you can share with stakeholders.

    Service Health helps you keep an eye on several event types:

    * Service issues are problems in Azure, such as outages, that affect you right now. You can drill down to the affected services, regions, updates from your engineering teams, and find ways to share and track the latest information.
    * Planned maintenance events can affect your availability. You can drill down to the affected services, regions, and details to show how an event will affect you and what you need to do. Most of these events occur without any impact to you and aren't shown here. In the rare case that a reboot is required, Service Health allows you to choose when to perform the maintenance to minimize the downtime.
    * Health advisories are issues that require you to act to avoid service interruption, including service retirements and breaking changes. Health advisories are announced far in advance to allow you to plan.

## Describe general security and network security features (10-15%)

### Describe Azure security features

1. describe basic features of Azure Security Center, including policy compliance, security alerts, secure score, and resource hygiene [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/protect-against-security-threats-azure/2-protect-threats-security-center)

   Azure Security Center is a monitoring service that provides visibility of your security posture across all of your services, both on Azure and on-premises. The term security posture refers to cybersecurity policies and controls, as well as how well you can predict, prevent, and respond to security threats.

   Security Center can:

   * Monitor security settings across on-premises and cloud workloads.
   * Automatically apply required security settings to new resources as they come online
   * Provide security recommendations that are based on your current configurations, resources, and networks.
   * Continuously monitor your resources and perform automatic security assessments to identify potential vulnerabilities before those vulnerabilities can be exploited.
   * Use machine learning to detect and block malware from being installed on your virtual machines (VMs) and other resources. You can also use adaptive application controls to define rules that list allowed applications to ensure that only applications you allow can run.
   * Detect and analyze potential inbound attacks and investigate threats and any post-breach activity that might have occurred.
   * Provide just-in-time access control for network ports. Doing so reduces your attack surface by ensuring that the network only allows traffic that you require at the time that you need it to.
  
    **Understand your security posture**

    Security Center can be used to get a detailed analysis of different components in its environment. Because the company's resources are analyzed against the security controls of any governance policies it has assigned, it can view its overall regulatory compliance from a security perspective all from one place.

    In the Resource security hygiene section, an Azure tenant can see the health of its resources from a security perspective. To help prioritize remediation actions, recommendations are categorized as low, medium, and high

    **What's secure score?**
    The Secure score is a measurement of an organization's security posture. It is based on security controls, or groups of related security recommendations. Your score is based on the percentage of security controls that you satisfy. The more security controls you satisfy, the higher the score you receive. Your score improves when you remediate all of the recommendations for a single resource within a control.

    Following the secure score recommendations can help protect your organization from threats. From a centralized dashboard in Azure Security Center, organizations can monitor and work on the security of their Azure resources like identities, data, apps, devices, and infrastructure.

    Secure score helps you:

    * Report on the current state of your organization's security posture.
    * Improve your security posture by providing discoverability, visibility, guidance, and control.
    * Compare with benchmarks and establish key performance indicators (KPIs).

    **Protect against threats**

    Security Center includes advanced cloud defense capabilities for VMs, network security, and file integrity. The following are some of these capabilities:

    * Just-in-time VM access: The organization can configure just-in-time access to VMs. This access blocks traffic by default to specific network ports of VMs, but allows traffic for a specified time when an admin requests and approves it.
    * Adaptive application controls: The organization can control which applications are allowed to run on its VMs. In the background, Security Center uses machine learning to look at the processes running on a VM. It creates exception rules for each resource group that holds the VMs and provides recommendations. This process provides alerts that inform the company about unauthorized applications that are running on its VMs
    * Adaptive network hardening: Security Center can monitor the internet traffic patterns of the VMs, and compare those patterns with the company's current network security group (NSG) settings. From there, Security Center can make recommendations about whether the NSGs should be locked down further and provide remediation steps.
    * File integrity monitoring: The organization can also configure the monitoring of changes to important files on both Windows and Linux, registry settings, applications, and other aspects that might indicate a security attack.
  
    **Respond to security alerts**

    An organization can use Security Center to get a centralized view of all of its security alerts. From there, the company can dismiss false alerts, investigate them further, remediate alerts manually, or use an automated response with a workflow automation.

    Workflow automation uses Azure Logic Apps and Security Center connectors. The logic app can be triggered by a threat detection alert or by a Security Center recommendation, filtered by name or by severity. You can then configure the logic app to run an action, such as sending an email, or posting a message to a Microsoft Teams channel.

2. describe the functionality and usage of Key Vault [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/protect-against-security-threats-azure/4-manage-secrets-key-vault)

   Azure Key Vault is a centralized cloud service for storing an application's secrets in a single, central location. It provides secure access to sensitive information by providing access control and logging capabilities.

   **What can Azure Key Vault do?**
   Azure Key Vault can help you:

   * Manage secrets: You can use Key Vault to securely store and tightly control access to tokens, passwords, certificates, API keys, and other secrets.
   * Manage encryption keys: You can use Key Vault as a key management solution. Key Vault makes it easier to create and control the encryption keys that are used to encrypt your data.
   * Manage SSL/TLS certificates: Key Vault enables you to provision, manage, and deploy your public and private Secure Sockets Layer/Transport Layer Security (SSL/TLS) certificates for both your Azure resources and your internal resources.
   * Store secrets backed by hardware security modules (HSMs): These secrets and keys can be protected either by software or by FIPS 140-2 Level 2 validated HSMs.

   **What are the benefits of Azure Key Vault?**

   The benefits of using Key Vault include:

   * Centralized application secrets: Centralizing the storage for your application secrets enables you to control their distribution, and reduces the chances that secrets are accidentally leaked.
   * Securely stored secrets and keys: Azure uses industry-standard algorithms, key lengths, and HSMs. Access to Key Vault requires proper authentication and authorization.
   * Access monitoring and access control: By using Key Vault, you can monitor and control access to your application secrets.
   * Simplified administration of application secrets: Key Vault makes it easier to enroll and renew certificates from public certificate authorities (CAs). You can also scale up and replicate content within regions and use standard certificate management tools.
   * Integration with other Azure services: You can integrate Key Vault with storage accounts, container registries, event hubs, and many more Azure services. These services can then securely reference the secrets stored in Key Vault.

3. describe the functionality and usage of Azure Sentinel [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/protect-against-security-threats-azure/3-detect-respond-threats-sentinel)

   Security management on a large scale can benefit from a dedicated security information and event management (SIEM) system. A SIEM system aggregates security data from many different sources (as long as those sources support an open-standard logging format). It also provides capabilities for threat detection and response.

   Azure Sentinel is Microsoft's cloud-based SIEM system. It uses intelligent security analytics and threat analysis.

   Azure Sentinel enables you to:

   * Collect cloud data at scale: Collect data across all users, devices, applications, and infrastructure, both on-premises and from multiple clouds.
   * Detect previously undetected threats: Minimize false positives by using Microsoft's comprehensive analytics and threat intelligence.
   * Investigate threats with artificial intelligence: Examine suspicious activities at scale, tapping into years of cybersecurity experience from Microsoft.
   * Respond to incidents rapidly: Use built-in orchestration and automation of common tasks.

   **Connect your data sources**

   Azure Sentinel supports a number of data sources, which it can analyze for security events. These connections are handled by built-in connectors or industry-standard log formats and APIs.

   * Connect Microsoft solutions: Connectors provide real-time integration for services like Microsoft Threat Protection solutions, Microsoft 365 sources (including Office 365), Azure Active Directory, and Windows Defender Firewall.
   * Connect other services and solutions: Connectors are available for common non-Microsoft services and solutions, including AWS CloudTrail, Citrix Analytics (Security), Sophos XG Firewall, VMware Carbon Black Cloud, and Okta SSO.
   * Connect industry-standard data sources: Azure Sentinel supports data from other sources that use the Common Event Format (CEF) messaging standard, Syslog, or REST API.

   **Detect threats**

   Azure Sentinel supports notification when something suspicious occurs. This can be done through the built-in analytics and custom rules to detect threats.

   Built in analytics use templates designed by Microsoft's team of security experts and analysts based on known threats, common attack vectors, and escalation chains for suspicious activity. These templates can be customized and search across the environment for any activity that looks suspicious. Some templates use machine learning behavioral analytics that are based on Microsoft proprietary algorithms.

   Custom analytics are rules that you create to search for specific criteria within your environment. You can preview the number of results that the query would generate (based on past log events) and set a schedule for the query to run. You can also set an alert threshold.

   **Investigate and respond**

   When Azure Sentinel detects suspicious events, the Azure tenant can investigate specific alerts or incidents (a group of related alerts). With the investigation graph, the company can review information from entities directly connected to the alert, and see common exploration queries to help guide the investigation.

   The company can also use Azure Monitor Workbooks to automate responses to threats. For example, it can set an alert that looks for malicious IP addresses that access the network and create a workbook that does the following steps:
   * When the alert is triggered, open a ticket in the IT ticketing system.
   * Send a message to the security operations channel in Microsoft Teams or Slack to make sure the security analysts are aware of the incident.
   * Send all of the information in the alert to the senior network admin and to the security admin. The email message includes two user option buttons: Block or Ignore.
  
   When an admin chooses Block, the IP address is blocked in the firewall, and the user is disabled in Azure Active Directory. When an admin chooses Ignore, the alert is closed in Azure Sentinel, and the incident is closed in the IT ticketing system.

   The workbook continues to run after it receives a response from the admins.

   Workbooks can be run manually or automatically when a rule triggers an alert.

4. describe the functionality and usage of Azure Dedicated Hosts [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/monitoring-fundamentals/2-identify-product-options)

   On Azure, virtual machines (VMs) run on shared hardware that Microsoft manages. Although the underlying hardware is shared, your VM workloads are isolated from workloads that other Azure customers run.

   Some organizations must follow regulatory compliance that requires them to be the only customer using the physical machine that hosts their virtual machines. Azure Dedicated Host provides dedicated physical servers to host your Azure VMs for Windows and Linux.

   Here's a diagram that shows how VMs relate to dedicated hosts and host groups. A dedicated host is mapped to a physical server in an Azure datacenter. A host group is a collection of dedicated hosts.
   ![Azure Dedicated Host](/assets/pages/2021-04-07-az-900-azure-fundamentals-preparation/6-dedicated-hosts.png)

   **What are the benefits of Azure Dedicated Host?**

   Azure Dedicated Host:
   * Gives you visibility into, and control over, the server infrastructure that's running your Azure VMs.
   * Helps address compliance requirements by deploying your workloads on an isolated server.
   * Lets you choose the number of processors, server capabilities, VM series, and VM sizes within the same host.

   **Availability considerations for Dedicated Host**

   After a dedicated host is provisioned, Azure assigns it to the physical server in Microsoft's cloud datacenter.

   For high availability, you can provision multiple hosts in a host group, and deploy your VMs across this group. VMs on dedicated hosts can also take advantage of maintenance control. This feature enables you to control when regular maintenance updates occur, within a 35-day rolling window.

   **Pricing considerations**

   You're charged per dedicated host, independent of how many VMs you deploy to it. The host price is based on the VM family, type (hardware size), and region.

   Software licensing, storage, and network usage are billed separately from the host and VMs. For more information. see Azure Dedicated Host pricing.

### Describe Azure network security

1. describe the concept of defense in depth [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/secure-network-connectivity-azure/2-what-is-defense-in-depth)

   The objective of defense in depth is to protect information and prevent it from being stolen by those who aren't authorized to access it.

   A defense-in-depth strategy uses a series of mechanisms to slow the advance of an attack that aims at acquiring unauthorized access to data.

   **Layers of defense in depth**

   You can visualize defense in depth as a set of layers, with the data to be secured at the center.
   ![Layers of Defense](/assets/pages/2021-04-07-az-900-azure-fundamentals-preparation/2-defense-depth.png)

   Each layer provides protection so that if one layer is breached, a subsequent layer is already in place to prevent further exposure. This approach removes reliance on any single layer of protection. It slows down an attack and provides alert telemetry that security teams can act upon, either automatically or manually.

   Here's a brief overview of the role of each layer:

   * The physical security layer is the first line of defense to protect computing hardware in the datacenter.
   * The identity and access layer controls access to infrastructure and change control.
   * The perimeter layer uses distributed denial of service (DDoS) protection to filter large-scale attacks before they can cause a denial of service for users.
   * The network layer limits communication between resources through segmentation and access controls.
   * The compute layer secures access to virtual machines.
   * The application layer helps ensure that applications are secure and free of security vulnerabilities.
   * The data layer controls access to business and customer data that you need to protect.

   These layers provide a guideline for you to help make security configuration decisions in all of the layers of your applications.

   Azure provides security tools and features at every level of the defense-in-depth concept. Let's take a closer look at each layer:

   *Physical security*

   Physically securing access to buildings and controlling access to computing hardware within the datacenter are the first line of defense.

   With physical security, the intent is to provide physical safeguards against access to assets. These safeguards ensure that other layers can't be bypassed, and loss or theft is handled appropriately. Microsoft uses various physical security mechanisms in its cloud datacenters.

   *Identity and access*

   At this layer, it's important to:

   * Control access to infrastructure and change control.
   * Use single sign-on (SSO) and multifactor authentication.
   * Audit events and changes.
  
   The identity and access layer is all about ensuring that identities are secure, access is granted only to what's needed, and sign-in events and changes are logged.

   *Perimeter*

   At this layer, it's important to:

   * Use DDoS protection to filter large-scale attacks before they can affect the availability of a system for users.
   * Use perimeter firewalls to identify and alert on malicious attacks against your network.
  
   At the network perimeter, it's about protecting from network-based attacks against your resources. Identifying these attacks, eliminating their impact, and alerting you when they happen are important ways to keep your network secure.

   *Network*

   At this layer, it's important to:

   * Limit communication between resources.
   * Deny by default.
   * Restrict inbound internet access and limit outbound access where appropriate.
   * Implement secure connectivity to on-premises networks.

   At this layer, the focus is on limiting the network connectivity across all your resources to allow only what's required. By limiting this communication, you reduce the risk of an attack spreading to other systems in your network.

   *Compute*

   At this layer, it's important to:

   * Secure access to virtual machines.
   * Implement endpoint protection on devices and keep systems patched and current.

   Malware, unpatched systems, and improperly secured systems open your environment to attacks. The focus in this layer is on making sure that your compute resources are secure and that you have the proper controls in place to minimize security issues.

   *Application*

   At this layer, it's important to:

   * Ensure that applications are secure and free of vulnerabilities
   * Store sensitive application secrets in a secure storage medium.
   * Make security a design requirement for all application development.

   Integrating security into the application development lifecycle helps reduce the number of vulnerabilities introduced in code. Every development team should ensure that its applications are secure by default.

   *Data*

   In almost all cases, attackers are after data:

   * Stored in a database.
   * Stored on disk inside virtual machines.
   * Stored in software as a service (SaaS) applications, such as Office 365.
   * Managed through cloud storage.

   Those who store and control access to data are responsible for ensuring that it's properly secured. Often, regulatory requirements dictate the controls and processes that must be in place to ensure the confidentiality, integrity, and availability of the data.

   **Security posture**

   Your security posture is your organization's ability to protect from and respond to security threats. The common principles used to define a security posture are confidentiality, integrity, and availability, known collectively as CIA.

   *Confidentiality*

   The principle of least privilege means restricting access to information only to individuals explicitly granted access, at only the level that they need to perform their work. This information includes protection of user passwords, email content, and access levels to applications and underlying infrastructure.

   *Integrity*

   Prevent unauthorized changes to information:
   * At rest: when it's stored.
   * In transit: when it's being transferred from one place to another, including from a local computer to the cloud.

   A common approach used in data transmission is for the sender to create a unique fingerprint of the data by using a one-way hashing algorithm. The hash is sent to the receiver along with the data. The receiver recalculates the data's hash and compares it to the original to ensure that the data wasn't lost or modified in transit.

   *Availability*

   Ensure that services are functioning and can be accessed only by authorized users. Denial-of-service attacks are designed to degrade the availability of a system, affecting its users.

2. describe the functionality and usage of Network Security Groups (NSG) [Microsoft Learn Reference](hhttps://docs.microsoft.com/en-us/learn/modules/secure-network-connectivity-azure/5-filter-traffic-network-security-groups)

   A network security group enables you to filter network traffic to and from Azure resources within an Azure virtual network. You can think of NSGs like an internal firewall. An NSG can contain multiple inbound and outbound security rules that enable you to filter traffic to and from resources by source and destination IP address, port, and protocol.

   **How do I specify NSG rules?**

   A network security group can contain as many rules as you need, within Azure subscription limits. Each rule specifies these properties:

   | Property              | Description                                                                                                               |
   | --------------------- | ------------------------------------------------------------------------------------------------------------------------- |
   | Name                  | A unique name for the NSG.                                                                                                |
   | Priority              | A number between 100 and 4096. Rules are processed in priority order, with lower numbers processed before higher numbers. |
   | Source or Destination | A single IP address or IP address range, service tag, or application security group.                                      |
   | Protocol              | TCP, UDP, or Any.                                                                                                         |
   | Direction             | Whether the rule applies to inbound or outbound traffic.                                                                  |
   | Port Range            | A single port or range of ports.                                                                                          |
   | Action                | Allow or Deny.                                                                                                            |

   When you create a network security group, Azure creates a series of default rules to provide a baseline level of security. You can't remove the default rules, but you can override them by creating new rules with higher priorities.

3. describe the functionality and usage of Azure Firewall [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/secure-network-connectivity-azure/3-protect-network-azure-firewall)

   A firewall is a network security device that monitors incoming and outgoing network traffic and decides whether to allow or block specific traffic based on a defined set of security rules. You can create firewall rules that specify ranges of IP addresses. Only clients granted IP addresses from within those ranges are allowed to access the destination server. Firewall rules can also include specific network protocol and port information.

   Azure Firewall is a managed, cloud-based network security service that helps protect resources in your Azure virtual networks. A virtual network is similar to a traditional network that you'd operate in your own datacenter. It's a fundamental building block for your private network that enables virtual machines and other compute resources to securely communicate with each other, the internet, and on-premises networks.

   Azure Firewall is a stateful firewall. A stateful firewall analyzes the complete context of a network connection, not just an individual packet of network traffic. Azure Firewall features high availability and unrestricted cloud scalability.

   Azure Firewall provides a central location to create, enforce, and log application and network connectivity policies across subscriptions and virtual networks. Azure Firewall uses a static (unchanging) public IP address for your virtual network resources, which enables outside firewalls to identify traffic coming from your virtual network. The service is integrated with Azure Monitor to enable logging and analytics.

   Azure Firewall provides many features, including:

   * Built-in high availability.
   * Unrestricted cloud scalability.
   * Inbound and outbound filtering rules.
   * Inbound Destination Network Address Translation (DNAT) support.
   * Azure Monitor logging.

   You typically deploy Azure Firewall on a central virtual network to control general network access.

   **What can I configure with Azure Firewall?**

   With Azure Firewall, you can configure:

   * Application rules that define fully qualified domain names (FQDNs) that can be accessed from a subnet.
   * Network rules that define source address, protocol, destination port, and destination address.
   * Network Address Translation (NAT) rules that define destination IP addresses and ports to translate inbound requests.

   Azure Application Gateway also provides a firewall that's called the web application firewall (WAF). WAF provides centralized, inbound protection for your web applications against common exploits and vulnerabilities. Azure Front Door and Azure Content Delivery Network also provide WAF services.

4. describe the functionality and usage of Azure DDoS protection [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/secure-network-connectivity-azure/4-protect-attacks-azure-ddos-protection)

   A distributed denial of service attack attempts to overwhelm and exhaust an application's resources, making the application slow or unresponsive to legitimate users. DDoS attacks can target any resource that's publicly reachable through the internet, including websites.

   Azure DDoS Protection (Standard) helps protect your Azure resources from DDoS attacks.

   When you combine DDoS Protection with recommended application design practices, you help provide a defense against DDoS attacks. DDoS Protection uses the scale and elasticity of Microsoft's global network to bring DDoS mitigation capacity to every Azure region. The DDoS Protection service helps protect your Azure applications by analyzing and discarding DDoS traffic at the Azure network edge, before it can affect your service's availability.

   DDoS Protection identifies the attacker's attempt to overwhelm the network and blocks further traffic from them, ensuring that traffic never reaches Azure resources. Legitimate traffic from customers still flows into Azure without any interruption of service.

   DDoS Protection can also help you manage your cloud consumption. When you run on-premises, you have a fixed number of compute resources. But in the cloud, elastic computing means that you can automatically scale out your deployment to meet demand. A cleverly designed DDoS attack can cause you to increase your resource allocation, which incurs unneeded expense. DDoS Protection Standard helps ensure that the network load you process reflects customer usage. You can also receive credit for any costs accrued for scaled-out resources during a DDoS attack.

   **What service tiers are available to DDoS Protection?**

   DDoS Protection provides these service tiers:

   *Basic*

   The Basic service tier is automatically enabled for free as part of your Azure subscription.

   Always-on traffic monitoring and real-time mitigation of common network-level attacks provide the same defenses that Microsoft's online services use. The Basic service tier ensures that Azure infrastructure itself is not affected during a large-scale DDoS attack.

   The Azure global network is used to distribute and mitigate attack traffic across Azure regions.

   *Standard*

   The Standard service tier provides additional mitigation capabilities that are tuned specifically to Azure Virtual Network resources. DDoS Protection Standard is relatively easy to enable and requires no changes to your applications.

   The Standard tier provides always-on traffic monitoring and real-time mitigation of common network-level attacks. It provides the same defenses that Microsoft's online services use.

   Protection policies are tuned through dedicated traffic monitoring and machine learning algorithms. Policies are applied to public IP addresses, which are associated with resources deployed in virtual networks such as Azure Load Balancer and Application Gateway.

   The Azure global network is used to distribute and mitigate attack traffic across Azure regions.

   **What kinds of attacks can DDoS Protection help prevent?**

   The Standard service tier can help prevent:

   *Volumetric attacks*

   The goal of this attack is to flood the network layer with a substantial amount of seemingly legitimate traffic.

   *Protocol attacks*

   These attacks render a target inaccessible by exploiting a weakness in the layer 3 and layer 4 protocol stack.

   *Resource-layer (application-layer) attacks (only with web application firewall)*

   These attacks target web application packets to disrupt the transmission of data between hosts. You need a web application firewall (WAF) to protect against L7 attacks. DDoS Protection Standard protects the WAF from volumetric and protocol attacks.

## Describe identity, governance, privacy, and compliance features (20-
25%)

### Describe core Azure identity services
1. explain the difference between authentication and authorization [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/secure-access-azure-identity-services/2-compare-authentication-authorization)

   **What is authentication?**

   Authentication is the process of establishing the identity of a person or service that wants to access a resource. It involves the act of challenging a party for legitimate credentials and provides the basis for creating a security principal for identity and access control. It establishes whether the user is who they say they are.

   **What is authorization?**

   Authentication establishes the user's identity, but authorization is the process of establishing what level of access an authenticated person or service has. It specifies what data they're allowed to access and what they can do with it.

   **How are authentication and authorization related?**

   Here's a diagram that shows the relationship between authentication and authorization:
   ![Authentication and Authorization](/assets/pages/2021-04-07-az-900-azure-fundamentals-preparation/2-id-card-access.png)

   The identification card represents credentials that the user has to prove their identity (you'll learn more about the types of credentials later in this module.) Once authenticated, authorization defines what kinds of applications, resources, and data that user can access.

2. define Azure Active Directory [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/secure-access-azure-identity-services/3-what-is-azure-active-directory)

   Azure Active Directory (Azure AD) provides identity services that enable your users to sign in and access both Microsoft cloud applications and cloud applications that you develop.

   **How does Azure AD compare to Active Directory?**
   Active Directory is related to Azure AD, but they have some key differences.

   Microsoft introduced Active Directory in Windows 2000 to give organizations the ability to manage multiple on-premises infrastructure components and systems by using a single identity per user.

   For on-premises environments, Active Directory running on Windows Server provides an identity and access management service that's managed by your own organization. Azure AD is Microsoft's cloud-based identity and access management service. With Azure AD, you control the identity accounts, but Microsoft ensures that the service is available globally. If you've worked with Active Directory, Azure AD will be familiar to you.

   When you secure identities on-premises with Active Directory, Microsoft doesn't monitor sign-in attempts. When you connect Active Directory with Azure AD, Microsoft can help protect you by detecting suspicious sign-in attempts at no extra cost. For example, Azure AD can detect sign-in attempts from unexpected locations or unknown devices.

   **Who uses Azure AD?**

   Azure AD is for:

   *IT administrators*

   Administrators can use Azure AD to control access to applications and resources based on their business requirements.

   *App developers*

   Developers can use Azure AD to provide a standards-based approach for adding functionality to applications that they build, such as adding SSO functionality to an app or enabling an app to work with a user's existing credentials.

   *Users*

   Users can manage their identities. For example, self-service password reset enables users to change or reset their password with no involvement from an IT administrator or help desk.

   *Online service subscribers*

   Microsoft 365, Microsoft Office 365, Azure, and Microsoft Dynamics CRM Online subscribers are already using Azure AD.

   A tenant is a representation of an organization. A tenant is typically separated from other tenants and has its own identity.

   Each Microsoft 365, Office 365, Azure, and Dynamics CRM Online tenant is automatically an Azure AD tenant.

3. describe the functionality and usage of Azure Active Directory [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/secure-access-azure-identity-services/3-what-is-azure-active-directory)

   Azure AD provides services such as:

   *Authentication*

   This includes verifying identity to access applications and resources. It also includes providing functionality such as self-service password reset, multifactor authentication, a custom list of banned passwords, and smart lockout services.

   *Single sign-on*

   SSO enables you to remember only one username and one password to access multiple applications. A single identity is tied to a user, which simplifies the security model. As users change roles or leave an organization, access modifications are tied to that identity, which greatly reduces the effort needed to change or disable accounts.

   *Application management*

   You can manage your cloud and on-premises apps by using Azure AD. Features like Application Proxy, SaaS apps, the My Apps portal (also called the access panel), and single-sign on provide a better user experience.

   *Device management*

   Along with accounts for individual people, Azure AD supports the registration of devices. Registration enables devices to be managed through tools like Microsoft Intune. It also allows for device-based conditional access policies to restrict access attempts to only those coming from known devices, regardless of the requesting user account.

   **What kinds of resources can Azure AD help secure?**

   Azure AD helps users access both external and internal resources.

   External resources might include Microsoft Office 365, the Azure portal, and thousands of other software as a service (SaaS) applications.

   Internal resources might include apps on your corporate network and intranet, along with any cloud applications developed within your organization.

   **What's single sign-on?**

   Single sign-on enables a user to sign in one time and use that credential to access multiple resources and applications from different providers.

   More identities mean more passwords to remember and change. Password policies can vary among applications. As complexity requirements increase, it becomes increasingly difficult for users to remember them. The more passwords a user has to manage, the greater the risk of a credential-related security incident.

   Consider the process of managing all those identities. Additional strain is placed on help desks as they deal with account lockouts and password reset requests. If a user leaves an organization, tracking down all those identities and ensuring they are disabled can be challenging. If an identity is overlooked, this might allow access when it should have been eliminated.

   With SSO, you need to remember only one ID and one password. Access across applications is granted to a single identity that's tied to the user, which simplifies the security model. As users change roles or leave an organization, access is tied to a single identity. This change greatly reduces the effort needed to change or disable accounts. Using SSO for accounts makes it easier for users to manage their identities and increases your security capabilities.

   You'll find resources at the end of this module about how to enable SSO through Azure AD.

   **How can I connect Active Directory with Azure AD?**

   Connecting Active Directory with Azure AD enables you to provide a consistent identity experience to your users.

   There are a few ways to connect your existing Active Directory installation with Azure AD. Perhaps the most popular method is to use Azure AD Connect.

   Azure AD Connect synchronizes user identities between on-premises Active Directory and Azure AD. Azure AD Connect synchronizes changes between both identity systems, so you can use features like SSO, multifactor authentication, and self-service password reset under both systems. Self-service password reset prevents users from using known compromised passwords.

   Here's a diagram that shows how Azure AD Connect fits between on-premises Active Directory and Azure AD:
   ![Azure AD Connect](/assets/pages/2021-04-07-az-900-azure-fundamentals-preparation/3-azure-ad-connect.png)

4. describe the functionality and usage of Conditional Access, Multi-Factor Authentication (MFA), and Single Sign-On (SSO) [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/secure-access-azure-identity-services/4-what-are-mfa-conditional-access)

   Azure provides two processes that enable secure authentication: Azure AD Multi-Factor Authentication and Conditional Access.

   **What's multifactor authentication?**

   Multifactor authentication is a process where a user is prompted during the sign-in process for an additional form of identification. Examples include a code on their mobile phone or a fingerprint scan.

   Think about how you sign in to websites, email, or online gaming services. In addition to your username and password, have you ever needed to enter a code that was sent to your phone? If so, you've used multifactor authentication to sign in.

   Multifactor authentication provides additional security for your identities by requiring two or more elements to fully authenticate.

   These elements fall into three categories:
   * Something the user knows: This might be an email address and password.
   * Something the user has: This might be a code that's sent to the user's mobile phone.
   * Something the user is: This is typically some sort of biometric property, such as a fingerprint or face scan that's used on many mobile devices.
  
   Multifactor authentication increases identity security by limiting the impact of credential exposure (for example, stolen usernames and passwords). With multifactor authentication enabled, an attacker who has a user's password would also need to have possession of their phone or their fingerprint to fully authenticate.

   Compare multifactor authentication with single-factor authentication. Under single-factor authentication, an attacker would need only a username and password to authenticate. Multifactor authentication should be enabled wherever possible because it adds enormous benefits to security.

   **What's Azure AD Multi-Factor Authentication?**

   Azure AD Multi-Factor Authentication is a Microsoft service that provides multifactor authentication capabilities. Azure AD Multi-Factor Authentication enables users to choose an additional form of authentication during sign-in, such as a phone call or mobile app notification.

   These services provide Azure AD Multi-Factor Authentication capabilities:

   *Azure Active Directory*

   The Azure Active Directory free edition enables Azure AD Multi-Factor Authentication for administrators with the global admin level of access, via the Microsoft Authenticator app, phone call, or SMS code. You can also enforce Azure AD Multi-Factor Authentication for all users via the Microsoft Authenticator app only, by enabling security defaults in your Azure AD tenant.

   Azure Active Directory Premium (P1 or P2 licenses) allows for comprehensive and granular configuration of Azure AD Multi-Factor Authentication through Conditional Access policies (explained shortly).

   *Multifactor authentication for Office 365*

   A subset of Azure AD Multi-Factor Authentication capabilities is part of your Office 365 subscription.

   For more information on licenses and Azure AD Multi-Factor Authentication capabilities, see Available versions of Azure AD Multi-Factor Authentication.

   **What's Conditional Access?**

   Conditional Access is a tool that Azure Active Directory uses to allow (or deny) access to resources based on identity signals. These signals include who the user is, where the user is, and what device the user is requesting access from.

   Conditional Access helps IT administrators:

   * Empower users to be productive wherever and whenever.
   * Protect the organization's assets.

   Conditional Access also provides a more granular multifactor authentication experience for users. For example, a user might not be challenged for second authentication factor if they're at a known location. However, they might be challenged for a second authentication factor if their sign-in signals are unusual or they're at an unexpected location.

   During sign-in, Conditional Access collects signals from the user, makes decisions based on those signals, and then enforces that decision by allowing or denying the access request or challenging for a multifactor authentication response.

   Here's a diagram that illustrates this flow:
   ![Conditional Access Flow](/assets/pages/2021-04-07-az-900-azure-fundamentals-preparation/4-conditional-access-signal-decision-enforcement.png)

   Here, the signal might be the user's location, the user's device, or the application that the user is trying to access.

   Based on these signals, the decision might be to allow full access if the user is signing in from their usual location. If the user is signing in from an unusual location or a location that's marked as high risk, then access might be blocked entirely or possibly granted after the user provides a second form of authentication.

   Enforcement is the action that carries out the decision. For example, the action is to allow access or require the user to provide a second form of authentication.

   **When can I use Conditional Access?**

   Conditional Access is useful when you need to:

   *Require multifactor authentication to access an application.*

   You can configure whether all users require multifactor authentication or only certain users, such as administrators.

   You can also configure whether multifactor authentication applies to access from all networks or only untrusted networks.

   *Require access to services only through approved client applications.*

   For example, you might want to allow users to access Office 365 services from a mobile device as long as they use approved client apps, like the Outlook mobile app.

   *Require users to access your application only from managed devices.*

   A managed device is a device that meets your standards for security and compliance.

   *Block access from untrusted sources, such as access from unknown or unexpected locations.*

   Conditional Access comes with a What If tool, which helps you plan and troubleshoot your Conditional Access policies. You can use this tool to model your proposed Conditional Access policies across recent sign-in attempts from your users to see what the impact would have been if those policies had been enabled. The What If tool enables you to test your proposed Conditional Access policies before you implement them.

   **Where is Conditional Access available?**

   To use Conditional Access, you need an Azure AD Premium P1 or P2 license. If you have a Microsoft 365 Business Premium license, you also have access to Conditional Access features.

### Describe Azure governance features

1. describe the functionality and usage of Role-Based Access Control (RBAC) [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/build-cloud-governance-strategy-azure/4-control-access-azure-rbac)

   When you have multiple IT and engineering teams, how can you control what access they have to the resources in your cloud environment? It's a good security practice to grant users only the rights they need to perform their job, and only to the relevant resources.

   Instead of defining the detailed access requirements for each individual, and then updating access requirements when new resources are created, Azure enables you to control access through Azure role-based access control (Azure RBAC).

   Azure provides built-in roles that describe common access rules for cloud resources. You can also define your own roles. Each role has an associated set of access permissions that relate to that role. When you assign individuals or groups to one or more roles, they receive all of the associated access permissions.

   **How is role-based access control applied to resources?**

   Role-based access control is applied to a scope, which is a resource or set of resources that this access applies to.

   Here's a diagram that shows the relationship between roles and scopes.
   ![Role Scope](/assets/pages/2021-04-07-az-900-azure-fundamentals-preparation/4-role-scope.png)

   Scopes include:

   * A management group (a collection of multiple subscriptions).
   * A single subscription.
   * A resource group.
   * A single resource.
  
   Observers, Users managing resources, Admins, and Automated processes illustrate the kinds of users or accounts that would typically be assigned each of the various roles.

   When you grant access at a parent scope, those permissions are inherited by all child scopes. For example:

   * When you assign the Owner role to a user at the management group scope, that user can manage everything in all subscriptions within the management group.
   * When you assign the Reader role to a group at the subscription scope, the members of that group can view every resource group and resource within the subscription.
   * When you assign the Contributor role to an application at the resource group scope, the application can manage resources of all types within that resource group, but not other resource groups within the subscription.

   **When should I use Azure RBAC?**

   Use Azure RBAC when you need to:

   * Allow one user to manage VMs in a subscription and another user to manage virtual networks.
   * Allow a database administrator group to manage SQL databases in a subscription.
   * Allow a user to manage all resources in a resource group, such as virtual machines, websites, and subnets.
   * Allow an application to access all resources in a resource group.

   These are just a few examples.

   **How is Azure RBAC enforced?**

   Azure RBAC is enforced on any action that's initiated against an Azure resource that passes through Azure Resource Manager. Resource Manager is a management service that provides a way to organize and secure your cloud resources.

   You typically access Resource Manager from the Azure portal, Azure Cloud Shell, Azure PowerShell, and the Azure CLI. Azure RBAC doesn't enforce access permissions at the application or data level. Application security must be handled by your application.

   RBAC uses an allow model. When you're assigned a role, RBAC allows you to perform certain actions, such as read, write, or delete. If one role assignment grants you read permissions to a resource group and a different role assignment grants you write permissions to the same resource group, you have both read and write permissions on that resource group.

   **Who does Azure RBAC apply to?**

   You can apply Azure RBAC to an individual person or to a group. You can also apply Azure RBAC to other special identity types, such as service principals and managed identities. These identity types are used by applications and services to automate access to Azure resources.

   **How do I manage Azure RBAC permissions?**

   You manage access permissions on the Access control (IAM) pane in the Azure portal. This pane shows who has access to what scope and what roles apply. You can also grant or remove access from this pane.

2. describe the functionality and usage of resource locks [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/build-cloud-governance-strategy-azure/5-prevent-changes-resource-locks)

   A resource lock prevents resources from being accidentally deleted or changed.

   Even with Azure role-based access control (Azure RBAC) policies in place, there's still a risk that people with the right level of access could delete critical cloud resources. Think of a resource lock as a warning system that reminds you that a resource should not be deleted or changed.

   **How do I manage resource locks?**

   You can manage resource locks from the Azure portal, PowerShell, the Azure CLI, or from an Azure Resource Manager template.

   To view, add, or delete locks in the Azure portal, go to the Settings section of any resource's Settings pane in the Azure portal.

   **What levels of locking are available?**

   You can apply locks to a subscription, a resource group, or an individual resource. You can set the lock level to CanNotDelete or ReadOnly.

   * CanNotDelete means authorized people can still read and modify a resource, but they can't delete the resource without first removing the lock.
   * ReadOnly means authorized people can read a resource, but they can't delete or change the resource. Applying this lock is like restricting all authorized users to the permissions granted by the Reader role in Azure RBAC.

   **How do I delete or change a locked resource?**

   Although locking helps prevent accidental changes, you can still make changes by following a two-step process.

   To modify a locked resource, you must first remove the lock. After you remove the lock, you can apply any action you have permissions to perform. This additional step allows the action to be taken, but it helps protect your administrators from doing something they might not have intended to do.

   Resource locks apply regardless of RBAC permissions. Even if you're an owner of the resource, you must still remove the lock before you can perform the blocked activity.

   **Combine resource locks with Azure Blueprints**

   What if a cloud administrator accidentally deletes a resource lock? If the resource lock is removed, its associated resources can be changed or deleted.

   To make the protection process more robust, you can combine resource locks with Azure Blueprints. Azure Blueprints enables you to define the set of standard Azure resources that your organization requires. For example, you can define a blueprint that specifies that a certain resource lock must exist. Azure Blueprints can automatically replace the resource lock if that lock is removed.

3. describe the functionality and usage of tags [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/build-cloud-governance-strategy-azure/7-organize-resource-tags)

   As your cloud usage grows, it's increasingly important to stay organized. A good organization strategy helps you understand your cloud usage and can help you manage costs.

   One way to organize related resources is to place them in their own subscriptions. You can also use resource groups to manage related resources. Resource tags are another way to organize resources. Tags provide extra information, or metadata, about your resources. This metadata is useful for:

   *Resource management*

   Tags enable you to locate and act on resources that are associated with specific workloads, environments, business units, and owners

   *Cost management and optimization*

   Tags enable you to group resources so that you can report on costs, allocate internal cost centers, track budgets, and forecast estimated cost.

   *Operations management*

   Tags enable you to group resources according to how critical their availability is to your business. This grouping helps you formulate service-level agreements (SLAs). An SLA is an uptime or performance guarantee between you and your users.

   *Security*

   Tags enable you to classify data by its security level, such as public or confidential.

   *Governance and regulatory compliance*

   Tags enable you to identify resources that align with governance or regulatory compliance requirements, such as ISO 27001.

   Tags can also be part of your standards enforcement efforts. For example, you might require that all resources be tagged with an owner or department name.

   *Workload optimization and automation*

   Tags can help you visualize all of the resources that participate in complex deployments. For example, you might tag a resource with its associated workload or application name and use software such as Azure DevOps to perform automated tasks on those resources.

   **How do I manage resource tags?**

   You can add, modify, or delete resource tags through PowerShell, the Azure CLI, Azure Resource Manager templates, the REST API, or the Azure portal.

   You can also manage tags by using Azure Policy. For example, you can apply tags to a resource group, but those tags aren't automatically applied to the resources within that resource group. You can use Azure Policy to ensure that a resource inherits the same tags as its parent resource group. You'll learn more about Azure Policy later in this module.

   You can also use Azure Policy to enforce tagging rules and conventions. For example, you can require that certain tags be added to new resources as they're provisioned. You can also define rules that reapply tags that have been removed.

4. describe the functionality and usage of Azure Policy [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/build-cloud-governance-strategy-azure/8-control-audit-resources-azure-policy)

   Now that you've identified your governance and business requirements, how do you ensure that your resources stay compliant? How can you be alerted if a resource's configuration has changed?

   Azure Policy is a service in Azure that enables you to create, assign, and manage policies that control or audit your resources. These policies enforce different rules and effects over your resource configurations so that those configurations stay compliant with corporate standards.

   **How does Azure Policy define policies?**

   Azure Policy enables you to define both individual policies and groups of related policies, known as initiatives. Azure Policy evaluates your resources and highlights resources that aren't compliant with the policies you've created. Azure Policy can also prevent noncompliant resources from being created.

   Azure Policy comes with a number of built-in policy and initiative definitions that you can use, under categories such as Storage, Networking, Compute, Security Center, and Monitoring.

   For example, say you define a policy that allows only a certain stock-keeping unit (SKU) size of virtual machines (VMs) to be used in your environment. After you enable this policy, that policy is applied when you create new VMs or resize existing VMs. Azure Policy also evaluates any current VMs in your environment.

   In some cases, Azure Policy can automatically remediate noncompliant resources and configurations to ensure the integrity of the state of the resources. For example, if all resources in a certain resource group should be tagged with the AppName tag and a value of "SpecialOrders," Azure Policy can automatically reapply that tag if it has been removed.

   Azure Policy also integrates with Azure DevOps by applying any continuous integration and delivery pipeline policies that apply to the pre-deployment and post-deployment phases of your applications.

   **Azure Policy in action**

   Implementing a policy in Azure Policy involves these three steps:

   *Create a policy definition.*

   A policy definition expresses what to evaluate and what action to take. For example, you could prevent VMs from being deployed in certain Azure regions. You also could audit your storage accounts to verify that they only accept connections from allowed networks.

   Every policy definition has conditions under which it's enforced. A policy definition also has an accompanying effect that takes place when the conditions are met. Here are some example policy definitions:

   * Allowed virtual machine SKUs: This policy enables you to specify a set of VM SKUs that your organization can deploy.
   * Allowed locations: This policy enables you to restrict the locations that your organization can specify when it deploys resources. Its effect is used to enforce your geographic compliance requirements.
   * MFA should be enabled on accounts with write permissions on your subscription: This policy requires that multifactor authentication (MFA) be enabled for all subscription accounts with write privileges to prevent a breach of accounts or resources.
   * CORS should not allow every resource to access your web applications: Cross-origin resource sharing (CORS) is an HTTP feature that enables a web application running under one domain to access resources in another domain. For security reasons, modern web browsers restrict cross-site scripting by default. This policy allows only required domains to interact with your web app.
   * System updates should be installed on your machines: This policy enables Azure Security Center to recommend missing security system updates on your servers.

   *Assign the definition to resources.*

   To implement your policy definitions, you assign definitions to resources. A policy assignment is a policy definition that takes place within a specific scope. This scope could be a management group (a collection of multiple subscriptions), a single subscription, or a resource group.

   Policy assignments are inherited by all child resources within that scope. If a policy is applied to a resource group, that policy is applied to all resources within that resource group. You can exclude a subscope from the policy assignment if there are specific child resources you need to be exempt from the policy assignment.

   *Review the evaluation results.*

   When a condition is evaluated against your existing resources, each resource is marked as compliant or noncompliant. You can review the noncompliant policy results and take any action that's needed.

   Policy evaluation happens about once per hour. If you make changes to your policy definition and create a policy assignment, that policy is evaluated over your resources within the hour.

   **What are Azure Policy initiatives?**

   An Azure Policy initiative is a way of grouping related policies into one set. The initiative definition contains all of the policy definitions to help track your compliance state for a larger goal.

   For example, Azure Policy includes an initiative named Enable Monitoring in Azure Security Center. Its goal is to monitor all of the available security recommendations for all Azure resource types in Azure Security Center.

   Under this initiative, the following policy definitions are included:

   * Monitor unencrypted SQL Database in Security Center: This policy monitors for unencrypted SQL databases and servers.
   * Monitor OS vulnerabilities in Security Center: This policy monitors servers that don't satisfy the configured OS vulnerability baseline.
   * Monitor missing Endpoint Protection in Security Center: This policy monitors for servers that don't have an installed endpoint protection agent.

   In fact, the Enable Monitoring in Azure Security Center initiative contains over 100 separate policy definitions.

   Azure Policy also includes initiatives that support regulatory compliance standards such as HIPAA and ISO 27001.

   **How do I define an initiative?**

   You define initiatives by using the Azure portal or by using command-line tools. From the Azure portal, you can search the list of built-in initiatives that are already provided by Azure. You also can create your own custom policy definition

   **How do I assign an initiative?**

   Like a policy assignment, an initiative assignment is an initiative definition that's assigned to a specific scope of a management group, a subscription, or a resource group.

   Even if you have only a single policy, an initiative enables you to increase the number of policies over time. Because the associated initiative remains assigned, it's easier to add and remove policies without the need to change the policy assignment for your resources.

5. describe the functionality and usage of Azure Blueprints [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/build-cloud-governance-strategy-azure/10-govern-subscriptions-azure-blueprints)

   So far, you've explored a number of Azure features that can help you implement your governance decisions, monitor the compliance of your cloud resources, and control access and protect critical resources from accidental deletion.

   What happens when your cloud environment starts to grow beyond just one subscription? How can you scale the configuration of these features, knowing they need to be enforced for resources in new subscriptions?

   Instead of having to configure features like Azure Policy for each new subscription, with Azure Blueprints you can define a repeatable set of governance tools and standard Azure resources that your organization requires. In this way, development teams can rapidly build and deploy new environments with the knowledge that they're building within organizational compliance with a set of built-in components that speed the development and deployment phases.

   Azure Blueprints orchestrates the deployment of various resource templates and other artifacts, such as:

   * Role assignments
   * Policy assignments
   * Azure Resource Manager templates
   * Resource groups

   **Azure Blueprints in action** 

   When you form a cloud center of excellence team or a cloud custodian team, that team can use Azure Blueprints to scale their governance practices throughout the organization.

   Implementing a blueprint in Azure Blueprints involves these three steps:

   * Create an Azure blueprint.
   * Assign the blueprint.
   * Track the blueprint assignments.

   With Azure Blueprints, the relationship between the blueprint definition (what should be deployed) and the blueprint assignment (what was deployed) is preserved. In other words, Azure creates a record that associates a resource with the blueprint that defines it. This connection helps you track and audit your deployments.

   Blueprints are also versioned. Versioning enables you to track and comment on changes to your blueprint.

   **What are blueprint artifacts?**

   Each component in the blueprint definition is known as an artifact.

   It is possible for artifacts to have no additional parameters (configurations). An example is the Deploy threat detection on SQL servers policy, which requires no additional configuration.

   Artifacts can also contain one or more parameters that you can configure.

   You can specify a parameter's value when you create the blueprint definition or when you assign the blueprint definition to a scope. In this way, you can maintain one standard blueprint but have the flexibility to specify the relevant configuration parameters at each scope where the definition is assigned.


6. describe the Cloud Adoption Framework for Azure [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/build-cloud-governance-strategy-azure/2-accelerate-cloud-adoption-framework)

   The Cloud Adoption Framework for Azure provides you with proven guidance to help with your cloud adoption journey. The Cloud Adoption Framework helps you create and implement the business and technology strategies needed to succeed in the cloud.

   It consists of tools, documentation, and proven practices. The Cloud Adoption Framework includes these stages:

   * Define your strategy.
   * Make a plan.
   * Ready your organization.
   * Adopt the cloud.
   * Govern and manage your cloud environments.

   ![Framework stages](/assets/pages/2021-04-07-az-900-azure-fundamentals-preparation/2-framework-stages.png)

   The govern stage focuses on cloud governance. You can refer back to the Cloud Adoption Framework for recommended guidance as you build your cloud governance strategy.

   To help build your adoption strategy, the Cloud Adoption Framework breaks out each stage into further exercises and steps. Let's take a brief look at each stage.

   **Define your strategy**

   Here, you answer why you're moving to the cloud and what you want to get out of cloud migration. Do you need to scale to meet demand or reach new markets? Will it reduce costs or increase business agility?
   * Define and document your motivations: Meeting with stakeholders and leadership can help you answer why you're moving to the cloud.
   * Document business outcomes: Meet with leadership from your finance, marketing, sales, and human resource groups to help you document your goals.
   * Develop a business case: Validate that moving to the cloud gives you the right return on investment (ROI) for your efforts.
   * Choose the right first project: Choose a project that's achievable but also shows progress toward your cloud migration goals.

   **Make a plan**

   Here, you build a plan that maps your aspirational goals to specific actions. A good plan helps ensure that your efforts map to the desired business outcomes.

   Here are the steps in this stage.

   * Digital estate: Create an inventory of the existing digital assets and workloads that you plan to migrate to the cloud.
   * Initial organizational alignment: Ensure that the right people are involved in your migration efforts, both from a technical standpoint as well as from a cloud governance standpoint.
   * Skills readiness plan: Build a plan that helps individuals build the skills they need to operate in the cloud.
   * Cloud adoption plan: Build a comprehensive plan that brings together the development, operations, and business teams toward a shared cloud adoption goal.

   **Ready your organization**

   Here, you create a landing zone, or an environment in the cloud to begin hosting your workloads.

   Here are the steps in this stage.

   * Azure setup guide: Review the Azure setup guide to become familiar with the tools and approaches you need to use to create a landing zone.
   * Azure landing zone: Begin to build out the Azure subscriptions that support each of the major areas of your business. A landing zone includes cloud infrastructure as well as governance, accounting, and security capabilities.
   * Expand the landing zone: Refine your landing zone to ensure that it meets your operations, governance, and security needs.
   * Best practices: Start with recommended and proven practices to help ensure that your cloud migration efforts are scalable and maintainable.

   **Adopt the cloud**

   Here, you begin to migrate your applications to the cloud. Along the way, you might find ways to modernize your applications and build innovative solutions that use cloud services.

   The Cloud Adoption Framework breaks this stage into two parts: migrate and innovate.

   Migrate: Here are the steps in the migrate part of this stage.

   * Migrate your first workload: Use the Azure migration guide to deploy your first project to the cloud.
   * Migration scenarios: Use additional in-depth guides to explore more complex migration scenarios.
   * Best practices: Check in with the Azure cloud migration best practices checklist to verify that you're following recommended practices.
   * Process improvements: Identify ways to make the migration process scale while requiring less effort.

   **Innovate: Here are the steps in the innovate part of this stage.**

   * Business value consensus: Verify that investments in new innovations add value to the business and meet customer needs.
   * Azure innovation guide: Use this guide to accelerate development and build a minimum viable product (MVP) for your idea.
   * Best practices: Verify that your progress maps to recommended practices before you move forward.
   * Feedback loops: Check in frequently with your customers to verify that you're building what they need.

   **Govern and manage your cloud environments**

   Here, you begin to form your cloud governance and cloud management strategies. As the cloud estate changes over time, so do cloud governance processes and policies. You need to create resilient solutions that are constantly optimized.

   Govern: Here are the steps in the govern part of this stage.

   * Methodology: Consider your end state solution. Then define a methodology that incrementally takes you from your first steps all the way to full cloud governance.
   * Benchmark: Use the governance benchmark tool to assess your current state and future state to establish a vision for applying the framework.
   * Initial governance foundation: Create an MVP that captures the first steps of your governance plan.
   * Improve the initial governance foundation: Iteratively add governance controls that address tangible risks as you progress toward your end state solution.

   **Manage: Here are the steps in the manage part of this stage.**

   * Establish a management baseline: Define your minimum commitment to operations management. A management baseline is the minimum set of tools and processes that should be applied to every asset in an environment.
   * Define business commitments: Document supported workloads to establish operational commitments with the business and agree on cloud management investments for each workload.
   * Expand the management baseline: Apply recommended best practices to iterate on your initial management baseline.
   * Advanced operations and design principles: For workloads that require a higher level of business commitment, perform a deeper architecture review to deliver on your resiliency and reliability commitments.

### Describe privacy and compliance resources

1. describe the Microsoft core tenets of Security, Privacy, and Compliance [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/examine-privacy-compliance-data-protection-standards/2-explore-compliance-terms-requirements)

   Microsoft's online services build upon a common set of regulatory and compliance controls. Think of a control as a known good standard that you can compare your solution against to ensure security. These controls address today's regulations and adapt as regulations evolve.

   **Which compliance categories are available on Azure?**

   Although there are many more, the following image shows some of the more popular compliance offerings that are available on Azure. These offerings are grouped under four categories: Global, US Government, Industry, and Regional.
   ![Compliance Categories](/assets/pages/2021-04-07-az-900-azure-fundamentals-preparation/2-compliance-matrix.png)

2. describe the purpose of the Microsoft Privacy Statement, Product Terms site, and Data Protection Addendum (DPA) [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/examine-privacy-compliance-data-protection-standards/3-access-microsoft-privacy-statement)

   **What's in the Microsoft Privacy Statement?**

   The Microsoft Privacy Statement explains what personal data Microsoft collects, how Microsoft uses it, and for what purposes.

   The privacy statement covers all of Microsoft's services, websites, apps, software, servers, and devices. This list ranges from enterprise and server products to devices that you use in your home to software that students use at school.

   Microsoft's privacy statement also provides information that's relevant to specific products such as Windows and Xbox.

   **What's in the Online Services Terms?**

   The Online Services Terms (OST) is a legal agreement between Microsoft and the customer. The OST details the obligations by both parties with respect to the processing and security of customer data and personal data. The OST applies specifically to Microsoft's online services that you license through a subscription, including Azure, Dynamics 365, Office 365, and Bing Maps.

   **What is the Data Protection Addendum?**

   The Data Protection Addendum (DPA) further defines the data processing and security terms for online services. These terms include:

   * Compliance with laws.
   * Disclosure of processed data.
   * Data Security, which includes security practices and policies, data encryption, data access, customer responsibilities, and compliance with auditing.
   * Data transfer, retention, and deletion.

   To access the DPA:
   * Go to the Licensing Terms and Documentation.
   * In the search bar, enter DPA.
   * From the search results, locate the link to the DPA in your preferred language.

   Alternatively, in the search bar that appears, enter your preferred language to filter the results. Here's an example that retrieves the English version of the DPA.

   Transparency is important when it comes to how a cloud provider communicates its privacy policies and how it treats your data. The Microsoft Privacy Statement, the OST, and the DPA detail Microsoft's commitment to protecting data and privacy in the cloud

   The Microsoft Privacy Statement, the OST, and the DPA detail Microsoft's commitment to protecting data and privacy in the cloud.

3. describe the purpose of the Trust Center [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/examine-privacy-compliance-data-protection-standards/4-explore-trust-center)

   The Trust Center showcases Microsoft's principles for maintaining data integrity in the cloud and how Microsoft implements and supports security, privacy, compliance, and transparency in all Microsoft cloud products and services. The Trust Center is an important part of the Microsoft Trusted Cloud Initiative and provides support and resources for the legal and compliance community.

   The Trust Center provides:

   * In-depth information about security, privacy, compliance offerings, policies, features, and practices across Microsoft cloud products.
   * Additional resources for each topic.
   * Links to the security, privacy, and compliance blogs and upcoming events.

   The Trust Center is a great resource for other people in your organization who might play a role in security, privacy, and compliance. These people include business managers, risk assessment and privacy officers, and legal compliance teams.

4. describe the purpose of the Azure compliance documentation [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/examine-privacy-compliance-data-protection-standards/5-access-azure-compliance-documentation)

   The Azure compliance documentation provides you with detailed documentation about legal and regulatory standards and compliance on Azure.

   Here you find compliance offerings across these categories:

   * Global
   * US government
   * Financial services
   * Health
   * Media and manufacturing
   * Regional

   There are also additional compliance resources, such as audit reports, privacy information, compliance implementations and mappings, and white papers and analyst reports. Country and region privacy and compliance guidelines are also included. Some resources might require you to be signed in to your cloud service to access them.

5. describe the purpose of Azure Sovereign Regions (Azure Government cloud services and Azure China cloud services) [Microsoft Learn Azure Government Reference](https://docs.microsoft.com/en-us/learn/modules/examine-privacy-compliance-data-protection-standards/6-what-is-azure-government) [Microsoft Learn Azure China Reference](https://docs.microsoft.com/en-us/learn/modules/examine-privacy-compliance-data-protection-standards/7-what-is-azure-china-21vianet)

   **What is Azure Government?**

   Azure Government is a separate instance of the Microsoft Azure service. It addresses the security and compliance needs of US federal agencies, state and local governments, and their solution providers. Azure Government offers physical isolation from non-US government deployments and provides screened US personnel.

   Azure Government services handle data that is subject to certain government regulations and requirements:

   * Federal Risk and Authorization Management Program (FedRAMP)
   * National Institute of Standards and Technology (NIST) 800.171 Defense Industrial Base (DIB)
   * International Traffic in Arms Regulations (ITAR)
   * Internal Revenue Service (IRS) 1075
   * Department of Defense (DoD) L4
   * Criminal Justice Information Service (CJIS)

   To provide the highest level of security and compliance, Azure Government uses physically isolated datacenters and networks located only in the US. Azure Government customers, such as the US federal, state, and local government or their partners, are subject to validation of eligibility.

   Azure Government provides the broadest compliance and Level 5 DoD approval. Azure Government is available in eight geographies and offers the most compliance certifications of any cloud provider.

   **What is Azure China 21Vianet?**

   Azure China 21Vianet is operated by 21Vianet. It's a physically separated instance of cloud services located in China. Azure China 21Vianet is independently operated and transacted by Shanghai Blue Cloud Technology Co., Ltd. ("21Vianet"), a wholly owned subsidiary of Beijing 21Vianet Broadband Data Center Co., Ltd.

   According to the China Telecommunication Regulation, providers of cloud services, infrastructure as a service (IaaS) and platform as a service (PaaS), must have value-added telecom permits. Only locally registered companies with less than 50 percent foreign investment qualify for these permits. To comply with this regulation, the Azure service in China is operated by 21Vianet, based on the technologies licensed from Microsoft.

   As the first foreign public cloud service provider offered in China in compliance with government regulations, Azure China 21Vianet provides world-class security as discussed on the Trust Center, as required by Chinese regulations for all systems and applications built on its architecture.

   *Azure products and services available in China*

   The Azure services are based on the same Azure, Office 365, and Power BI technologies that make up the Microsoft global cloud service, with comparable service levels. Azure agreements and contracts in China, where applicable, are signed between customers and 21Vianet.

   Azure includes the core components of IaaS, PaaS, and software as a service (SaaS). These components include network, storage, data management, identity management, and many other services.

   Azure China 21Vianet supports most of the same services that global Azure has, such as geosynchronous data replication and autoscaling. Even if you already use global Azure services, to operate in China you might need to rehost or refactor some or all your applications or services.

## Describe Azure cost management and Service Level Agreements (10-
15%)

### Describe methods for planning and managing costs

1. identify factors that can affect costs (resource types, services, locations, ingress and egress traffic) [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/plan-manage-azure-costs/4-purchase-azure-services)

   The way you use resources, your subscription type, and pricing from third-party vendors are common factors that influence the cost. Let's take a quick look at each.

   *Resource type*

   A number of factors influence the cost of Azure resources. They depend on the type of resource or how you customize it.

   For example, with a storage account you specify a type (such as block blob storage or table storage), a performance tier (standard or premium), and an access tier (hot, cool, or archive). These selections present different costs.

   *Usage meters*

   When you provision a resource, Azure creates meters to track usage of that resource. Azure uses these meters to generate a usage record that's later used to help calculate your bill.

   Think of usage meters similar to how you use electricity or water in your home. You might pay a base price each month for electricity or water service, but your final bill is based on the total amount that you consumed.

   Let's look at a single VM as an example. The following kinds of meters are relevant to tracking its usage:

   * Overall CPU time.
   * Time spent with a public IP address.
   * Incoming (ingress) and outgoing (egress) network traffic in and out of the VM.
   * Disk size and amount of disk read and disk write operations.

   Each meter tracks a specific type of usage. For example, a meter might track bandwidth usage (ingress or egress network traffic in bits per second), number of operations, or its size (storage capacity in bytes).

   The usage that a meter tracks correlates to a quantity of billable units. Those units are charged to your account for each billing period. The rate per billable unit depends on the resource type you're using.

   *Resource usage*

   In Azure, you're always charged based on what you use. As an example, let's look at how this billing applies to deallocating a VM.

   In Azure, you can delete or deallocate a VM. Deleting a VM means that you no longer need it. The VM is removed from your subscription, and then it's prepared for another customer.

   Deallocating a VM means that the VM is no longer running. But the associated hard disks and data are still kept in Azure. The VM isn't assigned to a CPU or network in Azure's datacenter, so it doesn't generate the costs associated with compute time or the VM's IP address. Because the disks and data are still stored, and the resource is present in your Azure subscription, you're still billed for disk storage.

   Deallocating a VM when you don't plan on using it for some time is just one way to minimize costs. For example, you might deallocate the VMs you use for testing purposes on weekends when your testing team isn't using them. You'll learn more about ways to minimize cost later in this module.

   *Azure subscription types*

   Some Azure subscription types also include usage allowances, which affect costs.

   For example, an Azure free trial subscription provides access to a number of Azure products that are free for 12 months. It also includes credit to spend within your first 30 days of sign-up. And you get access to more than 25 products that are always free (based on resource and region availability).

   *Azure Marketplace*

   You can also purchase Azure-based solutions and services from third-party vendors through Azure Marketplace. Examples include managed network firewall appliances or connectors to third-party backup services. Billing structures are set by the vendor.

   **Does location or network traffic affect cost?**

   When you provision a resource in Azure, you need to define the location (known as the Azure region) of where it will be deployed. Let's see why this decision can have cost consequences.

   *Location*

   Azure infrastructure is distributed globally, which enables you to deploy your services centrally or provision your services closest to where your customers use them.

   Different regions can have different associated prices. Because geographic regions can impact where your network traffic flows, network traffic is a cost influence to consider as well.

   For example, say if a tenant decides to provision its Azure resources in the Azure regions that offer the lowest prices. That decision would save the company some money. But, if they need to transfer data between those regions, or if their users are located in different parts of the world, any potential savings could be offset by the additional network usage costs of transferring data between those resources.

   *Zones for billing of network traffic*

   Billing zones are a factor in determining the cost of some Azure services.

   Bandwidth refers to data moving in and out of Azure datacenters. Some inbound data transfers (data going into Azure datacenters) are free. For outbound data transfers (data leaving Azure datacenters), data transfer pricing is based on zones.

   A zone is a geographical grouping of Azure regions for billing purposes. The following zones include some of the regions as shown here:

   * Zone 1: Australia Central, West US, East US, Canada West, West Europe, France Central, and others
   * Zone 2: Australia East, Japan West, Central India, Korea South, and others
   * Zone 3: Brazil South, South Africa North, South Africa West, UAE Central, UAE North
   * DE Zone 1: Germany Central, Germany Northeast

2. identify factors that can reduce costs (reserved instances, reserved capacity, hybrid use benefit, spot pricing) [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/plan-manage-azure-costs/6-manage-minimize-total-cost)

   **Use Azure Reservations to prepay**

   Azure Reservations offers discounted prices on certain Azure services. Azure Reservations can save you up to 72 percent as compared to pay-as-you-go prices. To receive a discount, you reserve services and resources by paying in advance.

   For example, you can prepay for one year or three years of use of VMs, database compute capacity, database throughput, and other Azure resources.

   Azure Reservations are available to customers with an Enterprise Agreement, Cloud Solution Providers, and pay-as-you-go subscriptions.

   **Choose low-cost locations and regions**

   The cost of Azure products, services, and resources can vary across locations and regions. If possible, you should use them in those locations and regions where they cost less.

   But remember, some resources are metered and billed according to how much outgoing (egress) network bandwidth they consume. You should provision connected resources that are metered by bandwidth in the same Azure region to reduce egress traffic between them.

   **Research available cost-saving offers**

   Keep up to date with the latest Azure customer and subscription offers, and switch to offers that provide the greatest cost-saving benefit.

3. describe the functionality and usage of the Pricing calculator and the Total Cost of Ownership (TCO) calculator [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/plan-manage-azure-costs/2-compare-costs-tco-calculator)

   **Pricing calculator**

   As you've learned, an accurate cost estimate takes all of the preceding factors into account. Fortunately, the Azure Pricing calculator helps you with that process.

   The Pricing calculator displays Azure products in categories. You add these categories to your estimate and configure according to your specific requirements. You then receive a consolidated estimated price, with a detailed breakdown of the costs associated with each resource you added to your solution. You can export or share that estimate or save it for later. You can load a saved estimate and modify it to match updated requirements.

   You also can access pricing details, product details, and documentation for each product from within the Pricing calculator.

   The options that you can configure in the Pricing calculator vary between products, but they can include:

   * Region: A region is the geographical location in which you can provision a service. Southeast Asia, Central Canada, Western United States, and Northern Europe are a few examples.
   * Tier: Tiers, such as the Free tier or Basic tier, have different levels of availability or performance and different associated costs.
   * Billing options: Billing options highlight the different ways you can pay for a service. Options can vary based on your customer type and subscription type and can include options to save costs.
   * Support options: These options enable you to select additional support pricing options for certain services.
   * Programs and offers: Your customer or subscription type might enable you to choose from specific licensing programs or other offers.
   * Azure Dev/Test pricing: This option lists the available prices for development and test workloads. Dev/Test pricing applies when you run resources within an Azure subscription that's based on a Dev/Test offer.

   Keep in mind that the Pricing calculator provides estimates and not actual price quotes. Actual prices can vary depending upon the date of purchase, the payment currency you're using, and the type of Azure customer you are.

  **TCO Calculator**

   The TCO Calculator helps you estimate the cost savings of operating your solution on Azure over time, instead of in your on-premises datacenter.

   The term total cost of ownership is commonly used in finance. It can be hard to see all the hidden costs related to operating a technology capability on-premises. Software licenses and hardware are additional costs.

   With the TCO Calculator, you enter the details of your on-premises workloads. Then you review the suggested industry average cost (which you can adjust) for related operational costs. These costs include electricity, network maintenance, and IT labor. You're then presented with a side-by-side report. Using the report, you can compare those costs with the same workloads running on Azure.

   **How does the TCO Calculator work?**

   Working with the TCO Calculator involves three steps:

   *Define your workloads.*

   First, you enter the specifications of your on-premises infrastructure into the TCO Calculator, based on these four categories:

    * Servers: This category includes operating systems, virtualization methods, CPU cores, and memory (RAM).
    * Databases: This category includes database types, server hardware, and the Azure service you want to use, which includes the expected maximum concurrent user sign-ins.
    * Storage: This category includes storage type and capacity, which includes any backup or archive storage.
    * Networking: This category includes the amount of network bandwidth you currently consume in your on-premises environment.

   *Adjust assumptions.*

   Next, you specify whether your current on-premises licenses are enrolled for Software Assurance, which can save you money by reusing those licenses on Azure. You also specify whether you need to replicate your storage to another Azure region for greater redundancy.

   Then, you can see the key operating cost assumptions across several different areas, which vary among teams and organizations. These costs have been certified by Nucleus Research, an independent research company. For example, these costs include:

    * Electricity price per kilowatt hour (KWh).
    * Hourly pay rate for IT administration.
    * Network maintenance cost as a percentage of network hardware and software costs.

   To improve the accuracy of the TCO Calculator results, you adjust the values so that they match the costs of your current on-premises infrastructure.

   *View the report.*

   Choose a time frame between one and five years. the TCO Calculator generates a report that's based on the information you've entered.

   For each category (compute, datacenter, networking, storage, and IT labor), you can also view a side-by-side comparison of the cost breakdown of operating those workloads on-premises versus operating them on Azure.

   You can download, share, or save this report to review later.

4. describe the functionality and usage of Azure Cost Management [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/plan-manage-azure-costs/6-manage-minimize-total-cost)

   Azure Cost Management + Billing is a free service that helps you understand your Azure bill, manage your account and subscriptions, monitor and control Azure spending, and optimize resource use.

   Azure Cost Management + Billing features include:

   * Reporting: Use historical data to generate reports and forecast future usage and expenditure.
   * Data enrichment: Improve accountability by categorizing resources with tags that correspond to real-world business and organizational units.
   * Budgets: Create and manage cost and usage budgets by monitoring resource demand trends, consumption rates, and cost patterns.
   * Alerting: Get alerts based on your cost and usage budgets.
   * Recommendations: Receive recommendations to eliminate idle resources and to optimize the Azure resources you provision.

   **Apply tags to identify cost owners**

   Tags help you manage costs associated with the different groups of Azure products and resources. You can apply tags to groups of Azure resources to organize billing data.

   For example, if you run several VMs for different teams, you can use tags to categorize costs by department, such as Human Resources, Marketing, or Finance, or by environment, such as Test or Production.

   Tags make it easier to identify groups that generate the biggest Azure costs, which can help you adjust your spending accordingly.

   **Resize underutilized virtual machines**

   A common recommendation that you'll find from Azure Cost Management + Billing and Azure Advisor is to resize or shut down VMs that are underutilized or idle.

   As an example, say you have a VM whose size is Standard_D4_v4, a general-purpose VM type with four vCPUs and 16 GB of memory. You might discover that this VM is idle 90 percent of the time.

   Virtual machine costs are linear and double for each size larger in the same series. So in this case, if you reduce the VM's size from Standard_D4_v4 to Standard_D2_v4, which is the next size lower, you reduce your compute cost by 50 percent.

   Keep in mind that resizing a VM requires it to be stopped, resized, and then restarted. This process might take a few minutes depending on how significant the size change is. Be sure to properly plan for an outage, or shift your traffic to another instance while you perform resize operations.

   **Deallocate virtual machines during off hours**

   Recall that to deallocate a VM means to no longer run the VM, but preserve the associated hard disks and data in Azure.

   If you have VM workloads that are only used during certain periods, but you're running them every hour of every day, you're wasting money. These VMs are great candidates to shut down when not in use and start back when you need them, saving you compute costs while the VM is deallocated.

   This approach is an excellent strategy for development and testing environments, where the VMs are needed only during business hours. Azure even provides a way to automatically start and stop your VMs on a schedule.

   **Delete unused resources**

   This recommendation might sound obvious, but if you aren't using a resource, you should shut it down. It's not uncommon to find nonproduction or proof-of-concept systems that are no longer needed following the completion of a project.

   Regularly review your environment, and work to identify these systems. Shutting down these systems can have a dual benefit by saving you on infrastructure costs and potential savings on licensing and operating cost

   **Migrate from IaaS to PaaS services**

   As you move your workloads to the cloud, a natural evolution is to start with infrastructure as a service (IaaS) services because they map more directly to concepts and operations you're already familiar with.

   Over time, one way to reduce costs is to gradually move IaaS workloads to run on platform as a service (PaaS) services. While you can think of IaaS as direct access to compute infrastructure, PaaS provides ready-made development and deployment environments that are managed for you.

   As an example, say you run SQL Server on a VM running on Azure. This configuration requires you to manage the underlying operating system, set up a SQL Server license, manage software and security updates, and so on. You also pay for the VM whether or not the database is processing queries. One way to potentially save costs is to move your database from SQL Server on a VM to Azure SQL Database. Azure SQL Database is based on SQL Server.

   Not only are PaaS services such as Azure SQL Database often less expensive to run, but because they're managed for you, you don't need to worry about software updates, security patches, or optimizing physical storage for read and write operations.

   **Save on licensing costs**

   Licensing is another area that can dramatically impact your cloud spending. Let's look at some ways you can reduce your licensing costs.

   **Choose cost-effective operating systems**

   Many Azure services provide a choice of running on Windows or Linux. In some cases, the cost depends on which you choose. When you have a choice, and your application doesn't depend on the underlying operating system, it's useful to compare pricing to see whether you can save money.

   **Use Azure Hybrid Benefit to repurpose software licenses on Azure**

   If you've purchased licenses for Windows Server or SQL Server, and your licenses are covered by Software Assurance, you might be able to repurpose those licenses on VMs on Azure.

   Some of the details vary between Windows Server or SQL Server. We'll provide resources at the end of this module where you can learn more.

### Describe Azure Service Level Agreements (SLAs) and service lifecycles
1. describe the purpose of an Azure Service Level Agreement (SLA) [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/examine-privacy-compliance-data-protection-standards/5-access-azure-compliance-documentation)

   A service-level agreement (SLA) is a formal agreement between a service company and the customer. For Azure, this agreement defines the performance standards that Microsoft commits to for you, the customer.

   In this part, you'll learn more about Azure SLAs, including why SLAs are important, where you can find the SLA for a specific Azure service, and what you'll find in a typical SLA.

   **Why are SLAs important?**

   Understanding the SLA for each Azure service you use helps you understand what guarantees you can expect.

   When you build applications on Azure, the availability of the services that you use affect your application's performance. Understanding the SLAs involved can help you establish the SLA you set with your customers.

   Later in this module, you'll learn about some strategies you can use when an Azure SLA doesn't meet your needs.

   **Where can I access SLAs for Azure services?**

   You can access SLAs from Service Level Agreements.

   Each Azure service defines its own SLA. Azure services are organized by category.

   **What's in a typical SLA?**

   A typical SLA breaks down into these sections:

   *Introduction*

   This section explains what to expect in the SLA, including its scope and how subscription renewals can affect the terms.

   *General terms*

   This section contains terms that are used throughout the SLA so that both parties (you and Microsoft) have a consistent vocabulary. For example, this section might define what's meant by downtime, incidents, and error codes.

   This section also defines the general terms of the agreement, including how to submit a claim, receive credit for any performance or availability issues, and limitations of the agreement.

   *SLA details*

   This section defines the specific guarantees for the service. Performance commitments are commonly measured as a percentage. That percentage typically ranges from 99.9 percent ("three nines") to 99.99 percent ("four nines").

   The primary performance commitment typically focuses on uptime, or the percentage of time that a product or service is successfully operational. Some SLAs focus on other factors as well, including latency, or how fast the service must respond to a request.

   This section also defines any additional terms that are specific to this service.

   Take a moment to review the SLA for Azure Database for MySQL.

   You see that this SLA focuses mainly on uptime. Azure Database for MySQL guarantees 99.99 percent, or "four nines", uptime. This means that the service is guaranteed to be running and available to process requests 99.99 percent of the time.

   **How do percentages relate to total downtime?**

   Downtime refers to the time duration that the service is unavailable.

   The difference between 99.9 percent and 99.99 percent might seem minor, but it's important to understand what these numbers mean in terms of total downtime.

   Here's a table to give you a sense of how total downtime decreases as the SLA percentage increases from 99 percent to 99.999 percent:

    | SLA percentage | Downtime per week | Downtime per month | Downtime per year |
    | -------------- | ----------------- | ------------------ | ----------------- |
    | 99             | 1.68 hours        | 7.2 hours          | 3.65 days         |
    | 99.9           | 10.1 minutes      | 43.2 minutes       | 8.76 hours        |
    | 99.95          | 5 minutes         | 21.6 minutes       | 4.38 hours        |
    | 99.99          | 1.01 minutes      | 4.32 minutes       | 52.56 minutes     |
    | 99.999         | 6 seconds         | 25.9 seconds       | 5.26 minutes      |

   These amounts are cumulative, which means that the duration of multiple different service outages would be combined, or added together.

   **What are service credits?**

   A service credit is the percentage of the fees you paid that are credited back to you according to the claim approval process.

   An SLA describes how Microsoft responds when an Azure service fails to perform to its specification. For example, you might receive a discount on your Azure bill as compensation when a service fails to perform according to its SLA.

   Credits typically increase as uptime decreases. Here's how credits are applied for Azure Database for MySQL according to uptime:

   | Monthly uptime percentage | Service credit percentage |
   | ------------------------- | ------------------------- |
   | < 99.99                   | 10                        |
   | < 99                      | 25                        |
   | < 95                      | 100                       |

   **What's the SLA for free services?**

   Free products typically don't have an SLA.

   For example, many Azure services provide a free or shared tier that provides more limited functionality. Services like Azure Advisor are always free. The SLA for Azure Advisor states that because it's free, it doesn't have a financially backed SLA.

   **How do I know when there's an outage?**

   Azure status provides a global view of the health of Azure services and regions. If you suspect there's an outage, this is often a good place to start your investigation.

   Azure status provides an RSS feed of changes to the health of Azure services that you can subscribe to. You can connect this feed to communication software such as Microsoft Teams or Slack.

   From the Azure status page, you can also access Azure Service Health. This provides a personalized view of the health of the Azure services and regions that you're using, directly from the Azure portal.

   **How can I request a service credit from Microsoft?**

   Typically, you need to file a claim with Microsoft to receive a service credit. If you purchase Azure services from a Cloud Solution Provider (CSP) partner, your CSP typically manages the claims process.

   Each SLA specifies the timeline by which you must submit your claim and when Microsoft processes your claim. For many services, you must submit your claim by the end of the calendar month following the month in which the incident occurred.

2. identify actions that can impact an SLA (i.e. Availability Zones) [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/choose-azure-services-sla-lifecycle/4-design-application-meet-sla)

   **Combine SLAs to compute the composite SLA**

   After you've identified the SLA for the individual workloads in the Special Orders application, you might notice that those SLAs are not all the same. How does this affect our overall application SLA requirement of 99.9 percent? To work that out, you'll need to do some math.

   The process of combining SLAs helps you compute the composite SLA for a set of services. Computing the composite SLA requires that you multiply the SLA of each individual service.

   **Choose customization options that fit your required SLA**

   Each of the workloads defined for an application has its own SLA, and the customization choices you make when you provision each workload affects that SLA. For example:

   *Disks*

   With Virtual Machines, you can choose from a Standard HDD Managed Disk, a Standard SSD Managed Disk, or a Premium SSD or Ultra Disk. The SLA for a single VM would be either 95 percent, 99.5 percent or 99.9 percent, depending on the disk choice.

   *Tiers*

   Some Azure services are offered as both a free tier product and as a standard paid service. For example, Azure Automation provides 500 minutes of job runtime in an Azure free account, but is not backed by an SLA. The standard tier SLA for Azure Automation is 99.9 percent.

   Make sure that your purchasing decisions take into account the impact on the SLA for the Azure services that you choose. Doing so ensures that the SLA supports your required application SLA.

   **Include redundancy to increase availability**
   To ensure high availability, you might plan for your application to have duplicate components across several regions, known as redundancy. Conversely, to minimize costs during non-critical periods, you might run your application only in a single region. Tailwind Traders might consider this if there's a trend that the special order rates are much higher during certain months or seasons.

   To achieve maximum availability in your application, add redundancy to every single part of the application. This redundancy includes the application itself, as well as the underlying services and infrastructure. Be aware, however, that doing so can be difficult and expensive, and often results in solutions that are more complex than they need to be.

3. describe the service lifecycle in Azure (Public Preview and General Availability) [Microsoft Learn Reference](https://docs.microsoft.com/en-us/learn/modules/choose-azure-services-sla-lifecycle/5-access-preview-services)

   The service lifecycle defines how every Azure service is released for public use.

   Every Azure service starts in the development phase. In this phase, the Azure team collects and defines its requirements, and begins to build the service.

   Next, the service is released to the public preview phase. During this phase, the public can access and experiment with it so that it can provide feedback. Your feedback helps Microsoft improve services. More importantly, providing feedback gives you the opportunity to request new or different capabilities so that services better meet your needs.

   After a new Azure service is validated and tested, it's released to all customers as a production-ready service. This is known as general availability (GA).

   **What terms and conditions can I expect?**

   Each Azure preview defines its own terms and conditions. All preview-specific terms and conditions supplement your existing Azure service agreement.

   Some previews aren't covered by customer support. Therefore, previews are not recommended for business-critical workloads.

   **How can I access preview services?**

   You can access preview services from the Azure portal.
   Here's how to see what preview services are available. 

   * Go to the Azure portal and sign in.
   * Select Create a resource.
   * Enter preview in the search box, and select Enter.
   * Select a service to learn more about it. You can also launch the service if you'd like to try it out.

   **How can I access new features for an existing service?**

   Some preview features relate to a specific area of an existing Azure service. For example, a compute or database service that you use daily might provide enhanced functionality. These preview features are accessible when you deploy, configure, and manage the service.

   Although you can use an Azure preview feature in production, make sure you're aware of any limitations around its use before you deploy it to production.

   **How can I access preview features for the Azure portal?**

   You can access preview features that are specific to the Azure portal from Microsoft Azure (Preview).

   Typical portal preview features provide performance, navigation, and accessibility improvements to the Azure portal interface.

   You see Microsoft Azure (Preview) near the menu bar to remind you that you're working with a preview version of the Azure portal.
   