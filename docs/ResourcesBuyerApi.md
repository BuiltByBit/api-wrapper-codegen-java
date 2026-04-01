# ResourcesBuyerApi

All URIs are relative to *https://api.builtbybit.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**getV2ResourcesBuyerLatest**](ResourcesBuyerApi.md#getV2ResourcesBuyerLatest) | **GET** /v2/resources/buyer/latest | Fetches the latest versions &amp; license information |


<a id="getV2ResourcesBuyerLatest"></a>
# **getV2ResourcesBuyerLatest**
> GetV2ResourcesBuyerLatest200Response getV2ResourcesBuyerLatest(nonce)

Fetches the latest versions &amp; license information

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ResourcesBuyerApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.builtbybit.com");
    
    // Configure API key authorization: token
    ApiKeyAuth token = (ApiKeyAuth) defaultClient.getAuthentication("token");
    token.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //token.setApiKeyPrefix("Token");

    ResourcesBuyerApi apiInstance = new ResourcesBuyerApi(defaultClient);
    String nonce = "nonce_example"; // String | 32 character hash provided by an anti-piracy placeholder of the NONCE type. Must be from a resource download (cannot be an addon download’s nonce, etc).
    try {
      GetV2ResourcesBuyerLatest200Response result = apiInstance.getV2ResourcesBuyerLatest(nonce);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ResourcesBuyerApi#getV2ResourcesBuyerLatest");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **nonce** | **String**| 32 character hash provided by an anti-piracy placeholder of the NONCE type. Must be from a resource download (cannot be an addon download’s nonce, etc). | [optional] |

### Return type

[**GetV2ResourcesBuyerLatest200Response**](GetV2ResourcesBuyerLatest200Response.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

