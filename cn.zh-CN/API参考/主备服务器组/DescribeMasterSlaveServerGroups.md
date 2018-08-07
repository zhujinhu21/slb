# DescribeMasterSlaveServerGroups {#reference_jn1_kzd_ndb .reference}

查询已创建的主备服务器组。

## 请求参数 {#section_v5w_nds_cz .section}

|名称|类型|是否必须|描述|
|:-|:-|:---|:-|
|Action|String|是|要执行的操作，取值：DescribeMasterSlaveServerGroups

|
|RegionId|String|是|负载均衡地域。您可以通过调用 DescribeRegions接口获取地域ID。

|
|LoadBalancerId|String|是|负载均衡实例ID。|

## 返回参数 {#section_ssd_pds_cz .section}

|名称|类型|描述|
|:-|:-|:-|
|RequestId|String|请求ID。|
|MasterSlaveServerGroupId|String|主备服务器组ID。|
|MasterSlaveServerGroupName|String|主备服务器组名称。|
|MasterSlaveBackendServers|StringJSON格式的List

|主备服务器组列表。|

|名称|类型|描述|
|:-|:-|:-|
|ServerId|String|ECS实例ID。|
|Port|String|后端服务器使用的端口。取值范围：1-65535

|
|Weight|String| 后端服务器的权重，取值：\[0,100\]

 默认值为100。如果值为0，则不会将请求转发给该后端服务器。

 |
|ServerType|String|服务器类型，取值：Master（默认值） | Slave

|

## 示例 {#section_oxr_pds_cz .section}

**请求示例**

``` {#public}
https://slb.aliyuncs.com/?Action=DescribeMasterSlaveServerGroups
&RegionId=cn-hangzhou
&LoadBalancerId=lb-t4nj5vuz8ish9emfk1f20
&公共请求参数
```

**返回示例**

-   XML格式

    ```
    <?xml version="1.0" encoding="utf-8"?>
    <DescribeMasterSlaveServerGroupsResponse>
        <RequestId>2631BB5E-B576-4925-BDED-07A66D23E5DE</RequestId>
        <MasterSlaveServerGroups>
    	<MasterSlaveServerGroup>
    		<MasterSlaveServerGroupId>rsp-bp1ro3mwp2x2m</MasterSlaveServerGroupId>
    		<MasterSlaveServerGroupName>test</MasterSlaveServerGroupName>
    	</MasterSlaveServerGroup>
        </MasterSlaveServerGroups>
    </DescribeMasterSlaveServerGroupsResponse>
    ```

-   JSON格式

    ```
    {
      "RequestId": "2631BB5E-B576-4925-BDED-07A66D23E5DE",
      "MasterSlaveServerGroups": {
        "MasterSlaveServerGroup": [
          {
            "MasterSlaveServerGroupId": "rsp-bp1ro3mwp2x2m",
            "MasterSlaveServerGroupName": "test"
          }
        ]
      }
    }
    ```


