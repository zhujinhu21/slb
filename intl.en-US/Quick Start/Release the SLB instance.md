# Release the SLB instance {#task_bh5_dll_vdb .task}

When you no longer need Server Load Balancer, release the corresponding instance to avoid additional charges. Releasing the Server Load Balancer instance does not delete or affect backend ECS instances.

**Note:** 

-   If you have resolved a domain name to a SLB service address, resolve it to another SLB service address first to avoid service interruption.
-   Only the Pay-As-You-Go instances can be released. The Subscription instances are automatically released when the instance is overdue after 15 days.
-   The backend ECS instance is still running after an SLB instance is released. You can release the backend ECS instances if you do not need them anymore.

1.   Log on to the [SLB console](https://slbnew.console.aliyun.com/#/list/cn-hangzhou). 
2.   On the Instances page, select the region where the instance is located. 
3.   Find the target instance and click **Release**. 
4.   In the Release dialog box, select **Release Now** or **Timed Release**. 

    If you select **Timed Release**, select the release date and release time.

5.   Click **Next** and then click **Confirm** to release the Server Load Balancer instance. 

