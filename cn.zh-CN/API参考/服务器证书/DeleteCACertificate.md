# DeleteCACertificate {#reference_wtr_v1f_ndb .reference}

删除CA证书。

**说明：** 如果指定删除的证书被引用，则无法删除。

## 请求参数 {#section_bqw_c1g_cz .section}

|名称|类型|是否必须|描述|
|:-|:-|:---|:-|
|Action|String|是|要执行的操作，取值：DeleteCACertificate

|
|RegionId|String|是|CA证书的地域。您可以通过调用 DescribeRegions接口获取地域ID。

|
|CACertificateId|String|是|要删除的CA证书ID。|

## 返回参数 {#section_ugs_f1g_cz .section}

|参数|类型|说明|
|:-|:-|:-|
|RequestId|String|请求ID。|

## 示例 {#section_ix5_h1g_cz .section}

**请求示例**

``` {#public}
https://slb.aliyuncs.com/?Action=DeleteCACertificate
&RegionId=cn-hangzhou
&CACertificateId=idkp-234-cn-test-02
&公共请求参数
```

**返回示例**

-   XML格式

    ```
    <?xml version="1.0" encoding="UTF-8"?>
    <DeleteCACertificateResponse>
    	<RequestId>CEF72CEB-54B6-4AE8-B225-F876FF7BA984</RequestId>
    </DeleteCACertificateResponse>
    ```

-   JSON格式

    ```
    {
      "RequestId": " CEF72CEB-54B6-4AE8-B225-F876FF7BA984"
    }
    ```


