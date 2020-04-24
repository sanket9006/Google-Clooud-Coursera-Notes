# Google-Clooud-Coursera-Notes



## <p align="center">  Managed Instance Groups</p>

A managed instance group is a collection of identical virtual machine instances that you control as a single entity using an instance template. You can easily update all the instances in the group by specifying a new template in a rolling update.

If an instance in the groups stops, crashes, or is deleted by an action other than the instance groups command, the managed instance group automatically recreates the instance so it can resume its processing tasks.

Regional managed instance groups are generally recommended over zonal managed instance groups because they allow you to spread the application load across multiple zones instead of confining your application to a single zone or you're having to manage multiple instance groups across different zones.

