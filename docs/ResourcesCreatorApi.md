# ResourcesCreatorApi

All URIs are relative to *https://api.builtbybit.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**getV2ResourcesCreatorAddons**](ResourcesCreatorApi.md#getV2ResourcesCreatorAddons) | **GET** /v2/resources/creator/addons | Fetch a list of your resources&#39; addons |
| [**getV2ResourcesCreatorBatch**](ResourcesCreatorApi.md#getV2ResourcesCreatorBatch) | **GET** /v2/resources/creator/batch | Fetch a list of your batches edits |
| [**getV2ResourcesCreatorCoupons**](ResourcesCreatorApi.md#getV2ResourcesCreatorCoupons) | **GET** /v2/resources/creator/coupons | Fetch a list of your coupons |
| [**getV2ResourcesCreatorCouponsEntries**](ResourcesCreatorApi.md#getV2ResourcesCreatorCouponsEntries) | **GET** /v2/resources/creator/coupons/entries | Fetch a list of your coupon entries |
| [**getV2ResourcesCreatorLicenses**](ResourcesCreatorApi.md#getV2ResourcesCreatorLicenses) | **GET** /v2/resources/creator/licenses | Fetch a list of your resources&#39; licenses |
| [**getV2ResourcesCreatorPurchases**](ResourcesCreatorApi.md#getV2ResourcesCreatorPurchases) | **GET** /v2/resources/creator/purchases | Fetch a list of your resources&#39; purchases |
| [**getV2ResourcesCreatorResources**](ResourcesCreatorApi.md#getV2ResourcesCreatorResources) | **GET** /v2/resources/creator/resources | Fetch a list of your resources |
| [**getV2ResourcesCreatorReviews**](ResourcesCreatorApi.md#getV2ResourcesCreatorReviews) | **GET** /v2/resources/creator/reviews | Fetch a list of your resources&#39; reviews |
| [**getV2ResourcesCreatorSaleEvents**](ResourcesCreatorApi.md#getV2ResourcesCreatorSaleEvents) | **GET** /v2/resources/creator/sale-events | Fetch a list of your sale events |
| [**getV2ResourcesCreatorSaleEventsEntries**](ResourcesCreatorApi.md#getV2ResourcesCreatorSaleEventsEntries) | **GET** /v2/resources/creator/sale-events/entries | Fetch a list of your sale event entries |
| [**getV2ResourcesCreatorStores**](ResourcesCreatorApi.md#getV2ResourcesCreatorStores) | **GET** /v2/resources/creator/stores | Fetch a list of your stores |
| [**getV2ResourcesCreatorUpdates**](ResourcesCreatorApi.md#getV2ResourcesCreatorUpdates) | **GET** /v2/resources/creator/updates | Fetch a list of your resource&#39;s updates |
| [**getV2ResourcesCreatorVersions**](ResourcesCreatorApi.md#getV2ResourcesCreatorVersions) | **GET** /v2/resources/creator/versions | Fetch a list of your resources&#39; versions |
| [**postV2ResourcesCreatorBatch**](ResourcesCreatorApi.md#postV2ResourcesCreatorBatch) | **POST** /v2/resources/creator/batch | Submit a new batch edit |
| [**postV2ResourcesCreatorCoupons**](ResourcesCreatorApi.md#postV2ResourcesCreatorCoupons) | **POST** /v2/resources/creator/coupons | Create a new coupon |
| [**postV2ResourcesCreatorUpdate**](ResourcesCreatorApi.md#postV2ResourcesCreatorUpdate) | **POST** /v2/resources/creator/update | Post a resource update |


<a id="getV2ResourcesCreatorAddons"></a>
# **getV2ResourcesCreatorAddons**
> GetV2ResourcesCreatorAddons200Response getV2ResourcesCreatorAddons(resourceIds)

Fetch a list of your resources&#39; addons

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ResourcesCreatorApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.builtbybit.com");
    
    // Configure API key authorization: token
    ApiKeyAuth token = (ApiKeyAuth) defaultClient.getAuthentication("token");
    token.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //token.setApiKeyPrefix("Token");

    ResourcesCreatorApi apiInstance = new ResourcesCreatorApi(defaultClient);
    List resourceIds = new List(); // List | A comma-separated list of resource IDs to filter on. No filter is applied if empty.
    try {
      GetV2ResourcesCreatorAddons200Response result = apiInstance.getV2ResourcesCreatorAddons(resourceIds);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ResourcesCreatorApi#getV2ResourcesCreatorAddons");
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
| **resourceIds** | [**List**](.md)| A comma-separated list of resource IDs to filter on. No filter is applied if empty. | [optional] |

### Return type

[**GetV2ResourcesCreatorAddons200Response**](GetV2ResourcesCreatorAddons200Response.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

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
import org.openapitools.client.api.ResourcesCreatorApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.builtbybit.com");
    
    // Configure API key authorization: token
    ApiKeyAuth token = (ApiKeyAuth) defaultClient.getAuthentication("token");
    token.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //token.setApiKeyPrefix("Token");

    ResourcesCreatorApi apiInstance = new ResourcesCreatorApi(defaultClient);
    List batchIds = new List(); // List | A comma-separated list of batch IDs to filter on. No filter is applied if empty.
    try {
      GetV2ResourcesCreatorBatch200Response result = apiInstance.getV2ResourcesCreatorBatch(batchIds);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ResourcesCreatorApi#getV2ResourcesCreatorBatch");
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
import org.openapitools.client.api.ResourcesCreatorApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.builtbybit.com");
    
    // Configure API key authorization: token
    ApiKeyAuth token = (ApiKeyAuth) defaultClient.getAuthentication("token");
    token.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //token.setApiKeyPrefix("Token");

    ResourcesCreatorApi apiInstance = new ResourcesCreatorApi(defaultClient);
    List couponIds = new List(); // List | A comma-separated list of coupon IDs to filter on. No filter is applied if empty.
    try {
      GetV2ResourcesCreatorCoupons200Response result = apiInstance.getV2ResourcesCreatorCoupons(couponIds);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ResourcesCreatorApi#getV2ResourcesCreatorCoupons");
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
import org.openapitools.client.api.ResourcesCreatorApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.builtbybit.com");
    
    // Configure API key authorization: token
    ApiKeyAuth token = (ApiKeyAuth) defaultClient.getAuthentication("token");
    token.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //token.setApiKeyPrefix("Token");

    ResourcesCreatorApi apiInstance = new ResourcesCreatorApi(defaultClient);
    List couponIds = new List(); // List | A comma-separated list of coupon IDs to filter on. No filter is applied if empty.
    try {
      GetV2ResourcesCreatorCouponsEntries200Response result = apiInstance.getV2ResourcesCreatorCouponsEntries(couponIds);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ResourcesCreatorApi#getV2ResourcesCreatorCouponsEntries");
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

<a id="getV2ResourcesCreatorLicenses"></a>
# **getV2ResourcesCreatorLicenses**
> GetV2ResourcesCreatorLicenses200Response getV2ResourcesCreatorLicenses(resourceIds)

Fetch a list of your resources&#39; licenses

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ResourcesCreatorApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.builtbybit.com");
    
    // Configure API key authorization: token
    ApiKeyAuth token = (ApiKeyAuth) defaultClient.getAuthentication("token");
    token.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //token.setApiKeyPrefix("Token");

    ResourcesCreatorApi apiInstance = new ResourcesCreatorApi(defaultClient);
    List resourceIds = new List(); // List | A comma-separated list of resource IDs to filter on. No filter is applied if empty.
    try {
      GetV2ResourcesCreatorLicenses200Response result = apiInstance.getV2ResourcesCreatorLicenses(resourceIds);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ResourcesCreatorApi#getV2ResourcesCreatorLicenses");
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
| **resourceIds** | [**List**](.md)| A comma-separated list of resource IDs to filter on. No filter is applied if empty. | [optional] |

### Return type

[**GetV2ResourcesCreatorLicenses200Response**](GetV2ResourcesCreatorLicenses200Response.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="getV2ResourcesCreatorPurchases"></a>
# **getV2ResourcesCreatorPurchases**
> GetV2ResourcesCreatorPurchases200Response getV2ResourcesCreatorPurchases(resourceIds, buyerIds, externalTids)

Fetch a list of your resources&#39; purchases

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ResourcesCreatorApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.builtbybit.com");
    
    // Configure API key authorization: token
    ApiKeyAuth token = (ApiKeyAuth) defaultClient.getAuthentication("token");
    token.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //token.setApiKeyPrefix("Token");

    ResourcesCreatorApi apiInstance = new ResourcesCreatorApi(defaultClient);
    List resourceIds = new List(); // List | A comma-separated list of resource IDs to filter on. No filter is applied if empty.
    List buyerIds = new List(); // List | A comma-separated list of buyer IDs to filter on. No filter is applied if empty
    List externalTids = new List(); // List | A comma-separated list of external transaction IDs (TIDs) to filter on. No filter is applied if empty.
    try {
      GetV2ResourcesCreatorPurchases200Response result = apiInstance.getV2ResourcesCreatorPurchases(resourceIds, buyerIds, externalTids);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ResourcesCreatorApi#getV2ResourcesCreatorPurchases");
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
| **resourceIds** | [**List**](.md)| A comma-separated list of resource IDs to filter on. No filter is applied if empty. | [optional] |
| **buyerIds** | [**List**](.md)| A comma-separated list of buyer IDs to filter on. No filter is applied if empty | [optional] |
| **externalTids** | [**List**](.md)| A comma-separated list of external transaction IDs (TIDs) to filter on. No filter is applied if empty. | [optional] |

### Return type

[**GetV2ResourcesCreatorPurchases200Response**](GetV2ResourcesCreatorPurchases200Response.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="getV2ResourcesCreatorResources"></a>
# **getV2ResourcesCreatorResources**
> GetV2ResourcesCreatorResources200Response getV2ResourcesCreatorResources(resourceIds)

Fetch a list of your resources

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ResourcesCreatorApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.builtbybit.com");
    
    // Configure API key authorization: token
    ApiKeyAuth token = (ApiKeyAuth) defaultClient.getAuthentication("token");
    token.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //token.setApiKeyPrefix("Token");

    ResourcesCreatorApi apiInstance = new ResourcesCreatorApi(defaultClient);
    List resourceIds = new List(); // List | A comma-separated list of resource IDs to filter on. No filter is applied if empty.
    try {
      GetV2ResourcesCreatorResources200Response result = apiInstance.getV2ResourcesCreatorResources(resourceIds);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ResourcesCreatorApi#getV2ResourcesCreatorResources");
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
| **resourceIds** | [**List**](.md)| A comma-separated list of resource IDs to filter on. No filter is applied if empty. | [optional] |

### Return type

[**GetV2ResourcesCreatorResources200Response**](GetV2ResourcesCreatorResources200Response.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="getV2ResourcesCreatorReviews"></a>
# **getV2ResourcesCreatorReviews**
> GetV2ResourcesCreatorReviews200Response getV2ResourcesCreatorReviews(resourceIds)

Fetch a list of your resources&#39; reviews

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ResourcesCreatorApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.builtbybit.com");

    ResourcesCreatorApi apiInstance = new ResourcesCreatorApi(defaultClient);
    List resourceIds = new List(); // List | A comma-separated list of resource IDs to filter on. No filter is applied if empty.
    try {
      GetV2ResourcesCreatorReviews200Response result = apiInstance.getV2ResourcesCreatorReviews(resourceIds);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ResourcesCreatorApi#getV2ResourcesCreatorReviews");
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
| **resourceIds** | [**List**](.md)| A comma-separated list of resource IDs to filter on. No filter is applied if empty. | [optional] |

### Return type

[**GetV2ResourcesCreatorReviews200Response**](GetV2ResourcesCreatorReviews200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

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
import org.openapitools.client.api.ResourcesCreatorApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.builtbybit.com");
    
    // Configure API key authorization: token
    ApiKeyAuth token = (ApiKeyAuth) defaultClient.getAuthentication("token");
    token.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //token.setApiKeyPrefix("Token");

    ResourcesCreatorApi apiInstance = new ResourcesCreatorApi(defaultClient);
    List saleEventIds = new List(); // List | A comma-separated list of sale event IDs to filter on. No filter is applied if empty.
    try {
      GetV2ResourcesCreatorSaleEvents200Response result = apiInstance.getV2ResourcesCreatorSaleEvents(saleEventIds);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ResourcesCreatorApi#getV2ResourcesCreatorSaleEvents");
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
import org.openapitools.client.api.ResourcesCreatorApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.builtbybit.com");
    
    // Configure API key authorization: token
    ApiKeyAuth token = (ApiKeyAuth) defaultClient.getAuthentication("token");
    token.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //token.setApiKeyPrefix("Token");

    ResourcesCreatorApi apiInstance = new ResourcesCreatorApi(defaultClient);
    List saleEventIds = new List(); // List | A comma-separated list of sale event IDs to filter on. No filter is applied if empty.
    try {
      GetV2ResourcesCreatorSaleEventsEntries200Response result = apiInstance.getV2ResourcesCreatorSaleEventsEntries(saleEventIds);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ResourcesCreatorApi#getV2ResourcesCreatorSaleEventsEntries");
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

<a id="getV2ResourcesCreatorStores"></a>
# **getV2ResourcesCreatorStores**
> GetV2ResourcesCreatorStores200Response getV2ResourcesCreatorStores()

Fetch a list of your stores

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ResourcesCreatorApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.builtbybit.com");
    
    // Configure API key authorization: token
    ApiKeyAuth token = (ApiKeyAuth) defaultClient.getAuthentication("token");
    token.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //token.setApiKeyPrefix("Token");

    ResourcesCreatorApi apiInstance = new ResourcesCreatorApi(defaultClient);
    try {
      GetV2ResourcesCreatorStores200Response result = apiInstance.getV2ResourcesCreatorStores();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ResourcesCreatorApi#getV2ResourcesCreatorStores");
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

[**GetV2ResourcesCreatorStores200Response**](GetV2ResourcesCreatorStores200Response.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="getV2ResourcesCreatorUpdates"></a>
# **getV2ResourcesCreatorUpdates**
> GetV2ResourcesCreatorUpdates200Response getV2ResourcesCreatorUpdates(resourceIds)

Fetch a list of your resource&#39;s updates

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ResourcesCreatorApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.builtbybit.com");
    
    // Configure API key authorization: token
    ApiKeyAuth token = (ApiKeyAuth) defaultClient.getAuthentication("token");
    token.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //token.setApiKeyPrefix("Token");

    ResourcesCreatorApi apiInstance = new ResourcesCreatorApi(defaultClient);
    List resourceIds = new List(); // List | A comma-separated list of resource IDs to filter on. No filter is applied if empty.
    try {
      GetV2ResourcesCreatorUpdates200Response result = apiInstance.getV2ResourcesCreatorUpdates(resourceIds);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ResourcesCreatorApi#getV2ResourcesCreatorUpdates");
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
| **resourceIds** | [**List**](.md)| A comma-separated list of resource IDs to filter on. No filter is applied if empty. | [optional] |

### Return type

[**GetV2ResourcesCreatorUpdates200Response**](GetV2ResourcesCreatorUpdates200Response.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="getV2ResourcesCreatorVersions"></a>
# **getV2ResourcesCreatorVersions**
> GetV2ResourcesCreatorVersions200Response getV2ResourcesCreatorVersions(resourceIds)

Fetch a list of your resources&#39; versions

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ResourcesCreatorApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.builtbybit.com");
    
    // Configure API key authorization: token
    ApiKeyAuth token = (ApiKeyAuth) defaultClient.getAuthentication("token");
    token.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //token.setApiKeyPrefix("Token");

    ResourcesCreatorApi apiInstance = new ResourcesCreatorApi(defaultClient);
    List resourceIds = new List(); // List | A comma-separated list of resource IDs to filter on. No filter is applied if empty.
    try {
      GetV2ResourcesCreatorVersions200Response result = apiInstance.getV2ResourcesCreatorVersions(resourceIds);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ResourcesCreatorApi#getV2ResourcesCreatorVersions");
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
| **resourceIds** | [**List**](.md)| A comma-separated list of resource IDs to filter on. No filter is applied if empty. | [optional] |

### Return type

[**GetV2ResourcesCreatorVersions200Response**](GetV2ResourcesCreatorVersions200Response.md)

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
import org.openapitools.client.api.ResourcesCreatorApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.builtbybit.com");

    ResourcesCreatorApi apiInstance = new ResourcesCreatorApi(defaultClient);
    PostV2ResourcesCreatorBatchRequest postV2ResourcesCreatorBatchRequest = new PostV2ResourcesCreatorBatchRequest(); // PostV2ResourcesCreatorBatchRequest | 
    try {
      PostV2ResourcesCreatorBatch200Response result = apiInstance.postV2ResourcesCreatorBatch(postV2ResourcesCreatorBatchRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ResourcesCreatorApi#postV2ResourcesCreatorBatch");
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
import org.openapitools.client.api.ResourcesCreatorApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.builtbybit.com");
    
    // Configure API key authorization: token
    ApiKeyAuth token = (ApiKeyAuth) defaultClient.getAuthentication("token");
    token.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //token.setApiKeyPrefix("Token");

    ResourcesCreatorApi apiInstance = new ResourcesCreatorApi(defaultClient);
    PostV2ResourcesCreatorCouponsRequest postV2ResourcesCreatorCouponsRequest = new PostV2ResourcesCreatorCouponsRequest(); // PostV2ResourcesCreatorCouponsRequest | 
    try {
      PostV2ResourcesCreatorCoupons200Response result = apiInstance.postV2ResourcesCreatorCoupons(postV2ResourcesCreatorCouponsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ResourcesCreatorApi#postV2ResourcesCreatorCoupons");
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

<a id="postV2ResourcesCreatorUpdate"></a>
# **postV2ResourcesCreatorUpdate**
> PostV2ResourcesCreatorUpdate200Response postV2ResourcesCreatorUpdate(postV2ResourcesCreatorUpdateRequest)

Post a resource update

Creates a new version for the resource and optionally posts a public update message. The uploaded file must be encoded using base64 as part of the JSON request body shown below.    The request body (including the base64 encoded file data) cannot exceed 100MB. This roughly equates to a 67MB upload limit for the raw file when taking into account base64 encoding losses.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ResourcesCreatorApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.builtbybit.com");
    
    // Configure API key authorization: token
    ApiKeyAuth token = (ApiKeyAuth) defaultClient.getAuthentication("token");
    token.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //token.setApiKeyPrefix("Token");

    ResourcesCreatorApi apiInstance = new ResourcesCreatorApi(defaultClient);
    PostV2ResourcesCreatorUpdateRequest postV2ResourcesCreatorUpdateRequest = new PostV2ResourcesCreatorUpdateRequest(); // PostV2ResourcesCreatorUpdateRequest | 
    try {
      PostV2ResourcesCreatorUpdate200Response result = apiInstance.postV2ResourcesCreatorUpdate(postV2ResourcesCreatorUpdateRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ResourcesCreatorApi#postV2ResourcesCreatorUpdate");
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
| **postV2ResourcesCreatorUpdateRequest** | [**PostV2ResourcesCreatorUpdateRequest**](PostV2ResourcesCreatorUpdateRequest.md)|  | [optional] |

### Return type

[**PostV2ResourcesCreatorUpdate200Response**](PostV2ResourcesCreatorUpdate200Response.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

