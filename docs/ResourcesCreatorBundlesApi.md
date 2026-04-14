# ResourcesCreatorBundlesApi

All URIs are relative to *https://api.builtbybit.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**getV2ResourcesCreatorBundles**](ResourcesCreatorBundlesApi.md#getV2ResourcesCreatorBundles) | **GET** /v2/resources/creator/bundles | Fetch a list of your bundles |
| [**getV2ResourcesCreatorBundlesEntries**](ResourcesCreatorBundlesApi.md#getV2ResourcesCreatorBundlesEntries) | **GET** /v2/resources/creator/bundles/entries | Fetch a list of your bundle entries |


<a id="getV2ResourcesCreatorBundles"></a>
# **getV2ResourcesCreatorBundles**
> GetV2ResourcesCreatorBundles200Response getV2ResourcesCreatorBundles(bundleIds)

Fetch a list of your bundles

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ResourcesCreatorBundlesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.builtbybit.com");
    
    // Configure API key authorization: token
    ApiKeyAuth token = (ApiKeyAuth) defaultClient.getAuthentication("token");
    token.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //token.setApiKeyPrefix("Token");

    ResourcesCreatorBundlesApi apiInstance = new ResourcesCreatorBundlesApi(defaultClient);
    List bundleIds = new List(); // List | A comma-separated list of bundle IDs to filter on. No filter is applied if empty.
    try {
      GetV2ResourcesCreatorBundles200Response result = apiInstance.getV2ResourcesCreatorBundles(bundleIds);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ResourcesCreatorBundlesApi#getV2ResourcesCreatorBundles");
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
| **bundleIds** | [**List**](.md)| A comma-separated list of bundle IDs to filter on. No filter is applied if empty. | [optional] |

### Return type

[**GetV2ResourcesCreatorBundles200Response**](GetV2ResourcesCreatorBundles200Response.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="getV2ResourcesCreatorBundlesEntries"></a>
# **getV2ResourcesCreatorBundlesEntries**
> GetV2ResourcesCreatorBundlesEntries200Response getV2ResourcesCreatorBundlesEntries(bundleIds)

Fetch a list of your bundle entries

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ResourcesCreatorBundlesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.builtbybit.com");
    
    // Configure API key authorization: token
    ApiKeyAuth token = (ApiKeyAuth) defaultClient.getAuthentication("token");
    token.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //token.setApiKeyPrefix("Token");

    ResourcesCreatorBundlesApi apiInstance = new ResourcesCreatorBundlesApi(defaultClient);
    List bundleIds = new List(); // List | A comma-separated list of bundle IDs to filter on. No filter is applied if empty.
    try {
      GetV2ResourcesCreatorBundlesEntries200Response result = apiInstance.getV2ResourcesCreatorBundlesEntries(bundleIds);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ResourcesCreatorBundlesApi#getV2ResourcesCreatorBundlesEntries");
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
| **bundleIds** | [**List**](.md)| A comma-separated list of bundle IDs to filter on. No filter is applied if empty. | [optional] |

### Return type

[**GetV2ResourcesCreatorBundlesEntries200Response**](GetV2ResourcesCreatorBundlesEntries200Response.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

