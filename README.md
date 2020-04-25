# Google Clooud Coursera Notes

## <p align="center"> Overview of HTTP(S) load balancing </p>
HTTP requests are load balanced on port 80 or 8080, and HTTPS requests are load balanced on port 443.
he backend services contain a health check, session affinity, a timeout setting, and one or more backends. A health check pulls instances attached to the backend service at configured intervals. Instances that pass the health check are allowed to receive new requests. Unhealthy instances are not sent requests until they are healthy again. Normally, HTTPS load balancing uses a round robin algorithm to distribute requests among available instances.
             If there are no healthy instances, with available capacity in a given region, the load balancer instead sends the request to the next closest region with available capacity. Therefore, traffic from the EMEA user, could be forwarded to the US Central 1-a back-end, if the Europe West 1-d back-end does not have capacity, or has no healthy instances as determined by the health checker. This is referred to as cross-region load balancing.

## <p align="center">  Managed Instance Groups</p>

A managed instance group is a collection of identical virtual machine instances that you control as a single entity using an instance template. You can easily update all the instances in the group by specifying a new template in a rolling update.

If an instance in the groups stops, crashes, or is deleted by an action other than the instance groups command, the managed instance group automatically recreates the instance so it can resume its processing tasks.

Regional managed instance groups are generally recommended over zonal managed instance groups because they allow you to spread the application load across multiple zones instead of confining your application to a single zone or you're having to manage multiple instance groups across different zones.

First, decide whether the instance group is going to be single or multi zoned and where those locations will be. Second, choose the ports that you are going to allow and load balance across. Third, select the instance template that you want to use. Fourth, decide whether you want to auto-scale and under what circumstances. Finally, consider creating a health check to determine which instances are healthy and should receive traffic. Essentially, you're still creating virtual machines, but you're applying more rules to that instance group.


Managed instance groups offer autoscaling capabilities that allow you to automatically add or remove instances from a managed instance group based on increase or decrease in load. Autoscaling helps your applications gracefully handle increase in traffic and reduces cost when the need for resource is lower.

Another important configuration for a managed instance group and load balancer is a health check. A health check is very similar to an Uptime check in Stackdriver. You just define a protocol, port, and health criteria . Based on this configuration, GCP computes a health state for each instance.
