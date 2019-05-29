# IO.Swagger.Api.PredictorScoringApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**CancelAndDeleteBatchExecution**](PredictorScoringApi.md#cancelanddeletebatchexecution) | **DELETE** /api/predictor_scoring/1.0/batch/{executionId} | Cancels and deletes all batch executions for predictor_scoring.
[**GetBatchExecutionFile**](PredictorScoringApi.md#getbatchexecutionfile) | **GET** /api/predictor_scoring/1.0/batch/{executionId}/{index}/files/{fileName} | Gets a specific file from an execution in predictor_scoring.
[**GetBatchExecutionFiles**](PredictorScoringApi.md#getbatchexecutionfiles) | **GET** /api/predictor_scoring/1.0/batch/{executionId}/{index}/files | Gets all files from an individual execution in predictor_scoring.
[**GetBatchExecutionStatus**](PredictorScoringApi.md#getbatchexecutionstatus) | **GET** /api/predictor_scoring/1.0/batch/{executionId} | Gets all batch executions for predictor_scoring.
[**GetBatchExecutions**](PredictorScoringApi.md#getbatchexecutions) | **GET** /api/predictor_scoring/1.0/batch | Gets all batch executions for predictor_scoring.
[**PredictorScoring**](PredictorScoringApi.md#predictorscoring) | **POST** /api/predictor_scoring/1.0 | 
[**StartBatchExecution**](PredictorScoringApi.md#startbatchexecution) | **POST** /api/predictor_scoring/1.0/batch | 


<a name="cancelanddeletebatchexecution"></a>
# **CancelAndDeleteBatchExecution**
> List<string> CancelAndDeleteBatchExecution (string executionId)

Cancels and deletes all batch executions for predictor_scoring.

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class CancelAndDeleteBatchExecutionExample
    {
        public void main()
        {
            // Configure API key authorization: Bearer
            Configuration.Default.AddApiKey("Authorization", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Authorization", "Bearer");

            var apiInstance = new PredictorScoringApi();
            var executionId = executionId_example;  // string | Execution id of the execution.

            try
            {
                // Cancels and deletes all batch executions for predictor_scoring.
                List&lt;string&gt; result = apiInstance.CancelAndDeleteBatchExecution(executionId);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling PredictorScoringApi.CancelAndDeleteBatchExecution: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **executionId** | **string**| Execution id of the execution. | 

### Return type

**List<string>**

### Authorization

[Bearer](../README.md#Bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="getbatchexecutionfile"></a>
# **GetBatchExecutionFile**
> System.IO.Stream GetBatchExecutionFile (string executionId, int? index, string fileName)

Gets a specific file from an execution in predictor_scoring.

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class GetBatchExecutionFileExample
    {
        public void main()
        {
            // Configure API key authorization: Bearer
            Configuration.Default.AddApiKey("Authorization", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Authorization", "Bearer");

            var apiInstance = new PredictorScoringApi();
            var executionId = executionId_example;  // string | Execution id of the execution
            var index = 56;  // int? | Index of the execution in the batch.
            var fileName = fileName_example;  // string | Name of the file to be returned.

            try
            {
                // Gets a specific file from an execution in predictor_scoring.
                System.IO.Stream result = apiInstance.GetBatchExecutionFile(executionId, index, fileName);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling PredictorScoringApi.GetBatchExecutionFile: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **executionId** | **string**| Execution id of the execution | 
 **index** | **int?**| Index of the execution in the batch. | 
 **fileName** | **string**| Name of the file to be returned. | 

### Return type

**System.IO.Stream**

### Authorization

[Bearer](../README.md#Bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="getbatchexecutionfiles"></a>
# **GetBatchExecutionFiles**
> List<string> GetBatchExecutionFiles (string executionId, int? index)

Gets all files from an individual execution in predictor_scoring.

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class GetBatchExecutionFilesExample
    {
        public void main()
        {
            // Configure API key authorization: Bearer
            Configuration.Default.AddApiKey("Authorization", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Authorization", "Bearer");

            var apiInstance = new PredictorScoringApi();
            var executionId = executionId_example;  // string | Execution id of the execution
            var index = 56;  // int? | Index of the execution in the batch.

            try
            {
                // Gets all files from an individual execution in predictor_scoring.
                List&lt;string&gt; result = apiInstance.GetBatchExecutionFiles(executionId, index);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling PredictorScoringApi.GetBatchExecutionFiles: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **executionId** | **string**| Execution id of the execution | 
 **index** | **int?**| Index of the execution in the batch. | 

### Return type

**List<string>**

### Authorization

[Bearer](../README.md#Bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="getbatchexecutionstatus"></a>
# **GetBatchExecutionStatus**
> BatchWebServiceResult GetBatchExecutionStatus (string executionId, bool? showPartialResults = null)

Gets all batch executions for predictor_scoring.

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class GetBatchExecutionStatusExample
    {
        public void main()
        {
            // Configure API key authorization: Bearer
            Configuration.Default.AddApiKey("Authorization", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Authorization", "Bearer");

            var apiInstance = new PredictorScoringApi();
            var executionId = executionId_example;  // string | Execution id of the execution
            var showPartialResults = true;  // bool? | Returns the already processed results of the batch execution even if it hasn't been fully completed. (optional) 

            try
            {
                // Gets all batch executions for predictor_scoring.
                BatchWebServiceResult result = apiInstance.GetBatchExecutionStatus(executionId, showPartialResults);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling PredictorScoringApi.GetBatchExecutionStatus: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **executionId** | **string**| Execution id of the execution | 
 **showPartialResults** | **bool?**| Returns the already processed results of the batch execution even if it hasn&#39;t been fully completed. | [optional] 

### Return type

[**BatchWebServiceResult**](BatchWebServiceResult.md)

### Authorization

[Bearer](../README.md#Bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="getbatchexecutions"></a>
# **GetBatchExecutions**
> List<string> GetBatchExecutions ()

Gets all batch executions for predictor_scoring.

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class GetBatchExecutionsExample
    {
        public void main()
        {
            // Configure API key authorization: Bearer
            Configuration.Default.AddApiKey("Authorization", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Authorization", "Bearer");

            var apiInstance = new PredictorScoringApi();

            try
            {
                // Gets all batch executions for predictor_scoring.
                List&lt;string&gt; result = apiInstance.GetBatchExecutions();
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling PredictorScoringApi.GetBatchExecutions: " + e.Message );
            }
        }
    }
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

**List<string>**

### Authorization

[Bearer](../README.md#Bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="predictorscoring"></a>
# **PredictorScoring**
> WebServiceResult PredictorScoring (InputParameters webServiceParameters)



Consume the predictor_scoring web service.

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class PredictorScoringExample
    {
        public void main()
        {
            // Configure API key authorization: Bearer
            Configuration.Default.AddApiKey("Authorization", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Authorization", "Bearer");

            var apiInstance = new PredictorScoringApi();
            var webServiceParameters = new InputParameters(); // InputParameters | Input parameters to the web service.

            try
            {
                WebServiceResult result = apiInstance.PredictorScoring(webServiceParameters);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling PredictorScoringApi.PredictorScoring: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **webServiceParameters** | [**InputParameters**](InputParameters.md)| Input parameters to the web service. | 

### Return type

[**WebServiceResult**](WebServiceResult.md)

### Authorization

[Bearer](../README.md#Bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a name="startbatchexecution"></a>
# **StartBatchExecution**
> StartBatchExecutionResponse StartBatchExecution (List<InputParameters> batchWebServiceParameters, int? parallelCount = null)



Consume the predictor_scoring web service asynchronously.

### Example
```csharp
using System;
using System.Diagnostics;
using IO.Swagger.Api;
using IO.Swagger.Client;
using IO.Swagger.Model;

namespace Example
{
    public class StartBatchExecutionExample
    {
        public void main()
        {
            // Configure API key authorization: Bearer
            Configuration.Default.AddApiKey("Authorization", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // Configuration.Default.AddApiKeyPrefix("Authorization", "Bearer");

            var apiInstance = new PredictorScoringApi();
            var batchWebServiceParameters = new List<InputParameters>(); // List<InputParameters> | Input parameters to the web service.
            var parallelCount = 56;  // int? | Number of threads used to process entries in the batch. Default value is 10. Please make sure not to use too high of a number because it might negatively impact performance. (optional) 

            try
            {
                StartBatchExecutionResponse result = apiInstance.StartBatchExecution(batchWebServiceParameters, parallelCount);
                Debug.WriteLine(result);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling PredictorScoringApi.StartBatchExecution: " + e.Message );
            }
        }
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **batchWebServiceParameters** | [**List&lt;InputParameters&gt;**](InputParameters.md)| Input parameters to the web service. | 
 **parallelCount** | **int?**| Number of threads used to process entries in the batch. Default value is 10. Please make sure not to use too high of a number because it might negatively impact performance. | [optional] 

### Return type

[**StartBatchExecutionResponse**](StartBatchExecutionResponse.md)

### Authorization

[Bearer](../README.md#Bearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

