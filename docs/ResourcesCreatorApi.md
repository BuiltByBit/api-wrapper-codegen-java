# ResourcesCreatorApi

All URIs are relative to *https://api.builtbybit.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**getV2ResourcesCreatorAddons**](ResourcesCreatorApi.md#getV2ResourcesCreatorAddons) | **GET** /v2/resources/creator/addons | Fetch a list of your resources&#39; addons |
| [**getV2ResourcesCreatorBundles**](ResourcesCreatorApi.md#getV2ResourcesCreatorBundles) | **GET** /v2/resources/creator/bundles | Fetch a list of your bundles |
| [**getV2ResourcesCreatorLicenses**](ResourcesCreatorApi.md#getV2ResourcesCreatorLicenses) | **GET** /v2/resources/creator/licenses | Fetch a list of your resources&#39; licenses |
| [**getV2ResourcesCreatorPurchases**](ResourcesCreatorApi.md#getV2ResourcesCreatorPurchases) | **GET** /v2/resources/creator/purchases | Fetch a list of your resources&#39; purchases |
| [**getV2ResourcesCreatorResources**](ResourcesCreatorApi.md#getV2ResourcesCreatorResources) | **GET** /v2/resources/creator/resources | Fetch a list of your resources |
| [**getV2ResourcesCreatorReviews**](ResourcesCreatorApi.md#getV2ResourcesCreatorReviews) | **GET** /v2/resources/creator/reviews | Fetch a list of your resources&#39; reviews |
| [**getV2ResourcesCreatorSaleEvents**](ResourcesCreatorApi.md#getV2ResourcesCreatorSaleEvents) | **GET** /v2/resources/creator/sale-events | Fetch a list of your sale events |
| [**getV2ResourcesCreatorUpdates**](ResourcesCreatorApi.md#getV2ResourcesCreatorUpdates) | **GET** /v2/resources/creator/updates | Fetch a list of your resource&#39;s updates |
| [**getV2ResourcesCreatorVersions**](ResourcesCreatorApi.md#getV2ResourcesCreatorVersions) | **GET** /v2/resources/creator/versions | Fetch a list of your resources&#39; versions |
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

<a id="getV2ResourcesCreatorBundles"></a>
# **getV2ResourcesCreatorBundles**
> GetV2ResourcesCreatorBundles200Response getV2ResourcesCreatorBundles()

Fetch a list of your bundles

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
      GetV2ResourcesCreatorBundles200Response result = apiInstance.getV2ResourcesCreatorBundles();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ResourcesCreatorApi#getV2ResourcesCreatorBundles");
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
> GetV2ResourcesCreatorSaleEvents200Response getV2ResourcesCreatorSaleEvents()

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
    try {
      GetV2ResourcesCreatorSaleEvents200Response result = apiInstance.getV2ResourcesCreatorSaleEvents();
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
This endpoint does not need any parameter.

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

