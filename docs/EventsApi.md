# EventsApi

All URIs are relative to *https://api.builtbybit.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**getV2Events**](EventsApi.md#getV2Events) | **GET** /v2/events | Fetch a list of pending events |
| [**postV2EventsComplete**](EventsApi.md#postV2EventsComplete) | **POST** /v2/events/complete | Mark events as complete |


<a id="getV2Events"></a>
# **getV2Events**
> GetV2Events200Response getV2Events()

Fetch a list of pending events

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.EventsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.builtbybit.com");
    
    // Configure API key authorization: token
    ApiKeyAuth token = (ApiKeyAuth) defaultClient.getAuthentication("token");
    token.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //token.setApiKeyPrefix("Token");

    EventsApi apiInstance = new EventsApi(defaultClient);
    try {
      GetV2Events200Response result = apiInstance.getV2Events();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EventsApi#getV2Events");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**GetV2Events200Response**](GetV2Events200Response.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="postV2EventsComplete"></a>
# **postV2EventsComplete**
> PostV2EventsComplete200Response postV2EventsComplete(postV2EventsCompleteRequest)

Mark events as complete

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.models.*;
import org.openapitools.client.api.EventsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.builtbybit.com");

    EventsApi apiInstance = new EventsApi(defaultClient);
    PostV2EventsCompleteRequest postV2EventsCompleteRequest = new PostV2EventsCompleteRequest(); // PostV2EventsCompleteRequest | 
    try {
      PostV2EventsComplete200Response result = apiInstance.postV2EventsComplete(postV2EventsCompleteRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EventsApi#postV2EventsComplete");
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
| **postV2EventsCompleteRequest** | [**PostV2EventsCompleteRequest**](PostV2EventsCompleteRequest.md)|  | [optional] |

### Return type

[**PostV2EventsComplete200Response**](PostV2EventsComplete200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

