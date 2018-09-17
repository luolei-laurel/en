# deleteInstance


## Description
Delete a single virtual machine that is paid by configuration,  or expires in a monthly package. You cannot delete a virtual machine without billing information. <br>
The virtual machine status must be <b>running<b>,  <b>stopped<b>,  <b>error<b>,  and the virtual machine is not in progress to delete. <br>
The virtual machine that has not expired in monthly package cannot be deleted. The white list user cannot delete the virtual machine that has expired in monthly package. <br>
If the data disk attached in the machine is the cloud disk billed by instance type and is not a shared cloud disk service, and the AutoDelete property is true, then the data disk is deleted along with the machine.
</br>敏感操作，可开启<a href="https://www.jdcloud.com/help/detail/3786/isCatalog/1">MFA操作保护</a>

## Request method
DELETE

## Request address
https://vm.jdcloud-api.com/v1/regions/{regionId}/instances/{instanceId}

|Name|Type|Required or not|Default value|Description|
|---|---|---|---|---|
|**instanceId**|String|True||VM ID|
|**regionId**|String|True||Region ID|

## Request parameter
None


## Return parameter
|Name|Type|Description|
|---|---|---|



## Return code
|Return code|Description|
|---|---|
|**400**|Invalid parameter|
|**401**|Authentication failed|
|**404**|Not found|
|**503**|Service unavailable|
|**200**|OK|
|**500**|Internal server error|