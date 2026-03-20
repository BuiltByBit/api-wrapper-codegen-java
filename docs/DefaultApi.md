# DefaultApi

All URIs are relative to *https://api.builtbybit.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**getV2Analytics**](DefaultApi.md#getV2Analytics) | **GET** /v2/analytics | Fetch a list of analytics definitions |
| [**getV2AnalyticsGraph**](DefaultApi.md#getV2AnalyticsGraph) | **GET** /v2/analytics/graph | Fetch analytics graph data |
| [**getV2Events**](DefaultApi.md#getV2Events) | **GET** /v2/events | Fetch a list of pending events |
| [**postV2EventsComplete**](DefaultApi.md#postV2EventsComplete) | **POST** /v2/events/complete | Mark events as complete |
| [**postV2ResourcesCreatorUpdate**](DefaultApi.md#postV2ResourcesCreatorUpdate) | **POST** /v2/resources/creator/update | Post a resource update |


<a id="getV2Analytics"></a>
# **getV2Analytics**
> GetV2Analytics200Response getV2Analytics()

Fetch a list of analytics definitions

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
    try {
      GetV2Analytics200Response result = apiInstance.getV2Analytics();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#getV2Analytics");
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

[**GetV2Analytics200Response**](GetV2Analytics200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="getV2AnalyticsGraph"></a>
# **getV2AnalyticsGraph**
> GetV2AnalyticsGraph200Response getV2AnalyticsGraph(analytics, period, grouping, filters, startDate, endDate)

Fetch analytics graph data

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
    List analytics = new List(); // List | 
    String period = "period_example"; // String | 
    String grouping = "grouping_example"; // String | 
    String filters = "filters_example"; // String | 
    String startDate = "startDate_example"; // String | Only respected when 'period' = 'custom_range'.
    String endDate = "endDate_example"; // String | Only respected when 'period' = 'custom_range'.
    try {
      GetV2AnalyticsGraph200Response result = apiInstance.getV2AnalyticsGraph(analytics, period, grouping, filters, startDate, endDate);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#getV2AnalyticsGraph");
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
| **analytics** | [**List**](.md)|  | [optional] |
| **period** | **String**|  | [optional] |
| **grouping** | **String**|  | [optional] |
| **filters** | **String**|  | [optional] |
| **startDate** | **String**| Only respected when &#39;period&#39; &#x3D; &#39;custom_range&#39;. | [optional] |
| **endDate** | **String**| Only respected when &#39;period&#39; &#x3D; &#39;custom_range&#39;. | [optional] |

### Return type

[**GetV2AnalyticsGraph200Response**](GetV2AnalyticsGraph200Response.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

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
import org.openapitools.client.models.*;
import org.openapitools.client.api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.builtbybit.com");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    try {
      GetV2Events200Response result = apiInstance.getV2Events();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#getV2Events");
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

No authorization required

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
import org.openapitools.client.api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.builtbybit.com");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    PostV2EventsCompleteRequest postV2EventsCompleteRequest = new PostV2EventsCompleteRequest(); // PostV2EventsCompleteRequest | 
    try {
      PostV2EventsComplete200Response result = apiInstance.postV2EventsComplete(postV2EventsCompleteRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#postV2EventsComplete");
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
import org.openapitools.client.models.*;
import org.openapitools.client.api.DefaultApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.builtbybit.com");

    DefaultApi apiInstance = new DefaultApi(defaultClient);
    PostV2ResourcesCreatorUpdateRequest postV2ResourcesCreatorUpdateRequest = new PostV2ResourcesCreatorUpdateRequest(); // PostV2ResourcesCreatorUpdateRequest | 
    try {
      PostV2ResourcesCreatorUpdate200Response result = apiInstance.postV2ResourcesCreatorUpdate(postV2ResourcesCreatorUpdateRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DefaultApi#postV2ResourcesCreatorUpdate");
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

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

