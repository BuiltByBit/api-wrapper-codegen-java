# DiscoveryApi

All URIs are relative to *https://api.builtbybit.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**getResourcesDiscoverCategories**](DiscoveryApi.md#getResourcesDiscoverCategories) | **GET** /v2/resources/discover/categories | Fetch a list of categories |
| [**getResourcesDiscoverResources**](DiscoveryApi.md#getResourcesDiscoverResources) | **GET** /v2/resources/discover/resources | Fetch a list of resources |
| [**getV2ResourcesDiscoverCartView**](DiscoveryApi.md#getV2ResourcesDiscoverCartView) | **GET** /v2/resources/discover/cart/view | View the user&#39;s cart items |
| [**getV2ResourcesDiscoverLicenses**](DiscoveryApi.md#getV2ResourcesDiscoverLicenses) | **GET** /v2/resources/discover/licenses | Fetch a list of the user&#39;s licenses |
| [**postV2ResourcesDiscoverCartAdd**](DiscoveryApi.md#postV2ResourcesDiscoverCartAdd) | **POST** /v2/resources/discover/cart/add | Add items to a user&#39;s cart |
| [**postV2ResourcesDiscoverCartCheckout**](DiscoveryApi.md#postV2ResourcesDiscoverCartCheckout) | **POST** /v2/resources/discover/cart/checkout | Initiate a checkout of a user&#39;s cart |
| [**postV2ResourcesDiscoverCartCouponAdd**](DiscoveryApi.md#postV2ResourcesDiscoverCartCouponAdd) | **POST** /v2/resources/discover/cart/coupon/add | Add a coupon to the user&#39;s cart |
| [**postV2ResourcesDiscoverCartCouponRemove**](DiscoveryApi.md#postV2ResourcesDiscoverCartCouponRemove) | **POST** /v2/resources/discover/cart/coupon/remove | Remove a coupon from the user&#39;s cart |
| [**postV2ResourcesDiscoverCartRemove**](DiscoveryApi.md#postV2ResourcesDiscoverCartRemove) | **POST** /v2/resources/discover/cart/remove | Remove an item from the user&#39;s cart |


<a id="getResourcesDiscoverCategories"></a>
# **getResourcesDiscoverCategories**
> GetResourcesDiscoverCategories200Response getResourcesDiscoverCategories(categoryId, with)

Fetch a list of categories

Supported &#39;with&#39; hints:  - Children: includes all subcategories and their children

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.models.*;
import org.openapitools.client.api.DiscoveryApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.builtbybit.com");

    DiscoveryApi apiInstance = new DiscoveryApi(defaultClient);
    String categoryId = "categoryId_example"; // String | A category ID to filter on.
    String with = "SortOptions"; // String | A comma-separated list of submodels to include.
    try {
      GetResourcesDiscoverCategories200Response result = apiInstance.getResourcesDiscoverCategories(categoryId, with);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DiscoveryApi#getResourcesDiscoverCategories");
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
| **categoryId** | **String**| A category ID to filter on. | [optional] |
| **with** | **String**| A comma-separated list of submodels to include. | [optional] [enum: SortOptions, FilterOptions] |

### Return type

[**GetResourcesDiscoverCategories200Response**](GetResourcesDiscoverCategories200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |
| **4XX** |  |  -  |
| **5XX** |  |  -  |

<a id="getResourcesDiscoverResources"></a>
# **getResourcesDiscoverResources**
> GetResourcesDiscoverResources200Response getResourcesDiscoverResources(categoryId, with, filters, resourceIds, page, perPage, noDependencies)

Fetch a list of resources

Supported &#39;with&#39; hints:  - &#x60;filters&#x60;: include dynamic filter information in the response.  - See &#39;Resource&#39; model for additional &#39;with&#39; hints.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.DiscoveryApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.builtbybit.com");
    
    // Configure API key authorization: token
    ApiKeyAuth token = (ApiKeyAuth) defaultClient.getAuthentication("token");
    token.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //token.setApiKeyPrefix("Token");

    DiscoveryApi apiInstance = new DiscoveryApi(defaultClient);
    String categoryId = "categoryId_example"; // String | A category ID to filter on. If the provided category is a parent, resources from subcategories will also be included.
    String with = "Description,Creator"; // String | A comma-separated list of additional data to include. See endpoint documentation for more information.
    Object filters = null; // Object | A list of dynamic filters to apply.
    String resourceIds = "resourceIds_example"; // String | A comma-separated list of resource IDs to filter on.
    Integer page = 1; // Integer | The page number to return.
    BigDecimal perPage = new BigDecimal("25"); // BigDecimal | The number of resources to return per page.
    Boolean noDependencies = true; // Boolean | 
    try {
      GetResourcesDiscoverResources200Response result = apiInstance.getResourcesDiscoverResources(categoryId, with, filters, resourceIds, page, perPage, noDependencies);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DiscoveryApi#getResourcesDiscoverResources");
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
| **categoryId** | **String**| A category ID to filter on. If the provided category is a parent, resources from subcategories will also be included. | [optional] |
| **with** | **String**| A comma-separated list of additional data to include. See endpoint documentation for more information. | [optional] |
| **filters** | [**Object**](.md)| A list of dynamic filters to apply. | [optional] |
| **resourceIds** | **String**| A comma-separated list of resource IDs to filter on. | [optional] |
| **page** | **Integer**| The page number to return. | [optional] [default to 1] |
| **perPage** | **BigDecimal**| The number of resources to return per page. | [optional] [default to 25] |
| **noDependencies** | **Boolean**|  | [optional] |

### Return type

[**GetResourcesDiscoverResources200Response**](GetResourcesDiscoverResources200Response.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |
| **4XX** |  |  -  |
| **5XX** |  |  -  |

<a id="getV2ResourcesDiscoverCartView"></a>
# **getV2ResourcesDiscoverCartView**
> GetV2ResourcesDiscoverCartView200Response getV2ResourcesDiscoverCartView()

View the user&#39;s cart items

Supported &#39;with hints&#39;:

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.models.*;
import org.openapitools.client.api.DiscoveryApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.builtbybit.com");

    DiscoveryApi apiInstance = new DiscoveryApi(defaultClient);
    try {
      GetV2ResourcesDiscoverCartView200Response result = apiInstance.getV2ResourcesDiscoverCartView();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DiscoveryApi#getV2ResourcesDiscoverCartView");
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

[**GetV2ResourcesDiscoverCartView200Response**](GetV2ResourcesDiscoverCartView200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="getV2ResourcesDiscoverLicenses"></a>
# **getV2ResourcesDiscoverLicenses**
> GetV2ResourcesDiscoverLicenses200Response getV2ResourcesDiscoverLicenses(page, perPage, with)

Fetch a list of the user&#39;s licenses

Supported &#39;with&#39; hints:  - Resource: the resource the license is for if content_type &#x3D; &#x60;resource&#x60;

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.models.*;
import org.openapitools.client.api.DiscoveryApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.builtbybit.com");

    DiscoveryApi apiInstance = new DiscoveryApi(defaultClient);
    Integer page = 56; // Integer | The page number/offset to return items for.
    Integer perPage = 25; // Integer | The number of items per page to return.
    String with = "with_example"; // String | A comma-separated list of supported 'with hints'. See model & endpoint-level docs for more info.
    try {
      GetV2ResourcesDiscoverLicenses200Response result = apiInstance.getV2ResourcesDiscoverLicenses(page, perPage, with);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DiscoveryApi#getV2ResourcesDiscoverLicenses");
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
| **page** | **Integer**| The page number/offset to return items for. | [optional] |
| **perPage** | **Integer**| The number of items per page to return. | [optional] [default to 25] |
| **with** | **String**| A comma-separated list of supported &#39;with hints&#39;. See model &amp; endpoint-level docs for more info. | [optional] |

### Return type

[**GetV2ResourcesDiscoverLicenses200Response**](GetV2ResourcesDiscoverLicenses200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |
| **4XX** |  |  -  |
| **5XX** |  |  -  |

<a id="postV2ResourcesDiscoverCartAdd"></a>
# **postV2ResourcesDiscoverCartAdd**
> PostV2ResourcesDiscoverCartAdd2XXResponse postV2ResourcesDiscoverCartAdd(postV2ResourcesDiscoverCartAddRequest)

Add items to a user&#39;s cart

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.models.*;
import org.openapitools.client.api.DiscoveryApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.builtbybit.com");

    DiscoveryApi apiInstance = new DiscoveryApi(defaultClient);
    PostV2ResourcesDiscoverCartAddRequest postV2ResourcesDiscoverCartAddRequest = new PostV2ResourcesDiscoverCartAddRequest(); // PostV2ResourcesDiscoverCartAddRequest | A list of content to add to the user's cart. The outer list is keyed by the content type and the inner list are the content IDs.    For instance, if adding a resource with the ID 555, the body becomes:  ```json  {\"add\": {\"resource\": [555]}}  ```
    try {
      PostV2ResourcesDiscoverCartAdd2XXResponse result = apiInstance.postV2ResourcesDiscoverCartAdd(postV2ResourcesDiscoverCartAddRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DiscoveryApi#postV2ResourcesDiscoverCartAdd");
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
| **postV2ResourcesDiscoverCartAddRequest** | [**PostV2ResourcesDiscoverCartAddRequest**](PostV2ResourcesDiscoverCartAddRequest.md)| A list of content to add to the user&#39;s cart. The outer list is keyed by the content type and the inner list are the content IDs.    For instance, if adding a resource with the ID 555, the body becomes:  &#x60;&#x60;&#x60;json  {\&quot;add\&quot;: {\&quot;resource\&quot;: [555]}}  &#x60;&#x60;&#x60; | [optional] |

### Return type

[**PostV2ResourcesDiscoverCartAdd2XXResponse**](PostV2ResourcesDiscoverCartAdd2XXResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **2XX** | Success |  -  |

<a id="postV2ResourcesDiscoverCartCheckout"></a>
# **postV2ResourcesDiscoverCartCheckout**
> PostV2ResourcesDiscoverCartCheckout200Response postV2ResourcesDiscoverCartCheckout(body)

Initiate a checkout of a user&#39;s cart

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.models.*;
import org.openapitools.client.api.DiscoveryApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.builtbybit.com");

    DiscoveryApi apiInstance = new DiscoveryApi(defaultClient);
    Object body = null; // Object | 
    try {
      PostV2ResourcesDiscoverCartCheckout200Response result = apiInstance.postV2ResourcesDiscoverCartCheckout(body);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DiscoveryApi#postV2ResourcesDiscoverCartCheckout");
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
| **body** | **Object**|  | [optional] |

### Return type

[**PostV2ResourcesDiscoverCartCheckout200Response**](PostV2ResourcesDiscoverCartCheckout200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="postV2ResourcesDiscoverCartCouponAdd"></a>
# **postV2ResourcesDiscoverCartCouponAdd**
> PostV2ResourcesDiscoverCartCouponAdd200Response postV2ResourcesDiscoverCartCouponAdd(postV2ResourcesDiscoverCartCouponAddRequest)

Add a coupon to the user&#39;s cart

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.models.*;
import org.openapitools.client.api.DiscoveryApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.builtbybit.com");

    DiscoveryApi apiInstance = new DiscoveryApi(defaultClient);
    PostV2ResourcesDiscoverCartCouponAddRequest postV2ResourcesDiscoverCartCouponAddRequest = new PostV2ResourcesDiscoverCartCouponAddRequest(); // PostV2ResourcesDiscoverCartCouponAddRequest | 
    try {
      PostV2ResourcesDiscoverCartCouponAdd200Response result = apiInstance.postV2ResourcesDiscoverCartCouponAdd(postV2ResourcesDiscoverCartCouponAddRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DiscoveryApi#postV2ResourcesDiscoverCartCouponAdd");
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
| **postV2ResourcesDiscoverCartCouponAddRequest** | [**PostV2ResourcesDiscoverCartCouponAddRequest**](PostV2ResourcesDiscoverCartCouponAddRequest.md)|  | [optional] |

### Return type

[**PostV2ResourcesDiscoverCartCouponAdd200Response**](PostV2ResourcesDiscoverCartCouponAdd200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="postV2ResourcesDiscoverCartCouponRemove"></a>
# **postV2ResourcesDiscoverCartCouponRemove**
> PostV2ResourcesDiscoverCartCouponRemove200Response postV2ResourcesDiscoverCartCouponRemove(postV2ResourcesDiscoverCartCouponRemoveRequest)

Remove a coupon from the user&#39;s cart

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.models.*;
import org.openapitools.client.api.DiscoveryApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.builtbybit.com");

    DiscoveryApi apiInstance = new DiscoveryApi(defaultClient);
    PostV2ResourcesDiscoverCartCouponRemoveRequest postV2ResourcesDiscoverCartCouponRemoveRequest = new PostV2ResourcesDiscoverCartCouponRemoveRequest(); // PostV2ResourcesDiscoverCartCouponRemoveRequest | 
    try {
      PostV2ResourcesDiscoverCartCouponRemove200Response result = apiInstance.postV2ResourcesDiscoverCartCouponRemove(postV2ResourcesDiscoverCartCouponRemoveRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DiscoveryApi#postV2ResourcesDiscoverCartCouponRemove");
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
| **postV2ResourcesDiscoverCartCouponRemoveRequest** | [**PostV2ResourcesDiscoverCartCouponRemoveRequest**](PostV2ResourcesDiscoverCartCouponRemoveRequest.md)|  | [optional] |

### Return type

[**PostV2ResourcesDiscoverCartCouponRemove200Response**](PostV2ResourcesDiscoverCartCouponRemove200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="postV2ResourcesDiscoverCartRemove"></a>
# **postV2ResourcesDiscoverCartRemove**
> PostV2ResourcesDiscoverCartRemove200Response postV2ResourcesDiscoverCartRemove(postV2ResourcesDiscoverCartRemoveRequest)

Remove an item from the user&#39;s cart

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.models.*;
import org.openapitools.client.api.DiscoveryApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.builtbybit.com");

    DiscoveryApi apiInstance = new DiscoveryApi(defaultClient);
    PostV2ResourcesDiscoverCartRemoveRequest postV2ResourcesDiscoverCartRemoveRequest = new PostV2ResourcesDiscoverCartRemoveRequest(); // PostV2ResourcesDiscoverCartRemoveRequest | 
    try {
      PostV2ResourcesDiscoverCartRemove200Response result = apiInstance.postV2ResourcesDiscoverCartRemove(postV2ResourcesDiscoverCartRemoveRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DiscoveryApi#postV2ResourcesDiscoverCartRemove");
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
| **postV2ResourcesDiscoverCartRemoveRequest** | [**PostV2ResourcesDiscoverCartRemoveRequest**](PostV2ResourcesDiscoverCartRemoveRequest.md)|  | [optional] |

### Return type

[**PostV2ResourcesDiscoverCartRemove200Response**](PostV2ResourcesDiscoverCartRemove200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

