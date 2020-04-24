# Google Clooud Coursera Notes



## <p align="center">  Managed Instance Groups</p>

A managed instance group is a collection of identical virtual machine instances that you control as a single entity using an instance template. You can easily update all the instances in the group by specifying a new template in a rolling update.

If an instance in the groups stops, crashes, or is deleted by an action other than the instance groups command, the managed instance group automatically recreates the instance so it can resume its processing tasks.

Regional managed instance groups are generally recommended over zonal managed instance groups because they allow you to spread the application load across multiple zones instead of confining your application to a single zone or you're having to manage multiple instance groups across different zones.

First, decide whether the instance group is going to be single or multi zoned and where those locations will be. Second, choose the ports that you are going to allow and load balance across. Third, select the instance template that you want to use. Fourth, decide whether you want to auto-scale and under what circumstances. Finally, consider creating a health check to determine which instances are healthy and should receive traffic. Essentially, you're still creating virtual machines, but you're applying more rules to that instance group.


Managed instance groups offer autoscaling capabilities that allow you to automatically add or remove instances from a managed instance group based on increase or decrease in load. Autoscaling helps your applications gracefully handle increase in traffic and reduces cost when the need for resource is lower.

Another important configuration for a managed instance group and load balancer is a health check. A health check is very similar to an Uptime check in Stackdriver. You just define a protocol, port, and health criteria . Based on this configuration, GCP computes a health state for each instance.
