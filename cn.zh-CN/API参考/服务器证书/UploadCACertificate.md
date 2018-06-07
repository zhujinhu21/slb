# UploadCACertificate {#reference_lpx_l1f_ndb .reference}

上传CA证书。

一次只能上传一份CA证书内容。添加成功后，返回该用户的该证书的ID、名称和指纹。

## 请求参数 {#section_bqw_c1g_cz .section}

|名称|类型|是否必须|描述|
|:-|:-|:---|:-|
|Action|String|是|要执行的操作，取值：UploadCACertificate

|
|RegionId|String|是|负载均衡实例的地域。您可以通过调用 DescribeRegions接口获取地域ID。

|
|CACertificate|String|是|要上传CA证书的内容。|
|CACertificateName|String|否|CA证书名称。|
|ResourceGroupId|String|否|企业资源组ID。|

## 返回参数 {#section_ugs_f1g_cz .section}

|名称|类型|描述|
|:-|:-|:-|
|RequestId|String|请求ID。|
|CACertificateId|String|CA证书ID。|
|CACertificateName|String|CA证书名称。|
|Fingerprint|String|CA证书的指纹。|
|CreateTime|String|CA证书上传的时间。|
|Fingerprint|Long|CA证书上传的时间戳。|

## 示例 {#section_ix5_h1g_cz .section}

**请求示例**

``` {#public}
https://slb.aliyuncs.com/?Action=UploadCACertificate
&RegionId=cn-east-hangzhou-01
&CACertificate=test
&CACertificateName=mycacert01
&公共请求参数
```

**返回示例**

-   XML格式

    ```
    <?xml version="1.0" encoding="UTF-8"?>
    <UploadCACertificateResponse>
    	<RequestId>365F4154-92F6-4AE4-92F8-7FF34B540710</RequestId>
    	<CACertificateId>idkp-234-cn-test-02</CACertificateId>
    	<CACertificateName>mycacert01</CACertificateName>
    	<Fingerprint>02:DF:AB:ED</Fingerprint>
    </UploadCACertificateResponse>
    ```

-   JSON格式

    ```
    {
      "RequestId":"365F4154-92F6-4AE4-92F8-7FF34B540710",
      "CACertificateId":"idkp-234-cn-test-02",
      "CACertificateName":"mycacert01",
      "Fingerprint":"02:DF:AB:ED"
    }
    ```


