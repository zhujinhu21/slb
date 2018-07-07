# What is Server Load Balancer {#concept_whs_lp4_tdb .concept}

Server Load Balancer \(SLB\) is a traffic distribution control service that distributes the incoming traffic among multiple Elastic Compute Service \(ECS\) instances according to the configured forwarding rules. SLB expands application service capabilities and enhances application availability.

SLB virtualizes the added ECS instances into a high-performance and highly available application service pool by setting virtual service addresses, and distributes the requests from clients to ECS instances in the backend server pool based on forwarding rules.

By default, SLB checks the health status of the added backend servers, and isolates abnormal ECS instances automatically to eliminate single point of failure \(SPOF\) on a single ECS instance and improves the overall service capability of an application. In addition, the SLB is able to resist DDoS attacks, enhancing application service protection.

## Components {#section_ppv_hq4_tdb .section}

SLB consists of three parts:

-   SLB instances

    A Server Load Balancer instance is a running load balancing service that receives and distributes the incoming traffic to the backend servers. To use the Server Load Balancer service, you must create a Server Load Balancer instance with at least one listener and two ECS instances configured.

-   Listeners

    A listener checks the client requests and forwards the requests to the backend servers.  It also performs health check on the backend servers.

-   Backend servers

    Backend servers are the ECS instances added to a Server Load Balancer instance to process the distributed requests. You can either add the ECS instances to the backend server pool or group the ECS instances hosting different applications or functioning different roles into different server groups.

    As shown in the following figure, after the Server Load Balancer instance receives a client request, the listener forwards the request to the corresponding backend ECS instances according to the configured listening rules.

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/4091/936_zh-CN.png)


## Benefits {#section_ws5_vq4_tdb .section}

-   High availability

    Server Load Balancer is designed to work in the full-redundancy mode without SPOF. Server Load Balancer supports local and cross-region disaster tolerance.  When Server Load Balancer is used together with DNS, the service availability is up to 99.95%.

    You can scale your service based on the application load, without interrupting services continuity.

-   Cost-effective

    Compared with the traditional hardware load balancing system, Server Load Balancer reduces the cost by 60%.

-   Security

    Alibaba Cloud makes a full optimization on Keepalived, an open-source software used to manage LVS. Therefore, the Layer-4 Server Load Balancer that is based on LVS is able to provide real-time defense. Combined with Alibaba Cloud Security, Server Load Balancer can defend against up to 5 Gbps DDoS attacks, such as HTTP flood and SYN flood attacks.

    Using Tengine as the basic module, the Layer-7 Server Load Balancer can provide multi-dimensional CC attack defenses.


