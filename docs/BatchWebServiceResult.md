# IO.Swagger.Model.BatchWebServiceResult
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**State** | **string** | State of the execution. Can be of the following values:  - Pending: The batch execution was submitted but is not yet scheduled. Ready: The batch execution was submitted and can be executed. InProgress: The batch execution is currently being processed. Complete: The batch execution has been completed. | [optional] 
**CompletedItemCount** | **int?** | Number of completed items in this batch operation. | [optional] 
**TotalItemCount** | **int?** | Number of total items in this batch operation. | [optional] 
**ParallelCount** | **int?** | Number of parallel threads that are processing this batch operation. | [optional] 
**BatchExecutionResults** | [**List&lt;WebServiceResult&gt;**](WebServiceResult.md) | The responses of the individual executions. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

