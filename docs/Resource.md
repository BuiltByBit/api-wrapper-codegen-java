

# Resource

Supported 'with' hints: - 'Creator': the resource creator/owner - 'Category': the resource category  - 'Description': the resource description (rendered HTML and BBCode) - 'LatestReviews': list of the 10 latest reviews - 'Filter values': filter values set by the creator

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**resourceId** | **Integer** |  |  [optional] |
|**title** | **String** |  |  [optional] |
|**summary** | **String** |  |  [optional] |
|**url** | **String** |  |  [optional] |
|**creatorId** | **Integer** |  |  [optional] |
|**publishedAt** | **Integer** |  |  [optional] |
|**lastUpdatedAt** | **Integer** |  |  [optional] |
|**purchases** | **Integer** |  |  [optional] |
|**downloads** | **Integer** |  |  [optional] |
|**coverImageUrl** | **String** |  |  [optional] |
|**carouselImageUrls** | **List&lt;String&gt;** |  |  [optional] |
|**reviewCount** | **Integer** |  |  [optional] |
|**reviewAverage** | **BigDecimal** |  |  [optional] |
|**listPrice** | [**Price**](Price.md) |  |  [optional] |
|**finalPrice** | [**Price**](Price.md) |  |  [optional] |
|**saleEventEntry** | [**SaleEventEntry**](SaleEventEntry.md) |  |  [optional] |
|**creator** | [**Member**](Member.md) |  |  [optional] |
|**latestVersion** | [**Version**](Version.md) |  |  [optional] |
|**latestUpdate** | [**Version**](Version.md) |  |  [optional] |
|**latestReviews** | [**List&lt;Review&gt;**](Review.md) |  |  [optional] |
|**description** | [**RichText**](RichText.md) |  |  [optional] |
|**category** | [**Category**](Category.md) |  |  [optional] |
|**addons** | **Map&lt;String, List&lt;Addon&gt;&gt;** |  |  [optional] |



