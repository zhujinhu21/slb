# DescribeVServerGroups {#reference_fy2_gvd_ddd .reference}

查询已创建的服务器组。

## 请求参数 {#section_v5w_nds_cz .section}

|名称|类型|是否必须|描述|
|:-|:-|:---|:-|
|Action|String|是|要执行的操作，取值：DescribeVServerGroups

|
|RegionId|String|是|负载均衡实例的地域ID。您可以通过调用 DescribeRegions接口获取地域ID。

|
|LoadBalancerId|String|是|负载均衡实例ID。|

## 返回参数 {#section_ssd_pds_cz .section}

|名称|类型|描述|
|:-|:-|:-|
|RequestId|String|请求ID。|
|VServerGroupId|String|服务器组ID。|
|VServerGroupName|String|服务器组名称。|
|BackendServers|List|后端服务器列表。|

|名称|类型|描述|
|:-|:-|:-|
|ServerId|String|ECS实例ID。|
|Port|Integer|后端服务器使用的端口。|
|Weight|Integer|后端服务器的权重。|
|Type|String|后端服务器类型：-   ecs：ECS实例（默认）
-   eni

|

## 示例 {#section_oxr_pds_cz .section}

**请求示例**

``` {#public}
https://slb.aliyuncs.com/?Action=DescribeVServerGroups
&RegionId=cn-hangzhou
&LoadBalancerId=lb-bp1yii0s312x83r3qpzke
&公共请求参数
```

**返回示例**

-   XML格式

    ```
    <?xml version="1.0" encoding="UTF-8" ?>
    	<VServerGroups>
    		<VServerGroup>
    			<VServerGroupId>rsp-bp1sqix4iuqyh</VServerGroupId>
    			<VServerGroupName>test1</VServerGroupName>
    			<AssociatedObjects>
    				<Listeners></Listeners>
    				<Rules></Rules>
    			</AssociatedObjects>
    		</VServerGroup>
    		<VServerGroup>
    			<VServerGroupId>rsp-bp1lv0r48xse4</VServerGroupId>
    			<VServerGroupName>test2</VServerGroupName>
    			<AssociatedObjects>
    				<Listeners></Listeners>
    				<Rules></Rules>
    			</AssociatedObjects>
    		</VServerGroup>
    	</VServerGroups>
    	<RequestId>B1B0F537-3F58-469F-8707-10CA36A17142</RequestId>
    ```

-   JSON格式

    ```
    {
        "VServerGroups": {
            "VServerGroup": [
                {
                    "VServerGroupId": "rsp-bp1sqix4iuqyh", 
                    "VServerGroupName": "test1", 
                    "AssociatedObjects": {
                        "Listeners": {
                            "Listener": [ ]
                        }, 
                        "Rules": {
                            "Rule": [ ]
                        }
                    }
                }, 
                {
                    "VServerGroupId": "rsp-bp1lv0r48xse4", 
                    "VServerGroupName": "test2", 
                    "AssociatedObjects": {
                        "Listeners": {
                            "Listener": [ ]
                        }, 
                        "Rules": {
                            "Rule": [ ]
                        }
                    }
                }
            ]
        }, 
        "RequestId": "B1B0F537-3F58-469F-8707-10CA36A17142"
    }
    ```


