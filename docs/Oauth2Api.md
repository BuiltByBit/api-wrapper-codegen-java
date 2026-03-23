# Oauth2Api

All URIs are relative to *https://api.builtbybit.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**getOauth2Token**](Oauth2Api.md#getOauth2Token) | **POST** /oauth2/token | Request an access token using an existing grant |
| [**getOauth2TokenRevoke**](Oauth2Api.md#getOauth2TokenRevoke) | **POST** /oauth2/token/revoke | Revoke an existing access or refresh token |


<a id="getOauth2Token"></a>
# **getOauth2Token**
> GetOauth2Token200Response getOauth2Token(grantType, code, refreshToken)

Request an access token using an existing grant

Supported grant types: &#x60;authorization_code&#x60;, and &#x60;refresh_token&#x60;.  Must authenticate via HTTP Basic Authentication, using your OAuth2 client credentials.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.Oauth2Api;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.builtbybit.com");
    
    // Configure API key authorization: token
    ApiKeyAuth token = (ApiKeyAuth) defaultClient.getAuthentication("token");
    token.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //token.setApiKeyPrefix("Token");

    Oauth2Api apiInstance = new Oauth2Api(defaultClient);
    String grantType = "grantType_example"; // String | 
    String code = "code_example"; // String | Required if grant_type = `authorization_code`.
    String refreshToken = "refreshToken_example"; // String | Required if grant_type = `refresh_token`.
    try {
      GetOauth2Token200Response result = apiInstance.getOauth2Token(grantType, code, refreshToken);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling Oauth2Api#getOauth2Token");
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
| **grantType** | **String**|  | |
| **code** | **String**| Required if grant_type &#x3D; &#x60;authorization_code&#x60;. | [optional] |
| **refreshToken** | **String**| Required if grant_type &#x3D; &#x60;refresh_token&#x60;. | [optional] |

### Return type

[**GetOauth2Token200Response**](GetOauth2Token200Response.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="getOauth2TokenRevoke"></a>
# **getOauth2TokenRevoke**
> GetOauth2TokenRevoke200Response getOauth2TokenRevoke(authorization, token, tokenHint)

Revoke an existing access or refresh token

Must authenticate via HTTP Basic Authentication, using your OAuth2 client credentials.

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.Oauth2Api;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://api.builtbybit.com");
    
    // Configure API key authorization: token
    ApiKeyAuth token = (ApiKeyAuth) defaultClient.getAuthentication("token");
    token.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //token.setApiKeyPrefix("Token");

    Oauth2Api apiInstance = new Oauth2Api(defaultClient);
    String authorization = "authorization_example"; // String | OAuth2 client credentials in the Basic authorization format.
    String token = "token_example"; // String | 
    String tokenHint = "tokenHint_example"; // String | 
    try {
      GetOauth2TokenRevoke200Response result = apiInstance.getOauth2TokenRevoke(authorization, token, tokenHint);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling Oauth2Api#getOauth2TokenRevoke");
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
| **authorization** | **String**| OAuth2 client credentials in the Basic authorization format. | |
| **token** | **String**|  | |
| **tokenHint** | **String**|  | [optional] |

### Return type

[**GetOauth2TokenRevoke200Response**](GetOauth2TokenRevoke200Response.md)

### Authorization

[token](../README.md#token)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

