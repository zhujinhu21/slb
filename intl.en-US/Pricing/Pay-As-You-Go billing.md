# Pay-As-You-Go billing {#concept_dph_vfs_wdb .concept}

SLB is billed based on traffic usage. 

## Billing items {#section_e22_ggs_wdb .section}

The total fee of an SLB instance is the sum of the billing items. The billing items vary by network type and instance type as shown in the following table. \(√ indicates that the corresponding item is billed. — indicates that the corresponding item is not billed.\)

|Network type|Instance type|Instance fee|Traffic fee|Capacity fee|
|:-----------|:------------|:-----------|:----------|:-----------|
|Internet|Shared-performance instances|√|√|—|
|Guaranteed-performance instances|√|√|√|
|Intranet|Shared-performance instances|—|—|—|
|Guaranteed-performance instances|—|—|√|

## Instance fee {#section_a1f_lgs_wdb .section}

Instance fees are charged for Internet SLB instances to reserve a public IP.

**Note:** Intranet SLB instances are not charged for instance fees.

Instance fees of Internet SLB instances are billed as follows:

-   Instance fee = instance price \(USD/Hour\) x instance reservation time

    The reservation time is the period from the time the instance is created to the time the instance is released.

-   Instance fees are billed on an hourly basis. Partial hours are billed as full hours.


The price in the following table is only for reference. Take the price on the console as standard.

|Region|Instance fee \(USD/hour\)|
|:-----|:------------------------|
|China \(Hangzhou\)/China \(Beijing\)/China \(Shenzhen\)/ China \(Shanghai\)/China \(Zhangjiakou\)|0.003|
|China \(Qingdao\)|0.003|
|China \(Hong Kong\)|0.009|
|US \(Virginia\) /US \(Silicon Valley\)|0.005|
|Singapore|0.006|
|Japan \(Tokyo\)|0.009|
|EU Central 1 \(Frankfurt\)|0.006|
|UAE \(Dubai\)|0.009|
|Australia \(Sydney\)|0.006|

## Traffic fee {#section_c1f_lgs_wdb .section}

Traffic fees are charged based on the traffic usage of Internet SLB instances.

**Note:** Intranet instances are free of traffic fee.

Traffic fees of Internet SLB instances are billed as follows:

-   Public traffic fee = public network traffic  \(USD/Hour\)  x time

    Public network traffic is the outbound traffic \(downstream\). Inbound traffic \(upstream\) is not included in the cost.

-   Instance fees are billed on an hourly basis. Partial hours are billed as full hours.

    The price in the following table is only for reference. Take the price on the console as standard.

    |Region|Traffic fee \(USD/Gbps\)|
    |:-----|:-----------------------|
    |China \(Hangzhou\)/China \(Beijing\)/China \(Shenzhen\)/China \(Shanghai\)/ China \(Zhangjiakou\)|0.125|
    |China \(Qingdao\)|0.113|
    |China \(Hong Kong\)|0.156|
    |US \(Virginia\) /US \(Silicon Valley\)|0.078|
    |Singapore|0.117|
    |Japan \(Tokyo\)|0.120|
    |EU Central 1 \(Frankfurt\)|0.070|
    |UAE \(Dubai\)|0.447|
    |Australia \(Sydney\)|0.130|


## Capacity fee {#section_l1n_5gs_wdb .section}

Guaranteed-performance instances provide guaranteed performance metrics \(performance SLA\). Different capacities are provided to meet unique business requirements.  The corresponding capacity fee is billed for each guaranteed-performance instance no matter the network type of the instance, and is billed based on the actual usage depending on the capacity selected. If the actual performance metrics of an instance occurs between two capacities, the capacity fee is charged at the higher capacity fee.

For example, if you purchase the slb.s3.large capacity \(1,000,000; CPS 500,000; QPS 50,000\) and the actual usage of your instance in an hour is as follows:

| Max Connection|CPS|QPS|
|:--------------|:--|:--|
|90,000|4,000|11,000|

-   From the perspective of Max Connection, the actual metrics 90,000 occurs between the limit 50,000 defined in the Standard I \(slb.s2.small\) capacity and the limit 100,000 defined in the Standard II \(slb.s2.medium\) capacity. Therefore, the capacity of the Max Connection metrics in this hour is Standard II \(slb.s2.medium\).

-   From the perspective of CPS, the actual metrics 4,000 occurs between the limit 3,000 defined in the Small I \(slb.s1.small\) capacity and the limit 5,000 defined in the Standard I \(slb.s2.small\) capacity. Therefore, the capacity of the CPS metrics in this hour is Standard I \(slb.s2.small\).

-   From the perspective of QPS, the actual metrics 11,000 occurs between the limit 10,000 defined in the Standard II \(slb.s2.medium\) capacity and the limit 20,000 defined in the Higher I \(slb.s3.small\) capacity. Therefore, the capacity of the QPS metrics in this hour is Higher I \(slb.s3.small\).

    Comparing these three metrics, the capacity of the QPS metrics is highest, therefore, the capacity fee of the instance in this hour is charged at the price of the Higher I \(slb.s3.small\) capacity.


The following figure shows how the capacity fee is billed for an SLB instance in the first three hours:

![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/13419/6420_en-US.png)

The billing of the guaranteed-performance instances is flexible.  The performance capacity selected when purchasing an instance is the performance limitation of the SLB instance. For example, if slb.s3.medium is selected, the new connections are dropped when the HTTP requests in one second reach 30,000.

The price in the following table is only for reference. Take the price on the console as standard. Capacity fees of guaranteed-performance instances in the international regions can enjoy an 83% discount.

|Region|Specification| Max Connection|CPS|QPS|Capacity price \(USD/Hour\)|
|:-----|:------------|:--------------|:--|:--|:--------------------------|
| China \(Hangzhou\)

 China \(Zhangjiakou\)

 China \(Hohhot\)

 China \(Qingdao\)

 China \(Beijing\)

 China \(Shanghai\)

 China \(Shenzhen\)

 |Capacity 1: Small I \(slb.s1.small\)|5000|3,000|1000|Free|
|Capacity 2: Standard I \(slb.s2.small\)|50,000|5,000|5,000|0.05|
|Capacity 3: Standard II \(slb.s2.medium\) |100,000|10,000|10,000|0.10|
|Capacity 4: Higher I \(slb.s3.small\)|200,000|20,000|20,000|0.20|
|Capacity 5: Higher II \(slb.s3.medium\)|500,000|50,000|30,000|0.31|
|Capacity 6: Super I \(slb.s3.large\)|1,000,000|100,000|50,000|0.51|
| Singapore

 Malaysia \(Kuala Lumpur\)

 Indonesia \(Jakarta\)

 India \(Mumbai\)

 US \(Silicon Valley\)

 US \(Virginia\)

 China \(Hong Kong\)

 |Capacity 1: Small I \(slb.s1.small\)|5,000|3,000|1,000|Free|
|Capacity 2: Standard I \(slb.s2.small\)|50,000|5,000|5,000|0.06|
|Capacity 3: Standard II \(slb.s2.medium\) |100,000|10,000|10,000|0.12|
|Capacity 4: Higher I \(slb.s3.small\)|200,000|20,000|20,000|0.24|
|Capacity 5: Higher II \(slb.s3.medium\)|500,000|50,000|30,000|0.37|
|Capacity 6: Super I \(slb.s3.large\)|1,000,000|100,000|50,000|0.61|

