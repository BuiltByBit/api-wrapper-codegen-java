

# License

Supported 'with' hints: - 'Resource': the resource this license is for, if content_type = 'resource' - 'Buyer': the buyer this license is for

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**contentType** | **String** |  |  |
|**contentId** | **Integer** |  |  |
|**buyerId** | **Integer** |  |  [optional] |
|**permanent** | **Boolean** | Whether or not this license is permanent. |  [optional] |
|**active** | **Boolean** | Only respected when permanent &#x3D; &#x60;true&#x60;. |  [optional] |
|**startDate** | **Integer** | Only respected when permanent &#x3D; &#x60;false&#x60;. |  [optional] |
|**endDate** | **Integer** | Only respected when permanent &#x3D; &#x60;false&#x60;. |  [optional] |
|**resource** | [**Resource**](Resource.md) |  |  [optional] |
|**buyer** | [**Member**](Member.md) |  |  [optional] |



