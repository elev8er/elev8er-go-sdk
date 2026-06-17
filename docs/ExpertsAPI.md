# \ExpertsAPI

All URIs are relative to *https://apidev.elev8er.ai/public/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**CreateAvailability**](ExpertsAPI.md#CreateAvailability) | **Post** /experts/availability | Create an availability entry
[**CreateExpert**](ExpertsAPI.md#CreateExpert) | **Post** /experts | Create an expert
[**CreateSession**](ExpertsAPI.md#CreateSession) | **Post** /experts/sessions | Create a session
[**DeleteAvailability**](ExpertsAPI.md#DeleteAvailability) | **Delete** /experts/availability/{id} | Delete an availability entry
[**DeleteExpert**](ExpertsAPI.md#DeleteExpert) | **Delete** /experts/{id} | Delete an expert
[**DeleteSession**](ExpertsAPI.md#DeleteSession) | **Delete** /experts/sessions/{id} | Delete a session
[**GetAvailability**](ExpertsAPI.md#GetAvailability) | **Get** /experts/availability/{id} | Get an availability entry
[**GetExpert**](ExpertsAPI.md#GetExpert) | **Get** /experts/{id} | Get an expert by id
[**GetExpertAvailability**](ExpertsAPI.md#GetExpertAvailability) | **Get** /experts/{expertId}/availability | Get an expert&#39;s availability
[**GetSession**](ExpertsAPI.md#GetSession) | **Get** /experts/sessions/{id} | Get a session
[**ListExpertSessions**](ExpertsAPI.md#ListExpertSessions) | **Get** /experts/{expertId}/sessions | List sessions for an expert
[**ListExperts**](ExpertsAPI.md#ListExperts) | **Get** /experts | List experts
[**ListSessions**](ExpertsAPI.md#ListSessions) | **Get** /experts/sessions | List sessions
[**SetExpertAvailability**](ExpertsAPI.md#SetExpertAvailability) | **Put** /experts/{expertId}/availability | Replace an expert&#39;s availability
[**UpdateAvailability**](ExpertsAPI.md#UpdateAvailability) | **Put** /experts/availability/{id} | Update an availability entry
[**UpdateExpert**](ExpertsAPI.md#UpdateExpert) | **Put** /experts/{id} | Update an expert
[**UpdateSession**](ExpertsAPI.md#UpdateSession) | **Put** /experts/sessions/{id} | Update a session
[**UpdateSessionStatus**](ExpertsAPI.md#UpdateSessionStatus) | **Patch** /experts/sessions/{id}/status | Update a session&#39;s status



## CreateAvailability

> SuccessEnvelope CreateAvailability(ctx).Body(body).Execute()

Create an availability entry

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
	body := map[string]interface{}{ ... } // map[string]interface{} | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.ExpertsAPI.CreateAvailability(context.Background()).Body(body).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ExpertsAPI.CreateAvailability``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `CreateAvailability`: SuccessEnvelope
	fmt.Fprintf(os.Stdout, "Response from `ExpertsAPI.CreateAvailability`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiCreateAvailabilityRequest struct via the builder pattern


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


## CreateExpert

> SuccessEnvelope CreateExpert(ctx).RequestBody(requestBody).Execute()

Create an expert

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
	resp, r, err := apiClient.ExpertsAPI.CreateExpert(context.Background()).RequestBody(requestBody).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ExpertsAPI.CreateExpert``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `CreateExpert`: SuccessEnvelope
	fmt.Fprintf(os.Stdout, "Response from `ExpertsAPI.CreateExpert`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiCreateExpertRequest struct via the builder pattern


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


## CreateSession

> SuccessEnvelope CreateSession(ctx).Body(body).Execute()

Create a session

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
	body := map[string]interface{}{ ... } // map[string]interface{} | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.ExpertsAPI.CreateSession(context.Background()).Body(body).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ExpertsAPI.CreateSession``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `CreateSession`: SuccessEnvelope
	fmt.Fprintf(os.Stdout, "Response from `ExpertsAPI.CreateSession`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiCreateSessionRequest struct via the builder pattern


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


## DeleteAvailability

> DeleteAvailability(ctx, id).Execute()

Delete an availability entry

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
	r, err := apiClient.ExpertsAPI.DeleteAvailability(context.Background(), id).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ExpertsAPI.DeleteAvailability``: %v\n", err)
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

Other parameters are passed through a pointer to a apiDeleteAvailabilityRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


### Return type

 (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## DeleteExpert

> DeleteExpert(ctx, id).Execute()

Delete an expert

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
	r, err := apiClient.ExpertsAPI.DeleteExpert(context.Background(), id).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ExpertsAPI.DeleteExpert``: %v\n", err)
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

Other parameters are passed through a pointer to a apiDeleteExpertRequest struct via the builder pattern


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


## DeleteSession

> DeleteSession(ctx, id).Execute()

Delete a session

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
	r, err := apiClient.ExpertsAPI.DeleteSession(context.Background(), id).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ExpertsAPI.DeleteSession``: %v\n", err)
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

Other parameters are passed through a pointer to a apiDeleteSessionRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


### Return type

 (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetAvailability

> SuccessEnvelope GetAvailability(ctx, id).Execute()

Get an availability entry

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
	resp, r, err := apiClient.ExpertsAPI.GetAvailability(context.Background(), id).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ExpertsAPI.GetAvailability``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetAvailability`: SuccessEnvelope
	fmt.Fprintf(os.Stdout, "Response from `ExpertsAPI.GetAvailability`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetAvailabilityRequest struct via the builder pattern


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


## GetExpert

> SuccessEnvelope GetExpert(ctx, id).Execute()

Get an expert by id

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
	resp, r, err := apiClient.ExpertsAPI.GetExpert(context.Background(), id).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ExpertsAPI.GetExpert``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetExpert`: SuccessEnvelope
	fmt.Fprintf(os.Stdout, "Response from `ExpertsAPI.GetExpert`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetExpertRequest struct via the builder pattern


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


## GetExpertAvailability

> SuccessEnvelope GetExpertAvailability(ctx, expertId).Execute()

Get an expert's availability

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
	expertId := "expertId_example" // string | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.ExpertsAPI.GetExpertAvailability(context.Background(), expertId).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ExpertsAPI.GetExpertAvailability``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetExpertAvailability`: SuccessEnvelope
	fmt.Fprintf(os.Stdout, "Response from `ExpertsAPI.GetExpertAvailability`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**expertId** | **string** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetExpertAvailabilityRequest struct via the builder pattern


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


## GetSession

> SuccessEnvelope GetSession(ctx, id).Execute()

Get a session

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
	resp, r, err := apiClient.ExpertsAPI.GetSession(context.Background(), id).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ExpertsAPI.GetSession``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetSession`: SuccessEnvelope
	fmt.Fprintf(os.Stdout, "Response from `ExpertsAPI.GetSession`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetSessionRequest struct via the builder pattern


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


## ListExpertSessions

> SuccessEnvelope ListExpertSessions(ctx, expertId).Execute()

List sessions for an expert

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
	expertId := "expertId_example" // string | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.ExpertsAPI.ListExpertSessions(context.Background(), expertId).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ExpertsAPI.ListExpertSessions``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListExpertSessions`: SuccessEnvelope
	fmt.Fprintf(os.Stdout, "Response from `ExpertsAPI.ListExpertSessions`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**expertId** | **string** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiListExpertSessionsRequest struct via the builder pattern


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


## ListExperts

> SuccessEnvelope ListExperts(ctx).Page(page).Limit(limit).Search(search).Execute()

List experts

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
	resp, r, err := apiClient.ExpertsAPI.ListExperts(context.Background()).Page(page).Limit(limit).Search(search).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ExpertsAPI.ListExperts``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListExperts`: SuccessEnvelope
	fmt.Fprintf(os.Stdout, "Response from `ExpertsAPI.ListExperts`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiListExpertsRequest struct via the builder pattern


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


## ListSessions

> SuccessEnvelope ListSessions(ctx).Page(page).Limit(limit).Execute()

List sessions

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

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.ExpertsAPI.ListSessions(context.Background()).Page(page).Limit(limit).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ExpertsAPI.ListSessions``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListSessions`: SuccessEnvelope
	fmt.Fprintf(os.Stdout, "Response from `ExpertsAPI.ListSessions`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiListSessionsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int32** | 1-based page number. | [default to 1]
 **limit** | **int32** | Items per page (max 100). | [default to 20]

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


## SetExpertAvailability

> SuccessEnvelope SetExpertAvailability(ctx, expertId).Body(body).Execute()

Replace an expert's availability

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
	expertId := "expertId_example" // string | 
	body := map[string]interface{}{ ... } // map[string]interface{} | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.ExpertsAPI.SetExpertAvailability(context.Background(), expertId).Body(body).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ExpertsAPI.SetExpertAvailability``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `SetExpertAvailability`: SuccessEnvelope
	fmt.Fprintf(os.Stdout, "Response from `ExpertsAPI.SetExpertAvailability`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**expertId** | **string** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiSetExpertAvailabilityRequest struct via the builder pattern


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


## UpdateAvailability

> SuccessEnvelope UpdateAvailability(ctx, id).Body(body).Execute()

Update an availability entry

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
	resp, r, err := apiClient.ExpertsAPI.UpdateAvailability(context.Background(), id).Body(body).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ExpertsAPI.UpdateAvailability``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `UpdateAvailability`: SuccessEnvelope
	fmt.Fprintf(os.Stdout, "Response from `ExpertsAPI.UpdateAvailability`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiUpdateAvailabilityRequest struct via the builder pattern


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


## UpdateExpert

> SuccessEnvelope UpdateExpert(ctx, id).RequestBody(requestBody).Execute()

Update an expert

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
	resp, r, err := apiClient.ExpertsAPI.UpdateExpert(context.Background(), id).RequestBody(requestBody).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ExpertsAPI.UpdateExpert``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `UpdateExpert`: SuccessEnvelope
	fmt.Fprintf(os.Stdout, "Response from `ExpertsAPI.UpdateExpert`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiUpdateExpertRequest struct via the builder pattern


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


## UpdateSession

> SuccessEnvelope UpdateSession(ctx, id).Body(body).Execute()

Update a session

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
	resp, r, err := apiClient.ExpertsAPI.UpdateSession(context.Background(), id).Body(body).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ExpertsAPI.UpdateSession``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `UpdateSession`: SuccessEnvelope
	fmt.Fprintf(os.Stdout, "Response from `ExpertsAPI.UpdateSession`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiUpdateSessionRequest struct via the builder pattern


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


## UpdateSessionStatus

> SuccessEnvelope UpdateSessionStatus(ctx, id).UpdateSessionStatusRequest(updateSessionStatusRequest).Execute()

Update a session's status

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
	updateSessionStatusRequest := *openapiclient.NewUpdateSessionStatusRequest("Status_example") // UpdateSessionStatusRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.ExpertsAPI.UpdateSessionStatus(context.Background(), id).UpdateSessionStatusRequest(updateSessionStatusRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ExpertsAPI.UpdateSessionStatus``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `UpdateSessionStatus`: SuccessEnvelope
	fmt.Fprintf(os.Stdout, "Response from `ExpertsAPI.UpdateSessionStatus`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiUpdateSessionStatusRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **updateSessionStatusRequest** | [**UpdateSessionStatusRequest**](UpdateSessionStatusRequest.md) |  | 

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

