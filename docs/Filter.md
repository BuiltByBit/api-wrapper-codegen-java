

# Filter


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**filterId** | **String** |  |  |
|**order** | **Integer** | The display order of this filter. Filters on BuiltByBit are displayed in ascending order of their order value.  |  |
|**primary** | **Boolean** | Whether or not BuiltByBit considers this a primary filter. Primary filters are displayed more prominently. |  |
|**title** | **String** |  |  |
|**type** | **String** | Supported types:    &#39;choice&#39;: a finite choice set (see &#x60;options&#x60;).    &#39;text&#39;: user text input |  |
|**choices** | [**List&lt;FilterChoice&gt;**](FilterChoice.md) |  |  [optional] |
|**queryField** | **String** |  |  [optional] |
|**value** | **String** | The pass-through value of this filter, only applicable where type &#x3D; &#x60;text&#x60;. |  [optional] |



