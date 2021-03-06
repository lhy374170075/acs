# View a cluster {#reference_tzl_jfd_xdb .reference}

View the cluster details according to the cluster ID.

## Request Information {#section_qwv_kfd_xdb .section}

**Request line \(RequestLine\)**

```
GET /clusters/{cluster_id} HTTP/1.1
```

**Request line parameter \(URI Param\)**

|Name |Parameters|Required|Description |
|:----|:---------|:-------|:-----------|
|cluster\_id|string|Yes.|Custer ID|

**Special request header \(RequestHead\)**

None. See [Public request headers](intl.en-US/Developer Guide/Swarm API reference/Cluster API call mode/Public parameters.md#section_cdv_4nd_xdb).

**Request body requestbody**

None. 

## Returns Information {#section_fhm_rfd_xdb .section}

**Response line \(ResponseLine\)**

```
HTTP/1.1 200 OK
```

**Special response header \(ResponseHead\)**

None. See [Public response headers](intl.en-US/Developer Guide/Swarm API reference/Cluster API call mode/Public parameters.md#section_qdv_4nd_xdb).

**Response body \(ResponseBody\)**

```
{
    "agent_version": "string",
    "Cluster_id": "string ",
    "created": "datetime",
    "external_loadbalancer_id": "string",
    "master_url": "string",
    "name": "string",
    "network_mode": "string",
    "region_id": "string",
    "security_group_id": "string",
    "size": "numbers",
    "state": "string",
    "updated": "datetime",
    "vpc_id": "string",
    "vswitch_id": "string"
}
```

**Response body explanation**

Cluster format

|Name |Type|Description|
|:----|:---|:----------|
|agent\_version|string|The Agent version.|
|cluster\_id|String|The cluster ID, which is the unique identifier of the cluster.|
|created|string|The creation time of the cluster.|
|external\_loadbalancer\_id|String|The Server Load Balancer instance ID of the cluster.|
|master\_url|string|The master address of the cluster, which is used to connect to the cluster to perform operations. For more information, see [Connect to a cluster by using Docker tools](../../../../intl.en-US/Quick Start/Swarm cluster/Connect to a cluster by using Docker tools.md#).|
|name |string|The cluster name, which is specified when you create the cluster and is unique for each account.|
|network\_mode|String|The network mode of the cluster \(Classic or Virtual Private Cloud \(VPC\)\).|
|region\_id|String|The ID of the region where the cluster is located.|
|security\_group\_id|String|The security group ID.|
|size|String|The number of nodes.|
|state|String|The cluster status. For more information, see [Cluster lifecycle](../../../../intl.en-US/User Guide/Swarm cluster/Clusters/Cluster lifecycle.md#).|
|updated|string|The last update time.|
|vpc\_id|string|The VPC ID.|
|vswitch\_id|string|The VSwitch ID.|

## Examples {#section_xmp_fgd_xdb .section}

**Request example**

```
GET /clusters/C5b5e80b0b64a4bf6939d2d8fbbc5ded7 HTTP/1.1
<Public request header>
```

**Response example**

```
HTTP/1.1 200 OK
<Public response headers>
{
    "agent_version": "0.5-e56dab3",
    "cluster_id": "c978ca3eaacd3409a9437db07598f1f69",
    "created": "2015-12-11T03:52:40Z",
    "external_loadbalancer_id": "1518f2b7e4c-cn-beijing-btc-a01",
    "master_url": "https://182.92.245.56:17589",
    "name": "my-python-cluster-039de960",
    "network_mode": "classic",
    "region_id": "cn-beijing",
    "security_group_id": "sg-25yqjuxhz",
    "size": 5,
    "state": "running",
    "updated": "2015-12-15T15:01:58Z",
    "vpc_id": "",
    "vswitch_id": ""
}
```

