# IO.Swagger.Api.UserApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**Login**](UserApi.md#login) | **POST** /login | Logs the user in
[**RenewToken**](UserApi.md#renewtoken) | **POST** /login/refreshToken | The user renews access token and refresh token
[**RevokeRefreshToken**](UserApi.md#revokerefreshtoken) | **DELETE** /login/refreshToken | The user revokes a refresh token


<a name="login"></a>
# **Login**
> AccessTokenResponse Login (LoginRequest loginRequest)

Logs the user in

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class LoginExample
    {
        public void main()
        {
            var apiInstance = new UserApi();
            var loginRequest = new LoginRequest(); // LoginRequest | 

            try
            {
                // Logs the user in
                AccessTokenResponse result = apiInstance.Login(loginRequest);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling UserApi.Login: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **loginRequest** | [**LoginRequest**](LoginRequest.md)|  | 

### Return type

[**AccessTokenResponse**](AccessTokenResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="renewtoken"></a>
# **RenewToken**
> AccessTokenResponse RenewToken (RenewTokenRequest renewTokenRequest)

The user renews access token and refresh token

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class RenewTokenExample
    {
        public void main()
        {
            var apiInstance = new UserApi();
            var renewTokenRequest = new RenewTokenRequest(); // RenewTokenRequest | 

            try
            {
                // The user renews access token and refresh token
                AccessTokenResponse result = apiInstance.RenewToken(renewTokenRequest);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling UserApi.RenewToken: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **renewTokenRequest** | [**RenewTokenRequest**](RenewTokenRequest.md)|  | 

### Return type

[**AccessTokenResponse**](AccessTokenResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="revokerefreshtoken"></a>
# **RevokeRefreshToken**
> AccessTokenResponse RevokeRefreshToken (string refreshToken)

The user revokes a refresh token

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class RevokeRefreshTokenExample
    {
        public void main()
        {
            var apiInstance = new UserApi();
            var refreshToken = refreshToken_example;  // string | The refresh token to be revoked

            try
            {
                // The user revokes a refresh token
                AccessTokenResponse result = apiInstance.RevokeRefreshToken(refreshToken);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling UserApi.RevokeRefreshToken: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **refreshToken** | **string**| The refresh token to be revoked | 

### Return type

[**AccessTokenResponse**](AccessTokenResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

