# DescribeCACertificates {#reference_h4p_lbf_ndb .reference}

查询已上传的CA证书。

**说明：** 为了保证证书安全，只返回证书的指纹和名称，不返回证书内容。

## 请求参数 {#section_bqw_c1g_cz .section}

|名称|类型|是否必须|描述|
|:-|:-|:---|:-|
|Action|String|是|要执行的操作，取值：DescribeCACertificates

|
|RegionId|String|是|负载均衡实例的地域。您可以通过调用 DescribeRegions接口获取地域ID。

|
|CACertificateId|String|否|CA证书ID。|
|ResourceGroupId|String|否|企业资源组ID。|

## 返回参数 {#section_ugs_f1g_cz .section}

|名称|类型|说明|
|:-|:-|:-|
|RequestId|String|请求ID。|
|CACertificates|List|CA证书列表。|

|名称|类型|说明|
|:-|:-|:-|
|CACertificateId|String|CA证书ID。|
|CACertificateName|String|CA证书名称。|
|RegionId|String|CA证书地域。|
|Fingerprint|String|CA证书的指纹。|
|CreateTimeStamp|Long|CA证书上传的时间戳。|

## 示例 {#section_ix5_h1g_cz .section}

**请求示例**

``` {#public}
https://slb.aliyuncs.com/?Action=DescribeCACertificates
&RegionId=cn-hangzhou
&公共请求参数
```

**返回示例**

-   XML格式

    ```
    <?xml version="1.0" encoding="UTF-8"?>
    <DescribeCACertificatesResponse>
       <RequestId>6DFA147D-EE7E-4FE2-831A-9FAC41C52AFA</RequestId>
       <CACertificates>
          <CACertificate>
                <CACertificateId>1231579085529123_15c73d77203_-986300114_-2110544408</CACertificateId>
                <CACertificateName>CA1</CACertificateName>
                <CreateTime>2017-06-04T16:01:58Z</CreateTime>
                <CreateTimeStamp>1496592118000</CreateTimeStamp>
                <Fingerprint>0d:f6:9e:ed:c2:6d:df:06:ac:af:82:fb:17:1b:5b:08:39:b3:d9:d0</Fingerprint>
                <RegionId>cn-hangzhou</RegionId>
                <ResourceGroupId>rg-acfmxazb4ph6aiy</ResourceGroupId>
             </CACertificate>
       </CACertificates>
    </DescribeCACertificatesResponse>
    ```

-   JSON格式

    ```
    {
       "RequestId":"6DFA147D-EE7E-4FE2-831A-9FAC41C52AFA",
       "CACertificates":{
          "CACertificate":[
             {
                "CreateTimeStamp":1496592118000,
                "CACertificateName":"CA1",
                "CreateTime":"2017-06-04T16:01:58Z",
                "ResourceGroupId":"rg-acfmxazb4ph6aiy",
                "RegionId":"cn-hangzhou",
                "CACertificateId":"1231579085529123_15c73d77203_-986300114_-2110544408",
                "Fingerprint":"0d:f6:9e:ed:c2:6d:df:06:ac:af:82:fb:17:1b:5b:08:39:b3:d9:d0"
             }
          ]
       }
    }
    ```


