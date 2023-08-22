# {{classname}}

All URIs are relative to *https://{environment}.hafiztheexplorer.com/api/v1/servers*

Method | HTTP request | Description
------------- | ------------- | -------------
[**TodolistGet**](ToDoListApi.md#TodolistGet) | **Get** /todolist | mengambil data todolistnya
[**TodolistPost**](ToDoListApi.md#TodolistPost) | **Post** /todolist | menambah data todolistnya
[**TodolistTodolistIdDelete**](ToDoListApi.md#TodolistTodolistIdDelete) | **Delete** /todolist/{todolistId} | menghapus data todolistnya
[**TodolistTodolistIdPut**](ToDoListApi.md#TodolistTodolistIdPut) | **Put** /todolist/{todolistId} | mengedit data todolistnya

# **TodolistGet**
> []Showtodolist TodolistGet(ctx, optional)
mengambil data todolistnya

hanya akan mengembalikan data to-do-list yang aktif, data to-do-list yang sudah dihapus atau semua data to-do-list tidak akan di return

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***ToDoListApiTodolistGetOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a ToDoListApiTodolistGetOpts struct
Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **includeDone** | **optional.Bool**| include done todolist dalam hasil | [default to true]
 **name** | **optional.String**| mencari data todolist by name | 

### Return type

[**[]Showtodolist**](array.md)

### Authorization

[todolistAuth](../README.md#todolistAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **TodolistPost**
> Showtodolist TodolistPost(ctx, body)
menambah data todolistnya

hanya akan menambah data to-do-list

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **body** | [**Createupdatetodolistwithvalidation**](Createupdatetodolistwithvalidation.md)|  | 

### Return type

[**Showtodolist**](showtodolist.md)

### Authorization

[todolistAuth](../README.md#todolistAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **TodolistTodolistIdDelete**
> InlineResponse200 TodolistTodolistIdDelete(ctx, todolistId)
menghapus data todolistnya

hanya akan menghapus data to-do-list yang dipilih

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **todolistId** | **string**| todolist id mana yang diedit | 

### Return type

[**InlineResponse200**](inline_response_200.md)

### Authorization

[todolistAuth](../README.md#todolistAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **TodolistTodolistIdPut**
> Showtodolist TodolistTodolistIdPut(ctx, body, todolistId)
mengedit data todolistnya

hanya akan mengedit data to-do-list yang dipilih

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **body** | [**Createupdatetodolistwithvalidation**](Createupdatetodolistwithvalidation.md)|  | 
  **todolistId** | **string**| todolist id mana yang diedit | 

### Return type

[**Showtodolist**](showtodolist.md)

### Authorization

[todolistAuth](../README.md#todolistAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

