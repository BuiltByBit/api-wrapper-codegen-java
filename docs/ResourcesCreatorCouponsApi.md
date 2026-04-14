# ResourcesCreatorCouponsApi

All URIs are relative to *https://api.builtbybit.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**getV2ResourcesCreatorCoupons**](ResourcesCreatorCouponsApi.md#getV2ResourcesCreatorCoupons) | **GET** /v2/resources/creator/coupons | Fetch a list of your coupons |
| [**getV2ResourcesCreatorCouponsEntries**](ResourcesCreatorCouponsApi.md#getV2ResourcesCreatorCouponsEntries) | **GET** /v2/resources/creator/coupons/entries | Fetch a list of your coupon entries |
| [**postV2ResourcesCreatorCoupons**](ResourcesCreatorCouponsApi.md#postV2ResourcesCreatorCoupons) | **POST** /v2/resources/creator/coupons | Create a new coupon |


<a id="getV2ResourcesCreatorCoupons"></a>
# **getV2ResourcesCreatorCoupons**
> GetV2ResourcesCreatorCoupons200Response getV2ResourcesCreatorCoupons(couponIds)

Fetch a list of your coupons

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ResourcesCreatorCouponsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.builtbybit.com");
    
    // Configure API key authorization: token
    ApiKeyAuth token = (ApiKeyAuth) defaultClient.getAuthentication("token");
    token.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //token.setApiKeyPrefix("Token");

    ResourcesCreatorCouponsApi apiInstance = new ResourcesCreatorCouponsApi(defaultClient);
    List couponIds = new List(); // List | A comma-separated list of coupon IDs to filter on. No filter is applied if empty.
    try {
      GetV2ResourcesCreatorCoupons200Response result = apiInstance.getV2ResourcesCreatorCoupons(couponIds);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ResourcesCreatorCouponsApi#getV2ResourcesCreatorCoupons");
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
| **couponIds** | [**List**](.md)| A comma-separated list of coupon IDs to filter on. No filter is applied if empty. | [optional] |

### Return type

[**GetV2ResourcesCreatorCoupons200Response**](GetV2ResourcesCreatorCoupons200Response.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="getV2ResourcesCreatorCouponsEntries"></a>
# **getV2ResourcesCreatorCouponsEntries**
> GetV2ResourcesCreatorCouponsEntries200Response getV2ResourcesCreatorCouponsEntries(couponIds)

Fetch a list of your coupon entries

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ResourcesCreatorCouponsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.builtbybit.com");
    
    // Configure API key authorization: token
    ApiKeyAuth token = (ApiKeyAuth) defaultClient.getAuthentication("token");
    token.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //token.setApiKeyPrefix("Token");

    ResourcesCreatorCouponsApi apiInstance = new ResourcesCreatorCouponsApi(defaultClient);
    List couponIds = new List(); // List | A comma-separated list of coupon IDs to filter on. No filter is applied if empty.
    try {
      GetV2ResourcesCreatorCouponsEntries200Response result = apiInstance.getV2ResourcesCreatorCouponsEntries(couponIds);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ResourcesCreatorCouponsApi#getV2ResourcesCreatorCouponsEntries");
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
| **couponIds** | [**List**](.md)| A comma-separated list of coupon IDs to filter on. No filter is applied if empty. | [optional] |

### Return type

[**GetV2ResourcesCreatorCouponsEntries200Response**](GetV2ResourcesCreatorCouponsEntries200Response.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="postV2ResourcesCreatorCoupons"></a>
# **postV2ResourcesCreatorCoupons**
> PostV2ResourcesCreatorCoupons200Response postV2ResourcesCreatorCoupons(postV2ResourcesCreatorCouponsRequest)

Create a new coupon

This endpoint is currently limited to percent-based coupons with a maximum discount of 50%.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ResourcesCreatorCouponsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.builtbybit.com");
    
    // Configure API key authorization: token
    ApiKeyAuth token = (ApiKeyAuth) defaultClient.getAuthentication("token");
    token.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //token.setApiKeyPrefix("Token");

    ResourcesCreatorCouponsApi apiInstance = new ResourcesCreatorCouponsApi(defaultClient);
    PostV2ResourcesCreatorCouponsRequest postV2ResourcesCreatorCouponsRequest = new PostV2ResourcesCreatorCouponsRequest(); // PostV2ResourcesCreatorCouponsRequest | 
    try {
      PostV2ResourcesCreatorCoupons200Response result = apiInstance.postV2ResourcesCreatorCoupons(postV2ResourcesCreatorCouponsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ResourcesCreatorCouponsApi#postV2ResourcesCreatorCoupons");
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
| **postV2ResourcesCreatorCouponsRequest** | [**PostV2ResourcesCreatorCouponsRequest**](PostV2ResourcesCreatorCouponsRequest.md)|  | [optional] |

### Return type

[**PostV2ResourcesCreatorCoupons200Response**](PostV2ResourcesCreatorCoupons200Response.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

