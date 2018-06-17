# Create an SLB instance {#task_bh5_dll_vdb .task}

Before using Server Load Balancer, you need to create a Server Load Balancer instance. You can add multiple listeners and backend servers to the Server Load Balancer instance. This tutorial shows you how to create an Internet-facing SLB instance. After the instance is created, a public IP is allocated to it. You can resolve a domain name to this IP.

1.   Log on to the [SLB console](https://partners-intl.console.aliyun.com/#/slb). 
2.  On the Instances page, click **Create Server Load Balancer**. 
3.   Select a billing method. In this tutorial, select **Pay-As-You-Go**.
4.   Configure the instance according to the descriptions in [Configure SLB instances](../../../../reseller.en-US/User Guide/Server Load Balancer instance/Create a Server Load Balancer instance.md#). The configurations for the Server Load Balancer instance in this tutorial are as follows:
    -   **Region**: Server Load Balancer does not support cross-region deployment. The region must be the same for the Server Load Balancer instance and ECS instances. In this tutorial, select **China \(Hangzhou\)**, which is the region of the ECS instances.
    -   **Zone type**: Multiple zones have been deployed in most regions for better disaster tolerance. When the SLB service is unavailable in the primary zone, it switches to a backup zone to restore service \(within 30 seconds\). Then, it will automatically switch back to the primary zone when service in the primary zone is recovered.

        In this tutorial, select **China East 1 Zone B** as the primary zone and **China East 1 Zone D** as the backup zone.

    -   **Instance type**: Select **Internet**.

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/4107/2264_en-US.png)

5.   Click **Buy Now** and complete the payment. 
6.   Go back to the SLB console. 
7.   On the Instances page, select the **China \(Hangzhou\)** region. Hover the mouse pointer over the instance ID and then click the pencil icon. Enter **SLB1** as the name of the instance, click **Confirm**. 

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/4107/2271_en-US.png)


