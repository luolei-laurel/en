# describeDisks


## Description
-   filters, between multiple filter conditions is logic AND, and multiple values ​​inside each condition is logic OR


## Request method
GET

## Request address
https://disk.jdcloud-api.com/v1/regions/{regionId}/disks

|Name|Type|Required or not|Default value|Description|
|---|---|---|---|---|
|**regionId**|String|True||Region ID|

## Request parameter
|Name|Type|Required or not|Default value|Description|
|---|---|---|---|---|
|**filters**|[Filter[]](##Filter)|False||diskId - cloud disk service ID, accurate match, support multiple<br>diskType - type of cloud disk service, accurate match, support multiple, ssd or premium-hdd<br>instanceId - ID of the machine, to which the cloud disk service is attached, accurate match, support multiple<br>instanceType - Type of the machine, to which the cloud disk service is attached, accurate match, support multiple<br>status - availability zone, accurate match, support multiple<br>az - status of cloud disk service, accurate match, support multiple<br>name - name of cloud disk service, fuzzy match, support single<br>multiAttach - whether the cloud disk service is multi-point attached, accurate match, support single<br>|
|**pageNumber**|Integer|False|1|Page number, defaults is 1; value range: [1, ∞)|
|**pageSize**|Integer|False|20|Page size, default is 20; value range: [10,100]|
|**tags**|[TagFilter[]](##TagFilter)|False||Tag filter condition|

### <a name="Filter">Filter</a>
|Name|Type|Required or not|Default value|Description|
|---|---|---|---|---|
|**name**|String|True||Name of filter requirements|
|**operator**|String|False||Operator of filter requirements is eq by default|
|**values**|String[]|True||Value of filter requirements|
### <a name="TagFilter">TagFilter</a>
|Name|Type|Required or not|Default value|Description|
|---|---|---|---|---|
|**key**|String|True||Tag Key|
|**values**|String[]|True||Tag Value|

## Return parameter
|Name|Type|Description|
|---|---|---|
|**requestId**|String|Request ID|
|**result**|[Result](##Result)|Query Result Set|


### <a name="Result">Result</a>
|Name|Type|Description|
|---|---|---|
|**disks**|[Disk[]](##Disk)|List of cloud disk service information details queried|
|**totalCount**|Integer|Number of cloud disk services queried|
### <a name="Disk">Disk</a>
|Name|Type|Description|
|---|---|---|
|**attachments**|[DiskAttachment[]](##DiskAttachment)|Attach Information|
|**az**|String|AZ, to which the cloud disk service belongs|
|**charge**|[Charge](##Charge)|Configuration information for cloud disk service billing|
|**createTime**|String|Cloud disk service creating time|
|**description**|String|Description of the cloud disk service. It allows you to enter all characters under UTF-8 encoding, but no more than 256 characters.|
|**diskId**|String|Cloud Disk Service ID|
|**diskSizeGB**|Integer|Disk size, in GiB|
|**diskType**|String|Disk type, ssd or premium-hdd|
|**multiAttachable**|Boolean|Does the cloud disk support multiple attachments?|
|**name**|String|Name of the cloud disk service. Only Chinese, numbers, uppercase and lowercase letters, English underline "_" and line-through "-" are allowed. It is not allowed to be blank and shall not exceed 32 characters.|
|**snapshotId**|String|Snapshot ID used to create the cloud disk service|
|**status**|String|Status of the cloud disk service, creating, available, in-use, extending, restoring, deleting, deleted, error_create, error_delete, error_restore or error_extend|
|**tags**|[Tag[]](##Tag)|Tag information|
### <a name="DiskAttachment">DiskAttachment</a>
|Name|Type|Description|
|---|---|---|
|**attachTime**|String|Attaching Time|
|**attachmentId**|String|Attach ID|
|**diskId**|String|Cloud Disk Service ID|
|**instanceId**|String|ID of instance attached|
|**instanceType**|String|Type of the instance  attached, vm or nc|
|**status**|String|Attaching state, "attaching", "attached", "detaching" or "detached"|
### <a name="Charge">Charge</a>
|Name|Type|Description|
|---|---|---|
|**chargeExpiredTime**|String|Expiration time, i.e. the expiration time of Pay-In-Advance resource, which shall be subject to ISO8601, with the UTC time used in the format of YYYY-MM-DDTHH:mm:ssZ. Pay-As-You-Go resource field is blank.|
|**chargeMode**|String|Payment model, the value shall be prepaid_by_duration, postpaid_by_usage or postpaid_by_duration; prepaid_by_duration refers to Pay-In-Advance; postpaid_by_usage refers to Pay By Consumption and Pay-As-You-Go; postpaid_by_duration refers to Pay By Configuration and Pay-As-You-Go, and is postpaid_by_duration by default|
|**chargeRetireTime**|String|The expected release time refers to the expected release time of resources. This value is both available for the Pay-In-Advance/Pay-As-You-Go resources, conforming to the ISO8601 standard, with the UTC time used in the format of YYYY-MM-DDTHH:mm:ssZ|
|**chargeStartTime**|String|The start time of the billing shall be subject to ISO8601, with the UTC time used in the format of YYYY-MM-DDTHH:mm:ssZ|
|**chargeStatus**|String|Cost payment status, the value is respectively normal, overdue and arrear.|
### <a name="Tag">Tag</a>
|Name|Type|Description|
|---|---|---|
|**key**|String|Tag Key|
|**value**|String|Tag Value|

## Return code
|Return code|Description|
|---|---|
|**200**|OK|
|**400**|Invalid parameter|
|**500**|Internal server error|
|**401**|Authentication failed|
|**503**|Service unavailable|
