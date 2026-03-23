# GlobalApi

All URIs are relative to *https://api.builtbybit.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**getV2Analytics**](GlobalApi.md#getV2Analytics) | **GET** /v2/analytics | Fetch a list of analytics definitions |
| [**getV2AnalyticsGraph**](GlobalApi.md#getV2AnalyticsGraph) | **GET** /v2/analytics/graph | Fetch analytics graph data |
| [**getV2AnalyticsSingle**](GlobalApi.md#getV2AnalyticsSingle) | **GET** /v2/analytics/single | Fetch a single analytics value |
| [**getV2Events**](GlobalApi.md#getV2Events) | **GET** /v2/events | Fetch a list of pending events |
| [**postV2EventsComplete**](GlobalApi.md#postV2EventsComplete) | **POST** /v2/events/complete | Mark events as complete |


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
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.GlobalApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.builtbybit.com");
    
    // Configure API key authorization: token
    ApiKeyAuth token = (ApiKeyAuth) defaultClient.getAuthentication("token");
    token.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //token.setApiKeyPrefix("Token");

    GlobalApi apiInstance = new GlobalApi(defaultClient);
    try {
      GetV2Analytics200Response result = apiInstance.getV2Analytics();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GlobalApi#getV2Analytics");
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

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="getV2AnalyticsGraph"></a>
# **getV2AnalyticsGraph**
> GetV2AnalyticsGraph200Response getV2AnalyticsGraph(analytics, period, filters, startDate, endDate)

Fetch analytics graph data

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.GlobalApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.builtbybit.com");
    
    // Configure API key authorization: token
    ApiKeyAuth token = (ApiKeyAuth) defaultClient.getAuthentication("token");
    token.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //token.setApiKeyPrefix("Token");

    GlobalApi apiInstance = new GlobalApi(defaultClient);
    List analytics = new List(); // List | A list of analytic IDs to fetch data for.
    String period = "period_example"; // String | The time period to fetch data over.
    List filters = new List(); // List | A set of filters which may be used for the analytics.
    String startDate = "startDate_example"; // String | Only respected when 'period' = 'custom_range', in the format 'YYYY-MM-DD'.
    String endDate = "endDate_example"; // String | Only respected when 'period' = 'custom_range', in the format 'YYYY-MM-DD'.
    try {
      GetV2AnalyticsGraph200Response result = apiInstance.getV2AnalyticsGraph(analytics, period, filters, startDate, endDate);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GlobalApi#getV2AnalyticsGraph");
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
| **analytics** | [**List**](.md)| A list of analytic IDs to fetch data for. | [optional] |
| **period** | **String**| The time period to fetch data over. | [optional] |
| **filters** | [**List**](.md)| A set of filters which may be used for the analytics. | [optional] |
| **startDate** | **String**| Only respected when &#39;period&#39; &#x3D; &#39;custom_range&#39;, in the format &#39;YYYY-MM-DD&#39;. | [optional] |
| **endDate** | **String**| Only respected when &#39;period&#39; &#x3D; &#39;custom_range&#39;, in the format &#39;YYYY-MM-DD&#39;. | [optional] |

### Return type

[**GetV2AnalyticsGraph200Response**](GetV2AnalyticsGraph200Response.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="getV2AnalyticsSingle"></a>
# **getV2AnalyticsSingle**
> GetV2AnalyticsSingle200Response getV2AnalyticsSingle(analytics, period, filters, startDate, endDate)

Fetch a single analytics value

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.GlobalApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.builtbybit.com");
    
    // Configure API key authorization: token
    ApiKeyAuth token = (ApiKeyAuth) defaultClient.getAuthentication("token");
    token.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //token.setApiKeyPrefix("Token");

    GlobalApi apiInstance = new GlobalApi(defaultClient);
    List analytics = new List(); // List | A list of analytic IDs to fetch data for.
    String period = "period_example"; // String | The time period to fetch data over.
    List filters = new List(); // List | A set of filters which may be used for the analytics.
    String startDate = "startDate_example"; // String | Only respected when 'period' = 'custom_range', in the format 'YYYY-MM-DD'.
    String endDate = "endDate_example"; // String | Only respected when 'period' = 'custom_range', in the format 'YYYY-MM-DD'.
    try {
      GetV2AnalyticsSingle200Response result = apiInstance.getV2AnalyticsSingle(analytics, period, filters, startDate, endDate);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GlobalApi#getV2AnalyticsSingle");
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
| **analytics** | [**List**](.md)| A list of analytic IDs to fetch data for. | [optional] |
| **period** | **String**| The time period to fetch data over. | [optional] |
| **filters** | [**List**](.md)| A set of filters which may be used for the analytics. | [optional] |
| **startDate** | **String**| Only respected when &#39;period&#39; &#x3D; &#39;custom_range&#39;, in the format &#39;YYYY-MM-DD&#39;. | [optional] |
| **endDate** | **String**| Only respected when &#39;period&#39; &#x3D; &#39;custom_range&#39;, in the format &#39;YYYY-MM-DD&#39;. | [optional] |

### Return type

[**GetV2AnalyticsSingle200Response**](GetV2AnalyticsSingle200Response.md)

### Authorization

[token](../README.md#token)

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
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.GlobalApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.builtbybit.com");
    
    // Configure API key authorization: token
    ApiKeyAuth token = (ApiKeyAuth) defaultClient.getAuthentication("token");
    token.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //token.setApiKeyPrefix("Token");

    GlobalApi apiInstance = new GlobalApi(defaultClient);
    try {
      GetV2Events200Response result = apiInstance.getV2Events();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GlobalApi#getV2Events");
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

[token](../README.md#token)

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
import org.openapitools.client.api.GlobalApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.builtbybit.com");

    GlobalApi apiInstance = new GlobalApi(defaultClient);
    PostV2EventsCompleteRequest postV2EventsCompleteRequest = new PostV2EventsCompleteRequest(); // PostV2EventsCompleteRequest | 
    try {
      PostV2EventsComplete200Response result = apiInstance.postV2EventsComplete(postV2EventsCompleteRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GlobalApi#postV2EventsComplete");
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

