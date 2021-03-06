# saveWorkFlow


## Description
Save the workflow information

## Request method
POST

## Request address
https://idata-jmr-api.jcloud.com/v1/regions/{regionId}/workflow:save

|Name|Type|Required or not|Default value|Description|
|---|---|---|---|---|
|**regionId**|String|True||Region ID|

## Request parameter
|Name|Type|Required or not|Default value|Description|
|---|---|---|---|---|
|**workflow**|[EmrWorkflow](##EmrWorkflow)|True|||

### <a name="EmrWorkflow">EmrWorkflow</a>
|Name|Type|Required or not|Default value|Description|
|---|---|---|---|---|
|**createTime**|String|False||Workflow creation time|
|**dataCenter**|String|False||Data center, i.e. regionId|
|**id**|Number|False|||
|**isSelfDependence**|Boolean|False||"Whether it is self-dependent"<br>"1: Self-dependent (default), 0: Non-dependent"<br>|
|**isSendMsg**|Boolean|False||Whether to send a notice after failed|
|**modifyTime**|String|False||Last time of modification|
|**status**|String|False||Workflow status|
|**taskScheduleType**|Integer|False||"0: Real-time Task (default)"<br>"1: Periodic Task"<br>"2: Regular Task"<br>|
|**userpin**|String|False||User name|
|**workflowId**|String|False||Workflow ID|
|**workflowName**|String|False||Workflow name|

## Return parameter
|Name|Type|Description|
|---|---|---|
|**requestId**|String||
|**result**|[Result](##Result)||


### <a name="Result">Result</a>
|Name|Type|Description|
|---|---|---|
|**data**|[Message](##Message)||
|**message**|String||
|**status**|String||
### <a name="Message">Message</a>
|Name|Type|Description|
|---|---|---|
|**code**|String|Code|
|**data**|Object|Data|
|**instanceId**|String||
|**jobId**|String|Job ID|
|**path**|[Path[]](##Path)||
|**pipeline**|String||
|**rect**|[Rect[]](##Rect)||
|**result**|String|Result|
|**source**|String||
|**sourceParameterList**|String[]||
|**target**|String||
|**targetParameterList**|String[]||
|**taskId**|String||
|**total**|Integer||
### <a name="Path">Path</a>
|Name|Type|Description|
|---|---|---|
|**child**|Integer||
|**father**|Integer||
### <a name="Rect">Rect</a>
|Name|Type|Description|
|---|---|---|
|**instanceId**|Integer||
|**instanceStatus**|Integer||
|**intervalTimes**|Integer|Re-running interval of the failed task|
|**jobId**|Integer||
|**retryTimes**|Integer|Retry times after the task is failed|
|**taskDesc**|String||
|**taskId**|String||
|**taskName**|String||
|**taskType**|String||
|**x**|Number||
|**y**|Number||

## Return code
|Return code|Description|
|---|---|
|**200**|OK|
|**500**|Internal server error|
