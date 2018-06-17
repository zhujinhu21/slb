# Configure the SLB instance {#task_bh5_dll_vdb .task}

After creating a Server Load Balancer instance, you must add at least one listener and a group of backend servers to it. In this tutorial, we will add one TCP listener and two ECS instances deployed with web pages as the backend servers to the created SLB instance.

1.   Log on to the [SLB](https://partners-intl.console.aliyun.com/#/slb) console. 
2.   On the Instances page, click the ID of the target SLB instance. 

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/4108/2147_en-US.png)

3.  In the left-side navigation pane, click **Listeners** and then click **Add Listener**. 
4.   Configure the listener as follows and use the default settings for other options: 
    -   **Frontend Protocol \[Port\]**: The front-end protocol and port are used to receive and distribute connection requests. The port number of each listener cannot be the same in an SLB instance.

        In this tutorial, select the **TCP** protocol and set the port number to **80**.

    -   **Backend Protocol \[Port\]**: The backend port is the port opened on the backend ECS instances to receive distributed requests. It can be the same in a Server Load Balancer instance.

        In this tutorial, set the backend port number to **80**.

    -   **Peak Bandwidth**: You can set a peak bandwidth to limit the service capabilities that applications on the ECS instances can provide.

        In this tutorial, you do not need to set the peak bandwidth because the instance is billed on traffic.

    -   **Scheduling Algorithm**: Server Load Balancer supports the following scheduling algorithms. In this tutorial, **Round Robin** is selected.

        -   Weighted round robin \(WRR\): You can set a weight for each backend server. Servers with higher weights receive more requests than those with lower weights.
        -   Weighted least connections \(WLC\): In addition to the weight set to each backend ECS server, the number of connections to the client is also considered. A server with a higher weight value will receive a larger percentage of live connections at any one time. If the weights are the same, the system directs network connections to the server with the least number of established connections.
        -   Round robin: Requests are distributed evenly across the group of backend ECS servers sequentially.
        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/4108/2151_en-US.png)

5.   Click **Next Step** to configure health check settings. Select the **TCP** mode and keep other settings as default, and click **Confirm**. 

    Through health check on the backend ECS instances, Server Load Balancer can automatically block abnormal ECS instances and distribute requests to them again when they become normal.

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/4108/2154_en-US.png)

6.   On the Success page, click **Confirm** to complete the configuration. 
7.   In the left-side navigation pane, **Click Servers** \> **Backend servers** . 
8.   On the Load Balancer Server Pool page, click the **Servers Not Added** tab, select the previously created ECS instances, and then click **Add in Batch**. 

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/4108/2159_en-US.png)

9.   In the Add a Backend Server dialog box, use the default weight value and click **Confirm**. 

    A server with a higher weight value receives more requests. The default weight value is 100.

10.  Go back to the Instances page and click **Refresh**. When health check is **Normal**, the corresponding ECS instance can process requests forwarded by the Server Load Balancer instance normally. 

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/4108/2160_en-US.png)

11.  In the web browser, enter the IP address of the Server Load Balancer instance to test the service. 

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/4108/2162_en-US.png)

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/4108/2164_en-US.png)


