# DeploymentsApi

All URIs are relative to *https://api.builtbybit.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**postV2DeploymentsUpgrade**](DeploymentsApi.md#postV2DeploymentsUpgrade) | **POST** /v2/deployments/upgrade | Upgrade a short-lived token |


<a id="postV2DeploymentsUpgrade"></a>
# **postV2DeploymentsUpgrade**
> PostV2DeploymentsUpgrade200Response postV2DeploymentsUpgrade(postV2DeploymentsUpgradeRequest)

Upgrade a short-lived token



### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.DeploymentsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.builtbybit.com");
    
    // Configure API key authorization: token
    ApiKeyAuth token = (ApiKeyAuth) defaultClient.getAuthentication("token");
    token.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //token.setApiKeyPrefix("Token");

    DeploymentsApi apiInstance = new DeploymentsApi(defaultClient);
    PostV2DeploymentsUpgradeRequest postV2DeploymentsUpgradeRequest = new PostV2DeploymentsUpgradeRequest(); // PostV2DeploymentsUpgradeRequest | 
    try {
      PostV2DeploymentsUpgrade200Response result = apiInstance.postV2DeploymentsUpgrade(postV2DeploymentsUpgradeRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DeploymentsApi#postV2DeploymentsUpgrade");
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
| **postV2DeploymentsUpgradeRequest** | [**PostV2DeploymentsUpgradeRequest**](PostV2DeploymentsUpgradeRequest.md)|  | [optional] |

### Return type

[**PostV2DeploymentsUpgrade200Response**](PostV2DeploymentsUpgrade200Response.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

