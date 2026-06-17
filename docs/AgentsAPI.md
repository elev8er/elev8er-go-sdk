# \AgentsAPI

All URIs are relative to *https://apidev.elev8er.ai/public/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**CreateAgentChat**](AgentsAPI.md#CreateAgentChat) | **Post** /agents/{id}/chats | Start a new chat with an agent
[**GetAgent**](AgentsAPI.md#GetAgent) | **Get** /agents/{id} | Get an agent by id
[**ListAgentChats**](AgentsAPI.md#ListAgentChats) | **Get** /agents/{id}/chats | List chats for an agent
[**ListAgents**](AgentsAPI.md#ListAgents) | **Get** /agents | List agents
[**ListChatMessages**](AgentsAPI.md#ListChatMessages) | **Get** /agents/{id}/chats/{chatId}/messages | Get messages in a chat
[**SendChatMessage**](AgentsAPI.md#SendChatMessage) | **Post** /agents/{id}/chats/{chatId}/messages | Send a message to the agent and get its reply (non-streaming)



## CreateAgentChat

> SuccessEnvelope CreateAgentChat(ctx, id).CreateAgentChatRequest(createAgentChatRequest).Execute()

Start a new chat with an agent

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
	createAgentChatRequest := *openapiclient.NewCreateAgentChatRequest() // CreateAgentChatRequest |  (optional)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.AgentsAPI.CreateAgentChat(context.Background(), id).CreateAgentChatRequest(createAgentChatRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `AgentsAPI.CreateAgentChat``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `CreateAgentChat`: SuccessEnvelope
	fmt.Fprintf(os.Stdout, "Response from `AgentsAPI.CreateAgentChat`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiCreateAgentChatRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **createAgentChatRequest** | [**CreateAgentChatRequest**](CreateAgentChatRequest.md) |  | 

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


## GetAgent

> SuccessEnvelope GetAgent(ctx, id).Execute()

Get an agent by id

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
	resp, r, err := apiClient.AgentsAPI.GetAgent(context.Background(), id).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `AgentsAPI.GetAgent``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetAgent`: SuccessEnvelope
	fmt.Fprintf(os.Stdout, "Response from `AgentsAPI.GetAgent`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetAgentRequest struct via the builder pattern


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


## ListAgentChats

> SuccessEnvelope ListAgentChats(ctx, id).Execute()

List chats for an agent

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
	resp, r, err := apiClient.AgentsAPI.ListAgentChats(context.Background(), id).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `AgentsAPI.ListAgentChats``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListAgentChats`: SuccessEnvelope
	fmt.Fprintf(os.Stdout, "Response from `AgentsAPI.ListAgentChats`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiListAgentChatsRequest struct via the builder pattern


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


## ListAgents

> SuccessEnvelope ListAgents(ctx).Page(page).Limit(limit).Execute()

List agents

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
	resp, r, err := apiClient.AgentsAPI.ListAgents(context.Background()).Page(page).Limit(limit).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `AgentsAPI.ListAgents``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListAgents`: SuccessEnvelope
	fmt.Fprintf(os.Stdout, "Response from `AgentsAPI.ListAgents`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiListAgentsRequest struct via the builder pattern


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


## ListChatMessages

> SuccessEnvelope ListChatMessages(ctx, id, chatId).Page(page).Limit(limit).Execute()

Get messages in a chat

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
	chatId := "chatId_example" // string | 
	page := int32(56) // int32 | 1-based page number. (optional) (default to 1)
	limit := int32(56) // int32 | Items per page (max 100). (optional) (default to 20)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.AgentsAPI.ListChatMessages(context.Background(), id, chatId).Page(page).Limit(limit).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `AgentsAPI.ListChatMessages``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListChatMessages`: SuccessEnvelope
	fmt.Fprintf(os.Stdout, "Response from `AgentsAPI.ListChatMessages`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** |  | 
**chatId** | **string** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiListChatMessagesRequest struct via the builder pattern


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


## SendChatMessage

> SuccessEnvelope SendChatMessage(ctx, id, chatId).ChatMessageInput(chatMessageInput).Execute()

Send a message to the agent and get its reply (non-streaming)



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
	chatId := "chatId_example" // string | 
	chatMessageInput := *openapiclient.NewChatMessageInput("Message_example") // ChatMessageInput | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.AgentsAPI.SendChatMessage(context.Background(), id, chatId).ChatMessageInput(chatMessageInput).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `AgentsAPI.SendChatMessage``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `SendChatMessage`: SuccessEnvelope
	fmt.Fprintf(os.Stdout, "Response from `AgentsAPI.SendChatMessage`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** |  | 
**chatId** | **string** |  | 

### Other Parameters

Other parameters are passed through a pointer to a apiSendChatMessageRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **chatMessageInput** | [**ChatMessageInput**](ChatMessageInput.md) |  | 

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

