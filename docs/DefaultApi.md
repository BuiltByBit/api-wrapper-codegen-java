# DefaultApi

All URIs are relative to *https://api.builtbybit.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**getV2ResourcesCreatorBatch**](DefaultApi.md#getV2ResourcesCreatorBatch) | **GET** /v2/resources/creator/batch | Fetch a list of your batches edits |
| [**postV2ResourcesCreatorBatch**](DefaultApi.md#postV2ResourcesCreatorBatch) | **POST** /v2/resources/creator/batch | Submit a new batch edit |


<a id="getV2ResourcesCreatorBatch"></a>
# **getV2ResourcesCreatorBatch**
> GetV2ResourcesCreatorBatch200Response getV2ResourcesCreatorBatch(batchIds)

Fetch a list of your batches edits

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.builtbybit.com");
    
    // Configure API key authorization: token
    ApiKeyAuth token = (ApiKeyAuth) defaultClient.getAuthentication("token");
    token.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //token.setApiKeyPrefix("Token");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    List batchIds = new List(); // List | A comma-separated list of batch IDs to filter on. No filter is applied if empty.
    try {
      GetV2ResourcesCreatorBatch200Response result = apiInstance.getV2ResourcesCreatorBatch(batchIds);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#getV2ResourcesCreatorBatch");
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
| **batchIds** | [**List**](.md)| A comma-separated list of batch IDs to filter on. No filter is applied if empty. | [optional] |

### Return type

[**GetV2ResourcesCreatorBatch200Response**](GetV2ResourcesCreatorBatch200Response.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="postV2ResourcesCreatorBatch"></a>
# **postV2ResourcesCreatorBatch**
> PostV2ResourcesCreatorBatch200Response postV2ResourcesCreatorBatch(postV2ResourcesCreatorBatchRequest)

Submit a new batch edit

Batch edits will be processed in the background meaning a successful call to this endpoint does not guarantee that the edits have been completed. You will instead receive an identifier to a batch edit which you can then use to fetch the status of via the below endpoint. This is not an atomic operation meaning some resources may be edited successfully and others may not be due to an error. You may only batch edit resources you own currently.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.models.*;
import org.openapitools.client.api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.builtbybit.com");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    PostV2ResourcesCreatorBatchRequest postV2ResourcesCreatorBatchRequest = new PostV2ResourcesCreatorBatchRequest(); // PostV2ResourcesCreatorBatchRequest | 
    try {
      PostV2ResourcesCreatorBatch200Response result = apiInstance.postV2ResourcesCreatorBatch(postV2ResourcesCreatorBatchRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#postV2ResourcesCreatorBatch");
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
| **postV2ResourcesCreatorBatchRequest** | [**PostV2ResourcesCreatorBatchRequest**](PostV2ResourcesCreatorBatchRequest.md)|  | [optional] |

### Return type

[**PostV2ResourcesCreatorBatch200Response**](PostV2ResourcesCreatorBatch200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

