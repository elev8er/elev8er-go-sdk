# \BlogsAPI

All URIs are relative to *https://apidev.elev8er.ai/public/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**CreateBlog**](BlogsAPI.md#CreateBlog) | **Post** /blogs | Create a blog
[**DeleteBlog**](BlogsAPI.md#DeleteBlog) | **Delete** /blogs/{id} | Delete a blog
[**GetBlog**](BlogsAPI.md#GetBlog) | **Get** /blogs/{id} | Get a blog by id
[**ListBlogs**](BlogsAPI.md#ListBlogs) | **Get** /blogs | List blogs
[**UpdateBlog**](BlogsAPI.md#UpdateBlog) | **Put** /blogs/{id} | Update a blog



## CreateBlog

> SuccessEnvelope CreateBlog(ctx).RequestBody(requestBody).Execute()

Create a blog

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
	resp, r, err := apiClient.BlogsAPI.CreateBlog(context.Background()).RequestBody(requestBody).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `BlogsAPI.CreateBlog``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `CreateBlog`: SuccessEnvelope
	fmt.Fprintf(os.Stdout, "Response from `BlogsAPI.CreateBlog`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiCreateBlogRequest struct via the builder pattern


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


## DeleteBlog

> DeleteBlog(ctx, id).Execute()

Delete a blog

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
	r, err := apiClient.BlogsAPI.DeleteBlog(context.Background(), id).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `BlogsAPI.DeleteBlog``: %v\n", err)
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

Other parameters are passed through a pointer to a apiDeleteBlogRequest struct via the builder pattern


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


## GetBlog

> SuccessEnvelope GetBlog(ctx, id).Execute()

Get a blog by id

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
	resp, r, err := apiClient.BlogsAPI.GetBlog(context.Background(), id).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `BlogsAPI.GetBlog``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetBlog`: SuccessEnvelope
	fmt.Fprintf(os.Stdout, "Response from `BlogsAPI.GetBlog`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetBlogRequest struct via the builder pattern


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


## ListBlogs

> SuccessEnvelope ListBlogs(ctx).Page(page).Limit(limit).Search(search).Execute()

List blogs

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
	resp, r, err := apiClient.BlogsAPI.ListBlogs(context.Background()).Page(page).Limit(limit).Search(search).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `BlogsAPI.ListBlogs``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListBlogs`: SuccessEnvelope
	fmt.Fprintf(os.Stdout, "Response from `BlogsAPI.ListBlogs`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiListBlogsRequest struct via the builder pattern


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


## UpdateBlog

> SuccessEnvelope UpdateBlog(ctx, id).RequestBody(requestBody).Execute()

Update a blog

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
	resp, r, err := apiClient.BlogsAPI.UpdateBlog(context.Background(), id).RequestBody(requestBody).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `BlogsAPI.UpdateBlog``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `UpdateBlog`: SuccessEnvelope
	fmt.Fprintf(os.Stdout, "Response from `BlogsAPI.UpdateBlog`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiUpdateBlogRequest struct via the builder pattern


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

