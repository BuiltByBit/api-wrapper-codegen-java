

# DownloadPlan


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**level** | [**LevelEnum**](#LevelEnum) |  |  |
|**actions** | [**List&lt;DownloadPlanAction&gt;**](DownloadPlanAction.md) |  |  [optional] |
|**notices** | [**List&lt;DownloadPlanNotice&gt;**](DownloadPlanNotice.md) |  |  [optional] |
|**unsupported** | **List&lt;String&gt;** | A list of features which were unsupported (not passed into the &#39;supported&#39; query paramter) which were needed, resulting in the plan level being downgraded to &#39;manual&#39;. |  [optional] |
|**requiresEmptyServer** | **String** | Whether the server files must be empty before exeucting the plan steps. |  [optional] |



## Enum: LevelEnum

| Name | Value |
|---- | -----|
| FULL | &quot;full&quot; |
| PARTIAL | &quot;partial&quot; |
| MANUAL | &quot;manual&quot; |



