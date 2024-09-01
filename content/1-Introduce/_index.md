---
title : "Introduction"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b> 1. </b> "
---
**Load Balancer** is a device or software used to distribute network or application traffic evenly across multiple servers or other resources. The main goal of a load balancer is to ensure that no single server is overwhelmed, thereby improving the performance, reliability, and scalability of the system.

**Elastic Load Balancing** is an AWS Load Balancing service that ensures requests are balanced between targets.

Key features include:

- High Availability
- Scalability: theoretically unlimited
- High Security: When combined with other services like WAF, Security Group.
ELB can easily integrate with various backends using EC2, Container, Lambda.

**Basic components of Load Balancer**

- **Target Group**: A group of servers managed by the load balancer to distribute traffic.
- **Listener**: Defines how the load balancer receives incoming traffic and routes it to target groups.
- **Rule**: Defines how the load balancer routes traffic to target groups.
- **Health Check**: Checks the status of servers in the target group.

**How does Load Balancer work?**

By default, the Load Balancer distributes requests from clients to targets in a Target Group in a balanced manner (round robin), even if the target is in more than one target group.

Example:
![vd1](/images/1.introduce/vd1.png)

In the above image, each instance will receive ~16.7% of the requests from clients.

The Load Balancer can route to more than one target. In the case of multi-target, the routing to a target is determined by several rules:

- Listener port (the port requested by the user will be routed to the corresponding target group)
- Path pattern (Application LB only)
- Fixed ratio. For example, Target Group 01 receives 20%, Target Group 02 receives 80% of the traffic (in scenarios where we want to release a new feature to 20% of users to gather feedback).