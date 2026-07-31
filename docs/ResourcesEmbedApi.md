# ResourcesEmbedApi

All URIs are relative to *https://api.builtbybit.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**getV2ResourcesEmbedDownloadInitiate**](ResourcesEmbedApi.md#getV2ResourcesEmbedDownloadInitiate) | **GET** /v2/resources/embed/download/initiate | Initiate a download request |
| [**getV2ResourcesEmbedDownloadStatus**](ResourcesEmbedApi.md#getV2ResourcesEmbedDownloadStatus) | **GET** /v2/resources/embed/download/status | Fetch the status of a download request |
| [**getV2ResourcesEmbedLatest**](ResourcesEmbedApi.md#getV2ResourcesEmbedLatest) | **GET** /v2/resources/embed/latest | Fetches the latest versions &amp; license information |


<a id="getV2ResourcesEmbedDownloadInitiate"></a>
# **getV2ResourcesEmbedDownloadInitiate**
> GetV2ResourcesEmbedDownloadInitiate200Response getV2ResourcesEmbedDownloadInitiate(contentType, contentId, nonce)

Initiate a download request

See: https://builtbybit.com/help/developers/resource-apis/embed/

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ResourcesEmbedApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.builtbybit.com");
    
    // Configure API key authorization: token
    ApiKeyAuth token = (ApiKeyAuth) defaultClient.getAuthentication("token");
    token.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //token.setApiKeyPrefix("Token");

    ResourcesEmbedApi apiInstance = new ResourcesEmbedApi(defaultClient);
    String contentType = "contentType_example"; // String | Either 'resource', 'resource_version', 'api_asset'
    Integer contentId = 56; // Integer | 
    String nonce = "nonce_example"; // String | 32 character hash provided by an anti-piracy placeholder of the NONCE type. Must be from a resource download (cannot be an addon download’s nonce, etc).
    try {
      GetV2ResourcesEmbedDownloadInitiate200Response result = apiInstance.getV2ResourcesEmbedDownloadInitiate(contentType, contentId, nonce);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ResourcesEmbedApi#getV2ResourcesEmbedDownloadInitiate");
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
| **contentType** | **String**| Either &#39;resource&#39;, &#39;resource_version&#39;, &#39;api_asset&#39; | |
| **contentId** | **Integer**|  | |
| **nonce** | **String**| 32 character hash provided by an anti-piracy placeholder of the NONCE type. Must be from a resource download (cannot be an addon download’s nonce, etc). | |

### Return type

[**GetV2ResourcesEmbedDownloadInitiate200Response**](GetV2ResourcesEmbedDownloadInitiate200Response.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="getV2ResourcesEmbedDownloadStatus"></a>
# **getV2ResourcesEmbedDownloadStatus**
> GetV2ResourcesEmbedDownloadStatus200Response getV2ResourcesEmbedDownloadStatus(token)

Fetch the status of a download request

See: https://builtbybit.com/help/developers/resource-apis/embed/

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ResourcesEmbedApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.builtbybit.com");
    
    // Configure API key authorization: token
    ApiKeyAuth token = (ApiKeyAuth) defaultClient.getAuthentication("token");
    token.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //token.setApiKeyPrefix("Token");

    ResourcesEmbedApi apiInstance = new ResourcesEmbedApi(defaultClient);
    String token = "token_example"; // String | The download request token returned from an initiate request.
    try {
      GetV2ResourcesEmbedDownloadStatus200Response result = apiInstance.getV2ResourcesEmbedDownloadStatus(token);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ResourcesEmbedApi#getV2ResourcesEmbedDownloadStatus");
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
| **token** | **String**| The download request token returned from an initiate request. | [optional] |

### Return type

[**GetV2ResourcesEmbedDownloadStatus200Response**](GetV2ResourcesEmbedDownloadStatus200Response.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="getV2ResourcesEmbedLatest"></a>
# **getV2ResourcesEmbedLatest**
> GetV2ResourcesEmbedLatest200Response getV2ResourcesEmbedLatest(nonce)

Fetches the latest versions &amp; license information

See: https://builtbybit.com/help/developers/resource-apis/embed/

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ResourcesEmbedApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.builtbybit.com");
    
    // Configure API key authorization: token
    ApiKeyAuth token = (ApiKeyAuth) defaultClient.getAuthentication("token");
    token.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //token.setApiKeyPrefix("Token");

    ResourcesEmbedApi apiInstance = new ResourcesEmbedApi(defaultClient);
    String nonce = "nonce_example"; // String | 32 character hash provided by an anti-piracy placeholder of the NONCE type. Must be from a resource download (cannot be an addon download’s nonce, etc).
    try {
      GetV2ResourcesEmbedLatest200Response result = apiInstance.getV2ResourcesEmbedLatest(nonce);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ResourcesEmbedApi#getV2ResourcesEmbedLatest");
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

[**GetV2ResourcesEmbedLatest200Response**](GetV2ResourcesEmbedLatest200Response.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

