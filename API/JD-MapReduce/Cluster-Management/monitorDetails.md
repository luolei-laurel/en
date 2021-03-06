# monitorDetails


## Description
Detailed data of service survival status monitoring

## Request method
POST

## Request address
https://idata-jmr-api.jcloud.com/v1/regions/{regionId}/monitorDetails

|Name|Type|Required or not|Default value|Description|
|---|---|---|---|---|
|**regionId**|String|True||Region ID|

## Request parameter
|Name|Type|Required or not|Default value|Description|
|---|---|---|---|---|
|**clusterId**|String|True||Cluster ID|
|**service**|String|True||Service name, such as HADOOP|


## Return parameter
|Name|Type|Description|
|---|---|---|
|**requestId**|String||
|**result**|[Result](##Result)||


### <a name="Result">Result</a>
|Name|Type|Description|
|---|---|---|
|**data**|String[]||
|**message**|String||
|**status**|String||

## Return code
|Return code|Description|
|---|---|
|**200**|OK|
|**500**|Internal server error|
