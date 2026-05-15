# ResourcesDiscoverCartApi

All URIs are relative to *https://api.builtbybit.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**getV2ResourcesDiscoverCartView**](ResourcesDiscoverCartApi.md#getV2ResourcesDiscoverCartView) | **GET** /v2/resources/discover/cart/view | View the user&#39;s cart items |
| [**postV2ResourcesDiscoverCartAdd**](ResourcesDiscoverCartApi.md#postV2ResourcesDiscoverCartAdd) | **POST** /v2/resources/discover/cart/add | Add items to a user&#39;s cart |
| [**postV2ResourcesDiscoverCartCheckout**](ResourcesDiscoverCartApi.md#postV2ResourcesDiscoverCartCheckout) | **POST** /v2/resources/discover/cart/checkout | Initiate a checkout of a user&#39;s cart |
| [**postV2ResourcesDiscoverCartCouponAdd**](ResourcesDiscoverCartApi.md#postV2ResourcesDiscoverCartCouponAdd) | **POST** /v2/resources/discover/cart/coupon/add | Add a coupon to the user&#39;s cart |
| [**postV2ResourcesDiscoverCartCouponRemove**](ResourcesDiscoverCartApi.md#postV2ResourcesDiscoverCartCouponRemove) | **POST** /v2/resources/discover/cart/coupon/remove | Remove a coupon from the user&#39;s cart |
| [**postV2ResourcesDiscoverCartRemove**](ResourcesDiscoverCartApi.md#postV2ResourcesDiscoverCartRemove) | **POST** /v2/resources/discover/cart/remove | Remove an item from the user&#39;s cart |


<a id="getV2ResourcesDiscoverCartView"></a>
# **getV2ResourcesDiscoverCartView**
> GetV2ResourcesDiscoverCartView200Response getV2ResourcesDiscoverCartView()

View the user&#39;s cart items



### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ResourcesDiscoverCartApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.builtbybit.com");
    
    // Configure OAuth2 access token for authorization: oauth2
    OAuth oauth2 = (OAuth) defaultClient.getAuthentication("oauth2");
    oauth2.setAccessToken("YOUR ACCESS TOKEN");

    ResourcesDiscoverCartApi apiInstance = new ResourcesDiscoverCartApi(defaultClient);
    try {
      GetV2ResourcesDiscoverCartView200Response result = apiInstance.getV2ResourcesDiscoverCartView();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ResourcesDiscoverCartApi#getV2ResourcesDiscoverCartView");
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

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

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
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ResourcesDiscoverCartApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.builtbybit.com");
    
    // Configure OAuth2 access token for authorization: oauth2
    OAuth oauth2 = (OAuth) defaultClient.getAuthentication("oauth2");
    oauth2.setAccessToken("YOUR ACCESS TOKEN");

    ResourcesDiscoverCartApi apiInstance = new ResourcesDiscoverCartApi(defaultClient);
    PostV2ResourcesDiscoverCartAddRequest postV2ResourcesDiscoverCartAddRequest = new PostV2ResourcesDiscoverCartAddRequest(); // PostV2ResourcesDiscoverCartAddRequest | A list of content to add to the user's cart. The outer list is keyed by the content type and the inner list are the content IDs.    For instance, if adding a resource with the ID 555, the body becomes:  ```json  {\"add\": {\"resource\": [555]}}  ```
    try {
      PostV2ResourcesDiscoverCartAdd2XXResponse result = apiInstance.postV2ResourcesDiscoverCartAdd(postV2ResourcesDiscoverCartAddRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ResourcesDiscoverCartApi#postV2ResourcesDiscoverCartAdd");
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

[oauth2](../README.md#oauth2)

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
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ResourcesDiscoverCartApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.builtbybit.com");
    
    // Configure OAuth2 access token for authorization: oauth2
    OAuth oauth2 = (OAuth) defaultClient.getAuthentication("oauth2");
    oauth2.setAccessToken("YOUR ACCESS TOKEN");

    ResourcesDiscoverCartApi apiInstance = new ResourcesDiscoverCartApi(defaultClient);
    Object body = null; // Object | 
    try {
      PostV2ResourcesDiscoverCartCheckout200Response result = apiInstance.postV2ResourcesDiscoverCartCheckout(body);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ResourcesDiscoverCartApi#postV2ResourcesDiscoverCartCheckout");
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

[oauth2](../README.md#oauth2)

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
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ResourcesDiscoverCartApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.builtbybit.com");
    
    // Configure OAuth2 access token for authorization: oauth2
    OAuth oauth2 = (OAuth) defaultClient.getAuthentication("oauth2");
    oauth2.setAccessToken("YOUR ACCESS TOKEN");

    ResourcesDiscoverCartApi apiInstance = new ResourcesDiscoverCartApi(defaultClient);
    PostV2ResourcesDiscoverCartCouponAddRequest postV2ResourcesDiscoverCartCouponAddRequest = new PostV2ResourcesDiscoverCartCouponAddRequest(); // PostV2ResourcesDiscoverCartCouponAddRequest | 
    try {
      PostV2ResourcesDiscoverCartCouponAdd200Response result = apiInstance.postV2ResourcesDiscoverCartCouponAdd(postV2ResourcesDiscoverCartCouponAddRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ResourcesDiscoverCartApi#postV2ResourcesDiscoverCartCouponAdd");
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

[oauth2](../README.md#oauth2)

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
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ResourcesDiscoverCartApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.builtbybit.com");
    
    // Configure OAuth2 access token for authorization: oauth2
    OAuth oauth2 = (OAuth) defaultClient.getAuthentication("oauth2");
    oauth2.setAccessToken("YOUR ACCESS TOKEN");

    ResourcesDiscoverCartApi apiInstance = new ResourcesDiscoverCartApi(defaultClient);
    PostV2ResourcesDiscoverCartCouponRemoveRequest postV2ResourcesDiscoverCartCouponRemoveRequest = new PostV2ResourcesDiscoverCartCouponRemoveRequest(); // PostV2ResourcesDiscoverCartCouponRemoveRequest | 
    try {
      PostV2ResourcesDiscoverCartCouponRemove200Response result = apiInstance.postV2ResourcesDiscoverCartCouponRemove(postV2ResourcesDiscoverCartCouponRemoveRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ResourcesDiscoverCartApi#postV2ResourcesDiscoverCartCouponRemove");
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

[oauth2](../README.md#oauth2)

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
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.ResourcesDiscoverCartApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.builtbybit.com");
    
    // Configure OAuth2 access token for authorization: oauth2
    OAuth oauth2 = (OAuth) defaultClient.getAuthentication("oauth2");
    oauth2.setAccessToken("YOUR ACCESS TOKEN");

    ResourcesDiscoverCartApi apiInstance = new ResourcesDiscoverCartApi(defaultClient);
    PostV2ResourcesDiscoverCartRemoveRequest postV2ResourcesDiscoverCartRemoveRequest = new PostV2ResourcesDiscoverCartRemoveRequest(); // PostV2ResourcesDiscoverCartRemoveRequest | 
    try {
      PostV2ResourcesDiscoverCartRemove200Response result = apiInstance.postV2ResourcesDiscoverCartRemove(postV2ResourcesDiscoverCartRemoveRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ResourcesDiscoverCartApi#postV2ResourcesDiscoverCartRemove");
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

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

