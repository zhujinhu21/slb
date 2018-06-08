# API概览 {#concept_qyw_x1d_cz .concept}

## 实例API {#section_rpm_m2w_pdb .section}

|API|描述|
|:--|:-|
|CreateLoadBalancer|创建负载均衡实例。|
|ModifyLoadBalancerInternetSpec|修改负载均衡实例的计费方式或规格。|
|DeleteLoadBalancer|删除负载均衡实例。|
|SetLoadBalancerStatus|设置负载均衡实例的状态。|
|SetLoadBalancerName|修改负载均衡实例的名称。|
|DescribeLoadBalancers|查询已创建的负载均衡实例。|
|DescribeLoadBalancerAttribute|查询指定负载均衡实例的详细信息。|
|ModifyLoadBalancerPayType|将后付费实例转换为预付费实例。|
|ModifyLoadBalancerInstanceSpec|修改负载均衡实例的规格。|
|DescribeRegions|查询可用地域。|
|DescribeZones|查询指定地域的可用区信息。|

## 监听API {#section_dc5_gfw_pdb .section}

|API|描述|
|:--|:-|
|**TCP监听**|
|CreateLoadBalancerTCPListener|创建TCP监听。|
|SetLoadBalancerTCPListenerAttribute|修改TPC监听的配置。|
|DescribeLoadBalancerTCPListenerAttribute|查询TCP监听配置。|
|**UDP监听**|
|CreateLoadBalancerUDPListener|创建UDP监听。|
|SetLoadBalancerUDPListenerAttribute|修改UDP监听的配置。|
|DescribeLoadBalancerUDPListenerAttribute|查询UDP监听配置。|
|**HTTP监听**|
|CreateLoadBalancerHTTPListener|创建HTTP监听。|
|SetLoadBalancerHTTPListenerAttribute|修改HTTP监听的配置。|
|DescribeLoadBalancerHTTPListenerAttribute|查询HTTP监听配置。|
|**HTTPS监听**|
|CreateLoadBalancerHTTPSListener|创建HTTPS监听。|
|SetLoadBalancerHTTPSListenerAttribute|修改HTTPS监听的配置。|
|DescribeLoadBalancerHTTPSListenerAttribute|查询HTTPS监听配置。|
|StartLoadBalancerListener|启动监听。|
|DeleteLoadBalancerListener|删除监听。|
|StopLoadBalancerListener|停止监听。|
|**访问控制**|
|SetListenerAccessControlStatus|为指定监听开启或关闭访问控制功能。|
|DescribeListenerAccessControlAttribute|查询监听的访问控制配置。|
|AddListenerWhiteListItem|添加监听访问控制白名单。|
|RemoveListenerWhiteListItem|删除监听白名单中的IP地址。|
|**转发策略**|
|CreateRules|为指定的HTTP/HTTPS监听添加转发规则。|
|DeleteRules|删除转发规则。|
|SetRule|更改转发规则的目标服务器组。|
|DescribeRules|查询指定监听已配置的转发规则。|
|DescribeRuleAttribute|查询指定转发规则的配置详情。|

## 后端服务器API {#section_vpc_kff_cz .section}

|API|描述|
|:--|:-|
|AddBackendServers|添加后端服务器。|
|RemoveBackendServers|移除后端服务器。|
|SetBackendServers|设置后端服务器权重。|
|DescribeHealthStatus|负载均衡实例的后端服务器进行健康检查，返回后端服务器的健康状况。|
|**虚拟服务器组**|
|CreateVServerGroup|创建虚拟服务器组，并添加后端服务器。|
|SetVServerGroupAttribute|修改虚拟服务器组的配置。|
|AddVServerGroupBackendServers|为指定的后端服务器组添加后端服务器。|
|RemoveVServerGroupBackendServers|从指定的后端服务器组中移除后端服务器。|
|ModifyVServerGroupBackendServers|替换服务器组中的后端服务器。|
|DeleteVServerGroup|删除服务器组。|
|DescribeVServerGroups|查询已创建的服务器组。|
|DescribeVServerGroupAttribute|查询服务器组的详细信息。|
|**主备服务器组**|
|CreateMasterSlaveServerGroup|创建主备服务器组。|
|DeleteMasterSlaveServerGroup|删除主备服务器组。|
|DescribeMasterSlaveServerGroupAttribute|查询指定主备服务器组的详细信息。|
|DescribeMasterSlaveServerGroups|查询已创建的主备服务器组。|

## 访问控制API {#section_evr_pcy_5db .section}

|API|描述|
|:--|:-|
|CreateAccessControlList|创建访问控制策略组。|
|DeleteAccessControlList|删除访问控制策略组。|
|DescribeAccessControlLists|查询已创建的访问控制策略组。|
|DescribeAccessControlListAttribute|查询访问控制策略组的配置。|
|SetAccessControlListAttribute|修改访问控制策略组的名称。|
|AddAccessControlListEntry|在访问控制策略组中添加IP条目。|
|RemoveAccessControlListEntry|删除访问控制策略组中的IP条目。|

## 标签API {#section_w4z_lff_cz .section}

|API|描述|
|:--|:-|
|AddTags|为指定的负载均衡实例添加标签。|
|DescribeTags|查询已创建的标签。|
|RemoveTags|解绑负载均衡实例的标签。|

