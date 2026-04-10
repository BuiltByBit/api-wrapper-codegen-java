

# PostV2ResourcesCreatorCouponsRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**type** | **String** | Must be &#39;perecent&#39;. |  |
|**discount** | **BigDecimal** |  |  |
|**label** | **String** | The trailing part of the coupon code (without &#39;{user_id}-&#39;). |  |
|**doExpiry** | **Boolean** | Whether or not to respect the &#39;expiry_date&#39; field. No expiry date is set otherwise. |  [optional] |
|**expiryDate** | **String** |  |  [optional] |
|**limitedUses** | **Boolean** | Whether or not to respect the &#39;max_uses&#39; field. No max use limit is set otherwise. |  [optional] |
|**maxUses** | **Integer** |  |  [optional] |
|**limitedUserUses** | **Boolean** | Whether or not to respect the &#39;max_per_user_uses&#39; field. No max uses per user limit is set otherwise. |  [optional] |
|**maxPerUserUses** | **Integer** |  |  [optional] |
|**allContentTypes** | **List&lt;String&gt;** | If a content type is included, all of the creator&#39;s content (of that type) can be used against this coupon.  Support values include: &#39;resource&#39;, &#39;addon&#39;, and &#39;bundle&#39; |  [optional] |
|**resources** | **String** | A comma-separated list of resource IDs which this coupon can be used against. |  [optional] |
|**addons** | **String** | A comma-separated list of addon IDs which this coupon can be used against. |  [optional] |
|**bundles** | **String** | A comma-separated list of bundle IDs which this coupon can be used against. |  [optional] |



