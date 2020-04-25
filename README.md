# Google Clooud Coursera Notes

## <p align="center">Elastic Google Cloud Infrastructure: Scaling and Automation : Week 1 : Module Review </p>


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
