# Introduction
This section creates a sample web site that uses Amazon EC2 Auto Scaling and Elastic Load Balancing and is configured to use multiple Availability Zones. 
The template also contains CloudWatch alarms that execute scaling policies to add or remove instances from the Auto Scaling group when the defined thresholds are exceeded.

# Break-down CFN templates - some basic templates from infrastructure section will be used.
01.vpc_1.yaml
02.security_group_1.yaml
03.networkACL_1.yaml
