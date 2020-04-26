# Google Clooud Coursera Notes

Validate your hands-on GCP skills and advance your career with the Associate Cloud Engineer certification. Certification can help you gain credibility and give you an advantage in today’s highly competitive market. The Associate Cloud Engineer certification is for individuals who want to demonstrate their ability to deploy applications, monitor operations, and maintain cloud projects on Google Cloud Platform. It is recommended that you have at least 6 months of hands-on experience working with GCP. The exam will assess your ability to:

Set up a cloud solution environment
Plan and configure a cloud solution
Deploy and implement a cloud solution
Ensure successful operation of a cloud solution
Configure access and security
I recommend broadening your knowledge by completing the following Qwiklabs Self-Paced Labs, which are single-topic hands-on activities; and Qwiklabs Quests, which are groups of self-paced labs on a focused theme:

Quest: Kubernetes in the Google Cloud
Quest: Google Kubernetes Engine Best Practices
Self-Paced Lab: Cloud Functions - Qwik Start
Self-Paced Lab: Deploying the Application into App Engine Flexible Environment - Java OR Deploying the Application into App Engine Flexible Environment - Python
To help you structure your preparation for the Associate Cloud Engineer exam, we recommend the Preparing for the Associate Cloud Engineer Examination course.

You can also prepare using the Official Google Cloud Certified Associate Cloud Engineer Study Guide, published by Wiley. Visit the Google Cloud Certification website for more information and to register.

Good luck!
## <p align="center">GCP Marketplace</p>

GCP marketplace lets you quickly deploy functional software packages that run on GCP. Essentially, GCP marketplace offers production grade solutions from third-party vendors who have already created their own deployment configurations based on Deployment Manager. These solutions are built together with all of your projects GCP services. If you already have a license for a third party service, you might be able to use a Bring Your Own License solution. You can deploy a software package now and scale that deployment later when your applications require additional capacity. GCP even updates the images of these software packages to fix critical issues and vulnerabilities but doesn't update software that you have already deployed. You even get direct access to partner support.

 A LAMP stack consists of Linux, Apache HTTP Server, MySQL, and PHP

## <p align="center">Module Review</p>

In this module, we automated the deployment of Infrastructure using Deployment Manager and Terraform and launched the Infrastructure solutions using GCP marketplace. Now, you might say that going through all the effort to deploy a network, firewalls rule, and the two Virtual Machine instances doesn't convince you to use Deployment Manager or Terraform. That's true if you only need to create these resources once and don't foresee ever creating them again. However, for those of us who manage several resources and need to deploy, update, and destroy them in a repeatable way Infrastructure Automation tools like Deployment Manager and Terraform become essential.




## <p align="center">BigQuery</p>

BigQuery is GCP's serverless, highly scalable, and cost effective Cloud data warehouse. It's a petabyte scale data warehouse that allows for super-fast queries using the processing power of Google's infrastructure. Because there's no infrastructure for you to manage, you can focus on uncovering meaningful insights using familiar SQL, without the need for the database administrator. BigQuery is used by all types of organizations, and there's a free usage tier to help you get started. For more information, see the links section of this video. You can access BigQuery by using the GCP console, by using the command line tool, or by making calls to the BigQuery REST API, using the variety of client libraries such as Java,.NET or Python. There are also several third-party tools that you can use to interact with BigQuery, such as visualizing the data, or loading the data. Here's an example of a query on the table with over 100 billion rows. This query processes over 4.1 terabyte, but takes less than a minute to execute. The same query would take hours if not days through a serial execution.


## <p align="center">Cloud Dataproc</p>

Let's learn a little bit about Cloud Dataproc. Cloud Dataproc is a fast easy to use fully managed Cloud service for running Apache Spark and Apache Hadoop clusters in a simpler way. You only pay for the resources you use with per second billing. If you leverage preemptible instances in your cluster, you can reduce your costs even further. Without using Cloud Dataproc, it can take from five to 30 minutes to create Spark and Hadoop clusters On-premise or through other infrastructure as a service providers. Cloud Dataproc clusters are quick to start, scale, and shut down with each of these operations taking 90 seconds or less on average. This means you can spend less time waiting for clusters and more hands-on time working with your data. Cloud Dataproc has built-in integration with other GCP services such as BigQuery, Cloud Storage, Cloud Bigtable, Stackdriver Logging, and Stackdriver monitoring. This provides you with the complete data platform rather than just a Spark or Hadoop cluster. As a managed service, you can create clusters quickly, manage them easily, and save money by turning clusters off when you don't need them. With less time and money spent on administration, you can focus on your jobs and your data. If you're already using Spark, Hadoop, Pig or Hive you don't even need to learn new tools or API's is to use Cloud Dataproc. This makes it easy to move existing projects into Cloud Dataproc without redevelopment. Now, Cloud Dataproc and Cloud Dataflow can both be used for data processing, and there's overlap in their batch and streaming capabilities. So how do you decide which product is a better fit for your environment? But first ask yourself whether you have dependencies on specific tools or packages in the Apache Hadoop or Spark ecosystem. If that's the case, you'll obviously want to use Cloud Dataproc. If not, ask yourself whether you prefer a hands-on or DevOps approach to Operations or a hands-off or serverless approach. If you opt for the DevOps approach, you want to use Cloud Dataproc. Otherwise, use Cloud Dataflow.


In this module, we provided you with an overview of managed services for data processing in GCP, namely BigQuery Cloud Dataflow, Cloud Dataprep, and Cloud Dataproc. Managed services allow you to outsource a lot of the administrative and maintenance overhead to Google, so you can focus on your workloads instead of infrastructure. Speaking of Infrastructure, most of the services that we covered our serverless. Now, this doesn't mean that there aren't any actual servers processing your data. Serverless means that servers or compute engine instances are obfuscated so that you don't have to worry about the Infrastructure. Cloud Dataproc isn't a serverless service because you were able to view and manage the underlying master and worker instances.


## <p align="center">Deployment Manager</p>

Deployment Manager takes this one step further. Deployment Manager is an infrastructure deployment service that automates the creation and management of GCP resources for you. You just specify all the resources needed for your application in a declarative format and deploy your configuration. This deployment can be repeated over and over with consistent results and you can delete a whole deployment with one command or click.

 By definition, an auto mode network automatically creates a subnetwork in each region. Therefore, I am setting the auto-create subnetworks property to true. 

 Now there are other infrastructure automation tools in addition to Deployment Manager that you can use in GCP. You can also use Terraform, CHEF, Puppet, Ansible, or Packer. All of these tools allow you to treat your infrastructure like software, which helps you decrease costs, reduce risk, and deploy faster by capturing infrastructure as code.
 
 Lab Intro: Automating the Infrastructure of Networks Using Deployment Manager or Terraform

In this lab we're giving you two choices. You can deploy resources by using Deployment Manager or Terraform. Either way, you deploy an automotive network called my network with a firewall rule to allow HTTP, SSH, RDP, and ICMP traffic. You also deploy the VM instances shown in this network diagram. Again, you have the choice of deploying these resources with Deployment Manager or Terraform through two separate labs. You can complete either lab or even both.

## <p align="center">Week 2 Module Overview </p>

Deployment manager uses a system of highly structured templates and configuration files to document the infrastructure in an easily readable and understandable format. Deployment manager conceals the actual Cloud API calls. So you don't need to write code and can focus on the definition of the infrastructure. In this module, we cover how to use deployment manager to automate the deployment of infrastructure, and how to use GCP marketplace to launch infrastructure solutions.

## <p align="center">Elastic Google Cloud Infrastructure: Scaling and Automation </p>

## <p align="center">Week 1 : Module Review </p>

In this module, we looked at the different types of load balancers that are available in GCP along with the managed instance groups and auto-scaling. You will able to apply most of the covered services and concepts by working through the two labs of this module. We also discussed the criteria for choosing between the different load balancers and looked at a flowchart and summary table to help you pick the right load balancers. Remember, sometimes it's useful to combine an internal and external load balancer to support three tier web services.


## <p align="center"> Choosing a load balancer </p>

let me help you determine which load balancer best meets your need. One differentiator between the different GCP load balancers is the support for IPv6 clients. Only the HTTPS, SSL proxy, and TCP proxy load balancing services support IPV6 clients

![image](https://github.com/sanket9006/Google-Clooud-Coursera-Notes/blob/master/Capture.PNG)




## <p align="center"> Internal load balancing </p>
 Internal load balancing is a regional, private load balancing service for TCP and UDP based traffic. In other words, this load balancer enables you to run and scale your services behind a private load balancing IP address. This means that it is only accessible through the internal IP address of virtual machine instances that are in the same region. Therefore, use internal load balancing to configure an internal load balancing IP address, to act as the front end to your private backend instances.


GCP internal load balancing is not based on a device or a virtual machine instance. Instead, it is a software-defined, fully distributed load balancing solution. In the traditional proxy model of internal load balancing as shown on the left, you configure an internal IP address on a load balancing device or instances, and your client instance connects to this IP address. Traffic coming to the IP address is terminated at the load balancer, and the load balancer selects a backend to establish a new connection to. Essentially, there are two connections. One between the client and the load balancer, and the one between the load balancer and the backend. GCP internal load balancing distributes client instance requests to the backend using a different approach,

It uses lightweight load balancing built on top of Andromeda, Google's network virtualization stack, to provide software-defined load balancing that directly delivers the traffic from the client instance to a backend instance. To learn more about Andromeda



## <p align="center"> TCP proxy load balancing </p>

TCP proxy is a global load balancing service for unencrypted non-HTTP traffic. This load balancer terminates your customers TCP sessions at the load balancing layer, then forwards the traffic to your virtual machine instances using TCP or SSO

TCP proxy load balancing supports both IPv4 and IPv6 addresses for Client Traffic. Similar to SSL proxy load balancer, the TCP proxy load balancer provides intelligent routing and security patching


## <p align="center"> Overview of HTTP(S) load balancing </p>
HTTP requests are load balanced on port 80 or 8080, and HTTPS requests are load balanced on port 443.
he backend services contain a health check, session affinity, a timeout setting, and one or more backends. A health check pulls instances attached to the backend service at configured intervals. Instances that pass the health check are allowed to receive new requests. Unhealthy instances are not sent requests until they are healthy again. Normally, HTTPS load balancing uses a round robin algorithm to distribute requests among available instances.
             
             
  If there are no healthy instances, with available capacity in a given region, the load balancer instead sends the request to the next closest region with available capacity. Therefore, traffic from the EMEA user, could be forwarded to the US Central 1-a back-end, if the Europe West 1-d back-end does not have capacity, or has no healthy instances as determined by the health checker. This is referred to as cross-region load balancing.


An HTTP(S) load balancer has the same basic structure as the HTTP load balancer, but differs in the following ways. An HTTP(s) load balancer uses a target HTTPS proxy instead of a target HTTP proxy. An HTTPS load balancer requires at least one signed SSL certificate installed on the target HTTPS proxy for the load balancer. The client SSL session terminates at the load balancer. HTTPS load balancer support the QUIC transport layer protocol. QUIC is a transport layer protocol that allows faster client connection initiation, eliminates head of line blocking in multiplexed streams, and supports connection migration when a client's IP address changes


## <p align="center">  Managed Instance Groups</p>

A managed instance group is a collection of identical virtual machine instances that you control as a single entity using an instance template. You can easily update all the instances in the group by specifying a new template in a rolling update.

If an instance in the groups stops, crashes, or is deleted by an action other than the instance groups command, the managed instance group automatically recreates the instance so it can resume its processing tasks.

Regional managed instance groups are generally recommended over zonal managed instance groups because they allow you to spread the application load across multiple zones instead of confining your application to a single zone or you're having to manage multiple instance groups across different zones.

First, decide whether the instance group is going to be single or multi zoned and where those locations will be. Second, choose the ports that you are going to allow and load balance across. Third, select the instance template that you want to use. Fourth, decide whether you want to auto-scale and under what circumstances. Finally, consider creating a health check to determine which instances are healthy and should receive traffic. Essentially, you're still creating virtual machines, but you're applying more rules to that instance group.


Managed instance groups offer autoscaling capabilities that allow you to automatically add or remove instances from a managed instance group based on increase or decrease in load. Autoscaling helps your applications gracefully handle increase in traffic and reduces cost when the need for resource is lower.

Another important configuration for a managed instance group and load balancer is a health check. A health check is very similar to an Uptime check in Stackdriver. You just define a protocol, port, and health criteria . Based on this configuration, GCP computes a health state for each instance.
