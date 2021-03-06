# getDomainQueryTraffic


## Description
View query traffic of domain names

## Request method
GET

## Request address
https://clouddnsservice.jdcloud-api.com/v1/regions/{regionId}/domain/{domainId}/queryTraffic

|Name|Type|Required or not|Default value|Description|
|---|---|---|---|---|
|**domainId**|String|True||Domain Name ID|
|**regionId**|String|True||Region ID to which the instance belongs|

## Request parameter
|Name|Type|Required or not|Default value|Description|
|---|---|---|---|---|
|**domainName**|String|True||Domain Name|
|**end**|String|True||Termination time, UTC time, for example, 2017-11-10T23:00:00Z|
|**start**|String|True||Start time, UTC time, for example, 2017-11-10T23:00:00Z|


## Return parameter
|Name|Type|Description|
|---|---|---|
|**requestId**|String||
|**result**|[Result](##Result)||


### <a name="Result">Result</a>
|Name|Type|Description|
|---|---|---|
|**time**|Integer[]|Time series|
|**traffic**|Number[]|Data series|
|**unit**|String|Unit of data|

## Return code
|Return code|Description|
|---|---|
|**200**|OK|
|**400**|NOT_FOUND|
