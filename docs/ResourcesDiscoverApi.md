# ResourcesDiscoverApi

All URIs are relative to *https://api.builtbybit.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**getResourcesDiscoverCategories**](ResourcesDiscoverApi.md#getResourcesDiscoverCategories) | **GET** /v2/resources/discover/categories | Fetch a list of categories |
| [**getResourcesDiscoverResources**](ResourcesDiscoverApi.md#getResourcesDiscoverResources) | **GET** /v2/resources/discover/resources | Fetch a list of resources |
| [**getV2ResourcesDiscoverLicenses**](ResourcesDiscoverApi.md#getV2ResourcesDiscoverLicenses) | **GET** /v2/resources/discover/licenses | Fetch a list of the user&#39;s licenses |


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
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ResourcesDiscoverApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.builtbybit.com");
    
    // Configure API key authorization: token
    ApiKeyAuth token = (ApiKeyAuth) defaultClient.getAuthentication("token");
    token.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //token.setApiKeyPrefix("Token");

    ResourcesDiscoverApi apiInstance = new ResourcesDiscoverApi(defaultClient);
    String categoryId = "categoryId_example"; // String | A category ID to filter on.
    String with = "SortOptions"; // String | A comma-separated list of submodels to include.
    try {
      GetResourcesDiscoverCategories200Response result = apiInstance.getResourcesDiscoverCategories(categoryId, with);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ResourcesDiscoverApi#getResourcesDiscoverCategories");
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

<a id="getResourcesDiscoverResources"></a>
# **getResourcesDiscoverResources**
> GetResourcesDiscoverResources200Response getResourcesDiscoverResources(categoryId, with, filters, resourceIds, page, perPage, noDependencies, excludedResourceIds, excludedCreatorIds)

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
import org.openapitools.client.api.ResourcesDiscoverApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.builtbybit.com");
    
    // Configure API key authorization: token
    ApiKeyAuth token = (ApiKeyAuth) defaultClient.getAuthentication("token");
    token.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //token.setApiKeyPrefix("Token");

    ResourcesDiscoverApi apiInstance = new ResourcesDiscoverApi(defaultClient);
    String categoryId = "categoryId_example"; // String | A category ID to filter on. If the provided category is a parent, resources from subcategories will also be included.
    String with = "Description,Creator"; // String | A comma-separated list of additional data to include. See endpoint documentation for more information.
    Object filters = null; // Object | A list of dynamic filters to apply.
    String resourceIds = "resourceIds_example"; // String | A comma-separated list of resource IDs to filter on.
    Integer page = 1; // Integer | The page number to return.
    BigDecimal perPage = new BigDecimal("25"); // BigDecimal | The number of resources to return per page.
    Boolean noDependencies = true; // Boolean | Whether or not to exclude resources with dependencies listed.
    String excludedResourceIds = "excludedResourceIds_example"; // String | A comma-separated list of resource IDs to exclude. No filter will be applied if empty.
    String excludedCreatorIds = "excludedCreatorIds_example"; // String | A comma-separated list of creator IDs to exclude. No filter will be applied if empty.
    try {
      GetResourcesDiscoverResources200Response result = apiInstance.getResourcesDiscoverResources(categoryId, with, filters, resourceIds, page, perPage, noDependencies, excludedResourceIds, excludedCreatorIds);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ResourcesDiscoverApi#getResourcesDiscoverResources");
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
| **noDependencies** | **Boolean**| Whether or not to exclude resources with dependencies listed. | [optional] |
| **excludedResourceIds** | **String**| A comma-separated list of resource IDs to exclude. No filter will be applied if empty. | [optional] |
| **excludedCreatorIds** | **String**| A comma-separated list of creator IDs to exclude. No filter will be applied if empty. | [optional] |

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
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ResourcesDiscoverApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.builtbybit.com");
    
    // Configure OAuth2 access token for authorization: oauth2
    OAuth oauth2 = (OAuth) defaultClient.getAuthentication("oauth2");
    oauth2.setAccessToken("YOUR ACCESS TOKEN");

    ResourcesDiscoverApi apiInstance = new ResourcesDiscoverApi(defaultClient);
    Integer page = 56; // Integer | The page number/offset to return items for.
    Integer perPage = 25; // Integer | The number of items per page to return.
    String with = "with_example"; // String | A comma-separated list of supported 'with hints'. See model & endpoint-level docs for more info.
    try {
      GetV2ResourcesDiscoverLicenses200Response result = apiInstance.getV2ResourcesDiscoverLicenses(page, perPage, with);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ResourcesDiscoverApi#getV2ResourcesDiscoverLicenses");
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

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |
| **4XX** |  |  -  |
| **5XX** |  |  -  |

