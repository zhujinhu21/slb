# CreateDomainExtension {#reference_mpx_bvf_j2b .reference}

创建扩展域名。

## 请求参数 {#section_rm1_bcg_j2b .section}

|名称|类型|是否必选|描述|
|:-|:-|:---|:-|
|Action|String|是| 要执行的操作，取值：

 CreateDomainExtension

 |
|RegionId|String|是|负载均衡实例的地域ID。|
|LoadBalancerId|String|是|负载均衡实例的ID。|
|ListenerPort|Integer|是| 负载均衡实例HTTS监听的前端端口，取值：

 1-65535

 |
|Domain|String|是|域名。|
|ServerCertificateId|String|是|与域名对应的证书ID。|

## 返回参数 {#section_xq3_scg_j2b .section}

|名称|类型|描述|
|--|--|--|
|RequestId|String|请求ID。|
|ListenerPort|Integer|负载均衡实例前端使用的端口。|
|DomainExtensionId|String|创建的扩展域名ID。|

## 示例 {#section_oxr_pds_cz .section}

**请求示例**

``` {#public}
https://slb.aliyuncs.com/?Action=CreateDomainExtension
&RegionId=cn-hangzhou
&LoadBalancerId=lb-t4nj5vuz8ish9emfk1f20
&ListenerPort=443
&Domain=*.example2.com
&ServerCertificateId=1231579085529123_164b57543a9_464232488_760347667
&公共请求参数
```

**返回示例**

-   XML格式

    ```
    <?xml version="1.0" encoding="UTF-8" ?>
    <CreateDomainExtensionResponse>
    	<RequestId>149A2470-F010-4437-BF68-343D5099C19D</RequestId>
    	<DomainExtensionId>de-bp1k4chwdnhxd</DomainExtensionId>
    	<ListenerPort>443</ListenerPort>
    </CreateDomainExtensionResponse>
    ```

-   JSON格式

    ```
    {
        "RequestId": "149A2470-F010-4437-BF68-343D5099C19D", 
        "DomainExtensionId": "de-bp1k4chwdnhxd", 
        "ListenerPort": 443
    }
    ```


