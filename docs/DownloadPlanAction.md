

# DownloadPlanAction


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**type** | [**TypeEnum**](#TypeEnum) |  |  |
|**src** | **String** | The source file/directory. |  [optional] |
|**dst** | **String** | A destination file/directory relative to the server root. |  [optional] |
|**actions** | [**List&lt;DownloadPlanAction&gt;**](DownloadPlanAction.md) | A set of subactions to execute in the context of this action. |  [optional] |



## Enum: TypeEnum

| Name | Value |
|---- | -----|
| COPY | &quot;copy&quot; |
| COPY_DIR | &quot;copy_dir&quot; |
| OPEN_ZIP | &quot;open_zip&quot; |
| SERVER_RESTART | &quot;server_restart&quot; |



