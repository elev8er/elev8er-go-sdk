# \VisualTestsAPI

All URIs are relative to *https://apidev.elev8er.ai/public/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**CreateVisualTest**](VisualTestsAPI.md#CreateVisualTest) | **Post** /visual-tests | Create a visual test
[**CreateVisualTestVersion**](VisualTestsAPI.md#CreateVisualTestVersion) | **Post** /visual-tests/{id}/versions | Create a new version of a visual test
[**DeleteVisualTest**](VisualTestsAPI.md#DeleteVisualTest) | **Delete** /visual-tests/{id} | Delete a visual test
[**GetVisualTest**](VisualTestsAPI.md#GetVisualTest) | **Get** /visual-tests/{id} | Get a visual test by id
[**GetVisualTestVersion**](VisualTestsAPI.md#GetVisualTestVersion) | **Get** /visual-tests/{id}/versions/{versionId} | Get a specific visual test version
[**ListVisualTestVersions**](VisualTestsAPI.md#ListVisualTestVersions) | **Get** /visual-tests/{id}/versions | List versions of a visual test
[**ListVisualTests**](VisualTestsAPI.md#ListVisualTests) | **Get** /visual-tests | List visual tests
[**RollbackVisualTestVersion**](VisualTestsAPI.md#RollbackVisualTestVersion) | **Post** /visual-tests/{id}/versions/{versionId}/rollback | Roll a visual test back to a specific version
[**UpdateVisualTest**](VisualTestsAPI.md#UpdateVisualTest) | **Put** /visual-tests/{id} | Update a visual test
[**UpdateVisualTestVersion**](VisualTestsAPI.md#UpdateVisualTestVersion) | **Put** /visual-tests/{id}/versions/{versionId} | Update a specific visual test version



## CreateVisualTest

> SuccessEnvelope CreateVisualTest(ctx).RequestBody(requestBody).Execute()

Create a visual test

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
	resp, r, err := apiClient.VisualTestsAPI.CreateVisualTest(context.Background()).RequestBody(requestBody).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `VisualTestsAPI.CreateVisualTest``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `CreateVisualTest`: SuccessEnvelope
	fmt.Fprintf(os.Stdout, "Response from `VisualTestsAPI.CreateVisualTest`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiCreateVisualTestRequest struct via the builder pattern


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


## CreateVisualTestVersion

> SuccessEnvelope CreateVisualTestVersion(ctx, id).Body(body).Execute()

Create a new version of a visual test

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
	resp, r, err := apiClient.VisualTestsAPI.CreateVisualTestVersion(context.Background(), id).Body(body).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `VisualTestsAPI.CreateVisualTestVersion``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `CreateVisualTestVersion`: SuccessEnvelope
	fmt.Fprintf(os.Stdout, "Response from `VisualTestsAPI.CreateVisualTestVersion`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiCreateVisualTestVersionRequest struct via the builder pattern


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


## DeleteVisualTest

> DeleteVisualTest(ctx, id).Execute()

Delete a visual test

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
	r, err := apiClient.VisualTestsAPI.DeleteVisualTest(context.Background(), id).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `VisualTestsAPI.DeleteVisualTest``: %v\n", err)
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

Other parameters are passed through a pointer to a apiDeleteVisualTestRequest struct via the builder pattern


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


## GetVisualTest

> SuccessEnvelope GetVisualTest(ctx, id).Execute()

Get a visual test by id

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
	resp, r, err := apiClient.VisualTestsAPI.GetVisualTest(context.Background(), id).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `VisualTestsAPI.GetVisualTest``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetVisualTest`: SuccessEnvelope
	fmt.Fprintf(os.Stdout, "Response from `VisualTestsAPI.GetVisualTest`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetVisualTestRequest struct via the builder pattern


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


## GetVisualTestVersion

> SuccessEnvelope GetVisualTestVersion(ctx, id, versionId).Execute()

Get a specific visual test version

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
	resp, r, err := apiClient.VisualTestsAPI.GetVisualTestVersion(context.Background(), id, versionId).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `VisualTestsAPI.GetVisualTestVersion``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetVisualTestVersion`: SuccessEnvelope
	fmt.Fprintf(os.Stdout, "Response from `VisualTestsAPI.GetVisualTestVersion`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** |  | 
**versionId** | **string** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetVisualTestVersionRequest struct via the builder pattern


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


## ListVisualTestVersions

> SuccessEnvelope ListVisualTestVersions(ctx, id).Execute()

List versions of a visual test

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
	resp, r, err := apiClient.VisualTestsAPI.ListVisualTestVersions(context.Background(), id).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `VisualTestsAPI.ListVisualTestVersions``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListVisualTestVersions`: SuccessEnvelope
	fmt.Fprintf(os.Stdout, "Response from `VisualTestsAPI.ListVisualTestVersions`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiListVisualTestVersionsRequest struct via the builder pattern


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


## ListVisualTests

> SuccessEnvelope ListVisualTests(ctx).Page(page).Limit(limit).Search(search).Execute()

List visual tests

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
	resp, r, err := apiClient.VisualTestsAPI.ListVisualTests(context.Background()).Page(page).Limit(limit).Search(search).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `VisualTestsAPI.ListVisualTests``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListVisualTests`: SuccessEnvelope
	fmt.Fprintf(os.Stdout, "Response from `VisualTestsAPI.ListVisualTests`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiListVisualTestsRequest struct via the builder pattern


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


## RollbackVisualTestVersion

> SuccessEnvelope RollbackVisualTestVersion(ctx, id, versionId).Execute()

Roll a visual test back to a specific version

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
	resp, r, err := apiClient.VisualTestsAPI.RollbackVisualTestVersion(context.Background(), id, versionId).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `VisualTestsAPI.RollbackVisualTestVersion``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `RollbackVisualTestVersion`: SuccessEnvelope
	fmt.Fprintf(os.Stdout, "Response from `VisualTestsAPI.RollbackVisualTestVersion`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** |  | 
**versionId** | **string** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiRollbackVisualTestVersionRequest struct via the builder pattern


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


## UpdateVisualTest

> SuccessEnvelope UpdateVisualTest(ctx, id).RequestBody(requestBody).Execute()

Update a visual test

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
	resp, r, err := apiClient.VisualTestsAPI.UpdateVisualTest(context.Background(), id).RequestBody(requestBody).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `VisualTestsAPI.UpdateVisualTest``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `UpdateVisualTest`: SuccessEnvelope
	fmt.Fprintf(os.Stdout, "Response from `VisualTestsAPI.UpdateVisualTest`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiUpdateVisualTestRequest struct via the builder pattern


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


## UpdateVisualTestVersion

> SuccessEnvelope UpdateVisualTestVersion(ctx, id, versionId).Body(body).Execute()

Update a specific visual test version

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
	resp, r, err := apiClient.VisualTestsAPI.UpdateVisualTestVersion(context.Background(), id, versionId).Body(body).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `VisualTestsAPI.UpdateVisualTestVersion``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `UpdateVisualTestVersion`: SuccessEnvelope
	fmt.Fprintf(os.Stdout, "Response from `VisualTestsAPI.UpdateVisualTestVersion`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** |  | 
**versionId** | **string** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiUpdateVisualTestVersionRequest struct via the builder pattern


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

