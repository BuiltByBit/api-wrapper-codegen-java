# ResourcesCreatorSaleEventsApi

All URIs are relative to *https://api.builtbybit.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**getV2ResourcesCreatorSaleEvents**](ResourcesCreatorSaleEventsApi.md#getV2ResourcesCreatorSaleEvents) | **GET** /v2/resources/creator/sale-events | Fetch a list of your sale events |
| [**getV2ResourcesCreatorSaleEventsEntries**](ResourcesCreatorSaleEventsApi.md#getV2ResourcesCreatorSaleEventsEntries) | **GET** /v2/resources/creator/sale-events/entries | Fetch a list of your sale event entries |


<a id="getV2ResourcesCreatorSaleEvents"></a>
# **getV2ResourcesCreatorSaleEvents**
> GetV2ResourcesCreatorSaleEvents200Response getV2ResourcesCreatorSaleEvents(saleEventIds)

Fetch a list of your sale events

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ResourcesCreatorSaleEventsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.builtbybit.com");
    
    // Configure API key authorization: token
    ApiKeyAuth token = (ApiKeyAuth) defaultClient.getAuthentication("token");
    token.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //token.setApiKeyPrefix("Token");

    ResourcesCreatorSaleEventsApi apiInstance = new ResourcesCreatorSaleEventsApi(defaultClient);
    List saleEventIds = new List(); // List | A comma-separated list of sale event IDs to filter on. No filter is applied if empty.
    try {
      GetV2ResourcesCreatorSaleEvents200Response result = apiInstance.getV2ResourcesCreatorSaleEvents(saleEventIds);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ResourcesCreatorSaleEventsApi#getV2ResourcesCreatorSaleEvents");
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
| **saleEventIds** | [**List**](.md)| A comma-separated list of sale event IDs to filter on. No filter is applied if empty. | [optional] |

### Return type

[**GetV2ResourcesCreatorSaleEvents200Response**](GetV2ResourcesCreatorSaleEvents200Response.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="getV2ResourcesCreatorSaleEventsEntries"></a>
# **getV2ResourcesCreatorSaleEventsEntries**
> GetV2ResourcesCreatorSaleEventsEntries200Response getV2ResourcesCreatorSaleEventsEntries(saleEventIds)

Fetch a list of your sale event entries

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ResourcesCreatorSaleEventsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.builtbybit.com");
    
    // Configure API key authorization: token
    ApiKeyAuth token = (ApiKeyAuth) defaultClient.getAuthentication("token");
    token.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //token.setApiKeyPrefix("Token");

    ResourcesCreatorSaleEventsApi apiInstance = new ResourcesCreatorSaleEventsApi(defaultClient);
    List saleEventIds = new List(); // List | A comma-separated list of sale event IDs to filter on. No filter is applied if empty.
    try {
      GetV2ResourcesCreatorSaleEventsEntries200Response result = apiInstance.getV2ResourcesCreatorSaleEventsEntries(saleEventIds);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ResourcesCreatorSaleEventsApi#getV2ResourcesCreatorSaleEventsEntries");
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
| **saleEventIds** | [**List**](.md)| A comma-separated list of sale event IDs to filter on. No filter is applied if empty. | [optional] |

### Return type

[**GetV2ResourcesCreatorSaleEventsEntries200Response**](GetV2ResourcesCreatorSaleEventsEntries200Response.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

