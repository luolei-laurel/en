# describeImportFiles


## Description
Obtain the list of files uploaded by the user to the instance through cloud on single database<br>- only support SQL Server

## Request method
GET

## Request address
https://rds.jdcloud-api.com/v1/regions/{regionId}/instances/{instanceId}/importFiles

|Name|Type|Required or not|Default value|Description|
|---|---|---|---|---|
|**instanceId**|String|True||RDS instance ID, which uniquely identifies an RDS instance|
|**regionId**|String|True||Region code, with range detailed in [Regions and Availability Zone Comparison Table](../Enum-Definitions/Regions-AZ.md)|

## Request parameter
无


## Return parameter
|Name|Type|Description|
|---|---|---|
|**result**|[Result](##Result)||


### <a name="Result">Result</a>
|Name|Type|Description|
|---|---|---|
|**importFiles**|[ImportFile[]](##ImportFile)|Collection of Imported Files|
### <a name="ImportFile">ImportFile</a>
|Name|Type|Description|
|---|---|---|
|**isLocal**|String|Whether it belongs to the current instance. <br> 1: Current instance; <br>0: It does not belong to current instance, and is a shared file|
|**name**|String|File Name|
|**sharedFileGid**|String|If the file is a shared file, it has a global ID, and it is empty if it is not a shared file. This global ID is needed when the file is deleted.|
|**sizeByte**|Integer|File Size, in Byte|
|**uploadTime**|String|File upload completion time, format: YYYY-MM-DD HH:mm:ss|

## Return code
|Return code|Description|
|---|---|
|**200**|OK|
