# ResourcesEmbedApi

All URIs are relative to *https://api.builtbybit.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**getV2ResourcesEmbedDownload**](ResourcesEmbedApi.md#getV2ResourcesEmbedDownload) | **GET** /v2/resources/embed/download | Fetch the status of a download request |
| [**getV2ResourcesEmbedLatest**](ResourcesEmbedApi.md#getV2ResourcesEmbedLatest) | **GET** /v2/resources/embed/latest | Fetches the latest versions &amp; license information |
| [**postV2ResourcesEmbedDownload**](ResourcesEmbedApi.md#postV2ResourcesEmbedDownload) | **POST** /v2/resources/embed/download | Submit a new download request |


<a id="getV2ResourcesEmbedDownload"></a>
# **getV2ResourcesEmbedDownload**
> GetV2ResourcesEmbedDownload200Response getV2ResourcesEmbedDownload(token)

Fetch the status of a download request

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
    String token = "token_example"; // String | The token provided when submitting a download request.
    try {
      GetV2ResourcesEmbedDownload200Response result = apiInstance.getV2ResourcesEmbedDownload(token);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ResourcesEmbedApi#getV2ResourcesEmbedDownload");
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
| **token** | **String**| The token provided when submitting a download request. | |

### Return type

[**GetV2ResourcesEmbedDownload200Response**](GetV2ResourcesEmbedDownload200Response.md)

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

<a id="postV2ResourcesEmbedDownload"></a>
# **postV2ResourcesEmbedDownload**
> PostV2ResourcesEmbedDownload200Response postV2ResourcesEmbedDownload(postV2ResourcesEmbedDownloadRequest)

Submit a new download request

Supported content types:  - &#39;resource_version&#39;  - &#39;api_asset&#39;

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
    PostV2ResourcesEmbedDownloadRequest postV2ResourcesEmbedDownloadRequest = new PostV2ResourcesEmbedDownloadRequest(); // PostV2ResourcesEmbedDownloadRequest | 
    try {
      PostV2ResourcesEmbedDownload200Response result = apiInstance.postV2ResourcesEmbedDownload(postV2ResourcesEmbedDownloadRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ResourcesEmbedApi#postV2ResourcesEmbedDownload");
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
| **postV2ResourcesEmbedDownloadRequest** | [**PostV2ResourcesEmbedDownloadRequest**](PostV2ResourcesEmbedDownloadRequest.md)|  | [optional] |

### Return type

[**PostV2ResourcesEmbedDownload200Response**](PostV2ResourcesEmbedDownload200Response.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

