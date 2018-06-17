# Tutorial overview {#concept_ybd_pfl_vdb .concept}

This section provides a complete tutorial on using Server Load Balancer. An Internet-facing Server Load Balancer instance is created to distribute received HTTP requests to backend servers.

**Note:** Before creating a Server Load Balancer instance, you must plan and design your load balancing service, such as the instance type, instance region, and more. For more information, see [Plan and prepare](reseller.en-US/Quick Start/Plan and prepare.md#).

The tutorial includes the following tasks:

1.  [Create ECS instances](reseller.en-US/Quick Start/Create ECS instances.md#)

    Server Load Balancer is a complementary service for ECS multi-machine solutions, and must be used in conjunction with ECS. In this tutorial, two ECS instances are created to process the distributed traffic.

2.  [Install web pages](reseller.en-US/Quick Start/Install web pages.md#)

    Create required applications on the ECS instances. In this tutorial, a static web page is created to test the load balancing service.

3.  [Create an SLB instance](reseller.en-US/Quick Start/Create an SLB instance.md#)

    Create an SLB instance. An SLB instance is a running entity of Server Load Balancer. In this tutorial, an Internet-facing Server Load Balancer instance is created.

4.  [Configure listeners and add backend servers](reseller.en-US/Quick Start/Configure the SLB instance.md#)

    After creating an SLB instance, you have to add at least one listener, and add ECS instances as backend servers. In this tutorial, a TCP listener is added, and the ECS instances created in task 1 are used as backend servers.

5.  [Resolve domain name](reseller.en-US/Quick Start/Resolve domain name.md#) \(Optional\)

    Use Alibaba Cloud DNS to resolve a domain name to the IP address of the SLB instance. Therefore, you can use the domain name to provide services.

6.  [Release the SLB instance](reseller.en-US/Quick Start/Release the SLB instance.md#)

    If you no longer need Server Load Balancer, release it to avoid additional charges.


