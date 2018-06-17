# Plan and prepare {#concept_ug3_rfl_vdb .concept}

Before using Server Load Balancer, you must determine the listener type and network type of Server Load Balancer according to your business.

## Plan the region of the Server Load Balancer instance {#section_nby_m4l_vdb .section}

Alibaba Cloud provides the Server Load Balancer service in various regions.

To provide more stable and reliable load balancing services, multiple zones for Server Load Balancer are deployed in most regions for better disaster tolerance. In addition, you can create multiple load balancing instances in different regions, improve cross-geographic availability by providing services to the outside world through DNS polling.

Note the following when selecting the region where the SLB instance is created:

-   To reduce latency and increase the download speed, we recommend that you choose a region that is physically closest to the region where your customers are located.
-   Server Load Balancer does not support cross-region deployment. Ensure that the region is the same for the Server Load Balancer and the backend ECS instances.

## Plan the instance type \(Internet or intranet\) {#section_o3k_44l_vdb .section}

Choose the instance type based on your business type. After you create a Server Load Balancer instance, a private or public IP is allocated. You can resolve a domain name to the IP to provide services using the domain name.

-   An Internet Server Load Balancer instance only has a public IP and is accessible from the Internet.

    If you choose the Internet type, you also need to choose the billing method:

    -   Billing by traffic: Suitable for an application with obvious traffic changes.
    -   Billing by bandwidth: Suitable for an application with relatively stable bandwidth.
-   An intranet Server Load Balancer instance only has a private IP and is accessible only from a classic network or VPC. Intranet Server Load Balancer instances are free of charge.

## Plan the listening protocol {#section_bhq_r4l_vdb .section}

Server Load Balancer supports Layer-4 \(TCP and UDP\) and Layer-7 \(HTTP and HTTPS\) load balancing.

-   A Layer-4 listener distributes connection requests directly to backend servers without modifying HTTP headers. After a request arrives at a Layer-4 listener, the SLB server uses the backend port configured in the listener to create a TCP connection with backend ECS instances.
-   A Layer-7 listener is an implementation of reverse proxy. After a request arrives at a Layer-7 listener, the SLB server uses a TCP connection to transmit the data packets to backend ECS instances instead of transmitting the data packets directly.

    The Layer-7 listener has one more procedure than the Layer-4 listener when forwarding incoming requests. Due to this additional procedure, the performance of the Layer-7 listener is less efficient to that of the Layer-4 listener. In addition, scenarios such as insufficient client ports and excessive connections to backend servers also affect the performance of the Layer-7 listeners. If you have high performance requirements, we recommend that you use Layer-4 listeners.


## Prepare the backend servers {#section_f5v_54l_vdb .section}

You must add ECS instances to the backend server pool of Server Load Balancer to process the distributed client requests. Before using Server Load Balancer, create at least two ECS instances and deploy corresponding applications. Note the following when creating ECS instances:

-   ECS regions and zones

    Make sure the region is the same for the ECS instances and Server Load Balancer instance. Additionally, we recommend that you deploy the ECS instances in different zones to improve availability.

-   ECS Configurations

    No additional configuration is not required after applications are deployed on the ECS instances.  However, if you create a Layer-4 listener, and the ECS instances use the Linux operating system, make sure the values of the following parameters in the nnet.ipv4.conf file are 0:

    ```
    
    net.ipv4.conf.default.rp_filter = 0
    net.ipv4.conf.all.rp_filter = 0
    net.ipv4.conf.eth0.rp_filter = 0
    ```

-   ECS deployment

    There is no restriction on the number of ECS instances added to a Server Load Balancer instance. To improve service stability and efficiency, we recommend that you add ECS instances responsible for different tasks or services to different Server Load Balancer instances.


