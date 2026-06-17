# \TestsAPI

All URIs are relative to *https://apidev.elev8er.ai/public/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**CreateTest**](TestsAPI.md#CreateTest) | **Post** /tests | Create a test
[**CreateTestVersion**](TestsAPI.md#CreateTestVersion) | **Post** /tests/{id}/versions | Create a new version of a test
[**DeleteTest**](TestsAPI.md#DeleteTest) | **Delete** /tests/{id} | Delete a test
[**GetTest**](TestsAPI.md#GetTest) | **Get** /tests/{id} | Get a test by id
[**GetTestVersion**](TestsAPI.md#GetTestVersion) | **Get** /tests/{id}/versions/{versionId} | Get a specific test version
[**ListTestVersions**](TestsAPI.md#ListTestVersions) | **Get** /tests/{id}/versions | List versions of a test
[**ListTests**](TestsAPI.md#ListTests) | **Get** /tests | List tests
[**RollbackTestVersion**](TestsAPI.md#RollbackTestVersion) | **Post** /tests/{id}/versions/{versionId}/rollback | Roll a test back to a specific version
[**UpdateTest**](TestsAPI.md#UpdateTest) | **Put** /tests/{id} | Update a test
[**UpdateTestVersion**](TestsAPI.md#UpdateTestVersion) | **Put** /tests/{id}/versions/{versionId} | Update a specific test version



## CreateTest

> SuccessEnvelope CreateTest(ctx).RequestBody(requestBody).Execute()

Create a test

### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
	openapiclient "github.com/elev8er/elev8er-go-sdk"
)

func main() {
	requestBody := map[string]interface{}{"key": interface{}(123)} // map[string]interface{} | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.TestsAPI.CreateTest(context.Background()).RequestBody(requestBody).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `TestsAPI.CreateTest``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `CreateTest`: SuccessEnvelope
	fmt.Fprintf(os.Stdout, "Response from `TestsAPI.CreateTest`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiCreateTestRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **requestBody** | **map[string]interface{}** |  | 

### Return type

[**SuccessEnvelope**](SuccessEnvelope.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## CreateTestVersion

> SuccessEnvelope CreateTestVersion(ctx, id).Body(body).Execute()

Create a new version of a test

### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
	openapiclient "github.com/elev8er/elev8er-go-sdk"
)

func main() {
	id := "id_example" // string | 
	body := map[string]interface{}{ ... } // map[string]interface{} | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.TestsAPI.CreateTestVersion(context.Background(), id).Body(body).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `TestsAPI.CreateTestVersion``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `CreateTestVersion`: SuccessEnvelope
	fmt.Fprintf(os.Stdout, "Response from `TestsAPI.CreateTestVersion`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiCreateTestVersionRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **body** | **map[string]interface{}** |  | 

### Return type

[**SuccessEnvelope**](SuccessEnvelope.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## DeleteTest

> DeleteTest(ctx, id).Execute()

Delete a test

### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
	openapiclient "github.com/elev8er/elev8er-go-sdk"
)

func main() {
	id := "id_example" // string | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	r, err := apiClient.TestsAPI.DeleteTest(context.Background(), id).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `TestsAPI.DeleteTest``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiDeleteTestRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


### Return type

 (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetTest

> SuccessEnvelope GetTest(ctx, id).Execute()

Get a test by id

### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
	openapiclient "github.com/elev8er/elev8er-go-sdk"
)

func main() {
	id := "id_example" // string | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.TestsAPI.GetTest(context.Background(), id).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `TestsAPI.GetTest``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetTest`: SuccessEnvelope
	fmt.Fprintf(os.Stdout, "Response from `TestsAPI.GetTest`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetTestRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


### Return type

[**SuccessEnvelope**](SuccessEnvelope.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetTestVersion

> SuccessEnvelope GetTestVersion(ctx, id, versionId).Execute()

Get a specific test version

### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
	openapiclient "github.com/elev8er/elev8er-go-sdk"
)

func main() {
	id := "id_example" // string | 
	versionId := "versionId_example" // string | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.TestsAPI.GetTestVersion(context.Background(), id, versionId).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `TestsAPI.GetTestVersion``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetTestVersion`: SuccessEnvelope
	fmt.Fprintf(os.Stdout, "Response from `TestsAPI.GetTestVersion`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** |  | 
**versionId** | **string** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetTestVersionRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------



### Return type

[**SuccessEnvelope**](SuccessEnvelope.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ListTestVersions

> SuccessEnvelope ListTestVersions(ctx, id).Execute()

List versions of a test

### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
	openapiclient "github.com/elev8er/elev8er-go-sdk"
)

func main() {
	id := "id_example" // string | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.TestsAPI.ListTestVersions(context.Background(), id).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `TestsAPI.ListTestVersions``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListTestVersions`: SuccessEnvelope
	fmt.Fprintf(os.Stdout, "Response from `TestsAPI.ListTestVersions`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiListTestVersionsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


### Return type

[**SuccessEnvelope**](SuccessEnvelope.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ListTests

> SuccessEnvelope ListTests(ctx).Page(page).Limit(limit).Search(search).Execute()

List tests

### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
	openapiclient "github.com/elev8er/elev8er-go-sdk"
)

func main() {
	page := int32(56) // int32 | 1-based page number. (optional) (default to 1)
	limit := int32(56) // int32 | Items per page (max 100). (optional) (default to 20)
	search := "search_example" // string | Free-text search filter. (optional)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.TestsAPI.ListTests(context.Background()).Page(page).Limit(limit).Search(search).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `TestsAPI.ListTests``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListTests`: SuccessEnvelope
	fmt.Fprintf(os.Stdout, "Response from `TestsAPI.ListTests`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiListTestsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int32** | 1-based page number. | [default to 1]
 **limit** | **int32** | Items per page (max 100). | [default to 20]
 **search** | **string** | Free-text search filter. | 

### Return type

[**SuccessEnvelope**](SuccessEnvelope.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## RollbackTestVersion

> SuccessEnvelope RollbackTestVersion(ctx, id, versionId).Execute()

Roll a test back to a specific version

### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
	openapiclient "github.com/elev8er/elev8er-go-sdk"
)

func main() {
	id := "id_example" // string | 
	versionId := "versionId_example" // string | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.TestsAPI.RollbackTestVersion(context.Background(), id, versionId).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `TestsAPI.RollbackTestVersion``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `RollbackTestVersion`: SuccessEnvelope
	fmt.Fprintf(os.Stdout, "Response from `TestsAPI.RollbackTestVersion`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** |  | 
**versionId** | **string** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiRollbackTestVersionRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------



### Return type

[**SuccessEnvelope**](SuccessEnvelope.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## UpdateTest

> SuccessEnvelope UpdateTest(ctx, id).RequestBody(requestBody).Execute()

Update a test

### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
	openapiclient "github.com/elev8er/elev8er-go-sdk"
)

func main() {
	id := "id_example" // string | 
	requestBody := map[string]interface{}{"key": interface{}(123)} // map[string]interface{} | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.TestsAPI.UpdateTest(context.Background(), id).RequestBody(requestBody).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `TestsAPI.UpdateTest``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `UpdateTest`: SuccessEnvelope
	fmt.Fprintf(os.Stdout, "Response from `TestsAPI.UpdateTest`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiUpdateTestRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **requestBody** | **map[string]interface{}** |  | 

### Return type

[**SuccessEnvelope**](SuccessEnvelope.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## UpdateTestVersion

> SuccessEnvelope UpdateTestVersion(ctx, id, versionId).Body(body).Execute()

Update a specific test version

### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
	openapiclient "github.com/elev8er/elev8er-go-sdk"
)

func main() {
	id := "id_example" // string | 
	versionId := "versionId_example" // string | 
	body := map[string]interface{}{ ... } // map[string]interface{} | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.TestsAPI.UpdateTestVersion(context.Background(), id, versionId).Body(body).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `TestsAPI.UpdateTestVersion``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `UpdateTestVersion`: SuccessEnvelope
	fmt.Fprintf(os.Stdout, "Response from `TestsAPI.UpdateTestVersion`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** |  | 
**versionId** | **string** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiUpdateTestVersionRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **body** | **map[string]interface{}** |  | 

### Return type

[**SuccessEnvelope**](SuccessEnvelope.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)

