

# Purchase

Supported 'with' hints: - 'Buyer': the buyer of the purchase - 'Seller': the seller of the purchase - 'Resource': the resource purchased, if content_type = 'resource' - 'Addon': the addon purchased, if content_type = 'addon'

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**purchaseId** | **Integer** |  |  [optional] |
|**contentType** | **String** |  |  [optional] |
|**contentId** | **Integer** |  |  [optional] |
|**buyerId** | **Integer** |  |  [optional] |
|**sellerId** | **Integer** |  |  [optional] |
|**createdAt** | **Integer** |  |  [optional] |
|**validatedAt** | **Integer** |  |  [optional] |
|**bundleId** | **Integer** |  |  [optional] |
|**saleEventId** | **Integer** |  |  [optional] |
|**externalTid** | **String** |  |  [optional] |
|**gateway** | **String** |  |  [optional] |
|**listPrice** | [**Price**](Price.md) |  |  [optional] |
|**finalPrice** | [**Price**](Price.md) |  |  [optional] |
|**platformFee** | [**Price**](Price.md) |  |  [optional] |
|**adFeePayment** | [**Price**](Price.md) |  |  [optional] |
|**adFeeCredit** | [**Price**](Price.md) |  |  [optional] |
|**resource** | [**Resource**](Resource.md) |  |  [optional] |
|**addon** | [**Addon**](Addon.md) |  |  [optional] |
|**buyer** | [**Member**](Member.md) |  |  [optional] |
|**seller** | [**Member**](Member.md) |  |  [optional] |



