# Create ECS instances {#task_bh5_dll_vdb .task}

Before using Server Load Balancer, you must create at least two ECS instances and deploy corresponding applications. Then, add the ECS instances to the Server Load Balancer instance to process distributed client requests.

Follow the instructions in this document to create two ECS instances, ECS01 and ECS02.

1.  Log on to the ECS console. 
2.  In the left-side navigation pane, click **Instances** and then click **Create Instance**. 
3.   On the Elastic Compute Services \(ECS\) page, configure the ECS instance. The following are ECS settings used in this tutorial. You can change the configuration according to your needs.

    -   **Region**: Server Load Balancer does not support cross-region deployment. The region must be the same for the Server Load Balancer instance and the ECS instances.  In this tutorial, select **China East 1**.
    -   **Network Type**: In this tutorial, select **VPC**. Use the default VPC and VSwitch.
    -   **Operating System**: In this tutorial, select Ubuntu 16.04 64 bit.
    -   **Number of Instances**: In this tutorial, select **2**. The system simultaneously creates two ECS instances with identical settings.
    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/4105/2201_en-US.png)

4.   Click **Buy Now** and complete the payment. 
5.   Go back to the Instance List page and click **China \(Hangzhou\)**. The two newly created ECS instances are displayed. Hover the mouse pointer over one instance name and click the displayed pencil icon to change the instance name to ECS01. Then change the other instance name to ECS02. 

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/4105/2204_en-US.png)


