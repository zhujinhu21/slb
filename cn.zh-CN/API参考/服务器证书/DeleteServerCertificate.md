# DeleteServerCertificate {#reference_i2g_sx2_ndb .reference}

删除服务器证书。

**说明：** 如果指定删除的证书被引用，无法删除。

## 请求参数 {#section_bqw_c1g_cz .section}

|名称|类型|是否必须|描述|
|:-|:-|:---|:-|
|Action|String|是|要执行的操作，取值：DeleteServerCertificate

|
|RegionId|String|否|负载均衡实例的地域。您可以通过调用 DescribeRegions接口获取地域ID。

|
|ServerCertificateId|String|是|服务器证书的ID。|

## 返回参数 {#section_ugs_f1g_cz .section}

|名称|类型|说明|
|:-|:-|:-|
|RequestId|String|请求ID。|

## 示例 {#section_ix5_h1g_cz .section}

**请求示例**

``` {#public}
https://slb.aliyuncs.com/?Action=DeleteServerCertificate
&RegionId=cn-hangzhou
&ServerCertificateId=idkp-123-cn-test-01
&公共请求参数
```

**返回示例**

-   XML格式

    ```
    <?xml version="1.0" encoding="UTF-8"?>
    <DeleteServerCertificateResponse>
    	<RequestId>CEF72CEB-54B6-4AE8-B225-F876FF7BA984</RequestId>
    </DeleteServerCertificateResponse>
    ```

-   JSON格式

    ```
    {
         "RequestId":" CEF72CEB-54B6-4AE8-B225-F876FF7BA984"
     }
    ```


