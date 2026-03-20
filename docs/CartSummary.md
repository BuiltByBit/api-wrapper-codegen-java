

# CartSummary


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**listPrice** | **BigDecimal** | The combined listed price of all items in the cart (ie. the original prices without any discounts applied). |  |
|**listPriceFormatted** | **String** | The list price formatted as a string using the given currency.  A list price of 5 would be formatted as &#x60;$5.00&#x60;. |  |
|**finalPrice** | **BigDecimal** | The combined final price of all items in the cart (ie. with discounts applied). This is the subtotal the user would pay upon checkout initiation, minus any applicable sales tax. |  |
|**finalPriceFormatted** | **String** | The final price formatted as a string using the given currency.  A final price of 5 would be formatted as &#x60;$5.00&#x60;. |  |
|**currency** | **String** | The currency code (ISO 4217) of the prices in this summary.  Will be USD for all transactions through BuiltByBit. |  |
|**notice** | **String** | A message to display to the user as a notice regarding their current cart items. We may use this to inform the user that they have a previous pending checkout which is yet to be fulfilled (either because the payment is still pending or because they closed out of the checkout). |  [optional] |



