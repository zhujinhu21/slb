# ModifyLoadBalancerPayType {#reference_i4w_xmt_ndb .reference}

将后付费实例转换为预付费实例。

## 请求参数 {#section_cch_pjg_mdb .section}

|名称|类型|是否必须|描述|
|:-|:-|:---|:-|
|Action|String|是|要执行的操作。 取值：ModifyLoadBalancerPayType

|
|RegionId|String|是|负载均衡实例的地域。您可以通过调用DescribeRegions接口查询地域ID。

|
|LoadBalancerId|String|是|负载均衡实例ID。|
|PayType|String|是|负载均衡实例的计费方式。取值：PrePay 

|
|PricingCycle|String|是|计费周期。取值：year | month

|
|Duration|String|是|计费时长。如果PricingCycle为month，取值1-9

如果PricingCycle为year，取值1-3

|
|AutoPay|Boolean|否|是否自动付费。取值：true | false

-   true：自动续费。
-   false（默认值）：不自动续费。

|

## 返回参数 {#section_ugs_f1g_cz .section}

|名称|类型|描述|
|:-|:-|:-|
|RequestId|String|请求ID。|

## 示例 {#section_ix5_h1g_cz .section}

**请求示例**

``` {#public}
https://slb.aliyuncs.com/?Action= ModifyLoadBalancerPayType
&RegionId=cn-hangzhou
&LoadBalancerId=lb-test
&PayType=PrePa
&PricingCycle=Month
&Duration=1
&<公共请求参数>
```

**返回示例**

-   XML格式

    ```
    <?xml version="1.0" encoding="UTF-8"?>
    <ModifyLoadBalancerPayTypeResponse>
      <RequestId>365F4154-92F6-4AE4-92F8-7FF34B540710</RequestId>
    </ModifyLoadBalancerPayTypeResponse>
    ```

-   JSON格式

    ```
    {
      "RequestId":"365F4154-92F6-4AE4-92F8-7FF34B540710",
    }
    ```


