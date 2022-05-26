# AWS *Elasticsearch* Load Balancing - Definition, Features & Benefits
AWS elasticsearch service is an open-source analytics and full-text search engine used for enabling search functionalities (such as log analytics, real-time application monitoring and click stream analytics) for applications. 

Elastic load balancing can automatically circulate incoming traffic across distinct targets such as EC2 instances, containers, and IP addresses, to name a few. It keeps track of the health of its registered targets and only sends traffic to those who are in good shape.

Elastic Load Balancing allows the user to scale their load balancer as their incoming traffic fluctuates. It can inevitably scale to the vast majority of workloads. 

##  How Does AWS Load Balancer Work?
AWS elasticsearch circulates workload through a load balancer among various compute resources, namely virtual servers. A load balancer improves the applications' availability and fault tolerance.  The load balancing specialists can add or subtract compute resources from the load balancer without interrupting their apps' overall flow of requests the overall flow of requests to their apps.

They can even configure health checks to monitor the health of the computing resources so that the load balancer only sends requests to those that are in good shape. They can also use the load balancer to handle encryption and decryption so that the computational resources can focus on their primary tasks.

It works this way:
- Load balancer accepts incoming traffic from clients.
- Then, it sends the route requests to its registered targets in the availability zones.
- It screens the health of its registered targets to ensure it routes to the healthy ones.
- Furthermore, when it detects any unhealthy target, it stops routing traffic to them.
- When it finds that the target is healthy again, it resumes directing traffic to it.

By specifying one or more listeners, the specialists setup the load balancer to receive incoming traffic. A **listener** is a process that monitors for connection requests. To build a connection with the clients and the load balancer, it is configured with a protocol and port number. For the connections from the load balancer to the targets, it also follows a specific configuration and port number. It supports the following groups of load balancers:
- Application Load Balancers
- Network Load Balancers
- Gateway Load Balancers
- Classic Load Balancers 

The configuration of the load balancer types differs significantly. Specialists register targets in target groups and route traffic there using Application Load Balancers, Network Load Balancers, and Gateway Load Balancers. They register instances with the load balancer with Classic Load Balancers.

## AWS *Elasticsearch* Challenges 

AWS-hosted elasticsearch produces direct Elasticsearch access that enables specific configurations and customizations to fit the users’ application’s exact needs. Yet, there are a few drawbacks with the legacy system that AWS supports. 

The first is that, one can only run maximum of 10 instances per cluster. A service request needs to be submitted if there’s a requirement for two.

The second error is found with the node memory.

However, Elasticsearch is not solely a log management solution. It's one amongst the many components required to build up a log management solution. One can directly access the Elastic Open source API’s so that the code and applications can easily function.

## How is the Challenge Being Resolved?

Securing Amazon Elasticsearch Service (Amazon ES) domain ensures the data aren't being accessed or altered by unauthorized users. Most customers prefer open access over IP address or identity-based access controls because it is more convenient. This option is not ideal for most customers because a domain with open access will accept requests from any entity on the Internet to create, read, alter, and delete data from the Amazon ES domain.

The domain Amazon ES comprises the nodes in the Elasticsearch cluster and resources from several AWS services. When one builds a domain using Amazon ES, it creates instances in a service-controlled VPC. Elastic Load Balancing (ELB) is used to overlook those instances, and the load balancer's endpoint is published through Route 53. Requests to the domain are sent to the domain's EC2 instances through the ELB load balancer. Regardless of where the request is sent, the instance contacts IAM to see if it is approved. Requests that are not allowed are blocked and ignored.

## Approaches Taken to Ease Out Elastic Load Balancing

One can use any of the following APIs to create, access, and administer your load balancers:

- AWS Management Console— Providing a web interface that one can use to access Elastic Load Balancing.
-  AWS Command Line Interface (AWS CLI) — Providing commands for a broad set of AWS services, including Elastic Load Balancing. This is supported on Windows, macOS, and Linux. 
- AWS SDKs — Delivers language-specific APIs and handles different kinds of the connection intricacies, such as calculating signatures, handling request retries, and resolving errors. 
- Query API— Enables low-level API actions that generally known as HTTPS requests. The Query API is the quickest method to get started with Elastic Load Balancing. However, the Query API requires the application to handle low-level details such as generating the hash to sign the request, and error handling.

## Conclusion

The OpenSearch Service is a critical component for the search and analytics infrastructure's operational stability, security, and performance. The decision to move is simple when one considers the following benefits provided by OpenSearch Service:

- Innovative UltraWarm functionality , to help you manage your costs.
- Ability to delegate operational procedures to a seasoned vendor who understands how to scale OpenSearch
- Plugins that enable fine-grained access, vector-based similarity algorithms, or warning and monitoring with the potential to automate incident response are available at no additional cost.
