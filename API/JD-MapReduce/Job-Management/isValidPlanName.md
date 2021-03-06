# isValidPlanName


## Description
Verify whether the execution plan name is available

## Request method
POST

## Request address
https://idata-jmr-api.jcloud.com/v1/regions/{regionId}/planName:valid

|Name|Type|Required or not|Default value|Description|
|---|---|---|---|---|
|**regionId**|String|True||Region ID|

## Request parameter
|Name|Type|Required or not|Default value|Description|
|---|---|---|---|---|
|**planId**|String|True||It is considered as the verification basis|
|**planName**|String|True||Verified plan name|


## Return parameter
|Name|Type|Description|
|---|---|---|
|**requestId**|String||
|**result**|[Result](##Result)||


### <a name="Result">Result</a>
|Name|Type|Description|
|---|---|---|
|**message**|String||
|**status**|String||

## Return code
|Return code|Description|
|---|---|
|**200**|OK|
|**500**|Internal server error|
