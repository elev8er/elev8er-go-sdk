# ListPrograms200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Success** | **bool** |  | 
**Message** | Pointer to **string** |  | [optional] 
**Data** | Pointer to **interface{}** |  | [optional] 
**Pagination** | Pointer to [**Pagination**](Pagination.md) |  | [optional] 

## Methods

### NewListPrograms200Response

`func NewListPrograms200Response(success bool, ) *ListPrograms200Response`

NewListPrograms200Response instantiates a new ListPrograms200Response object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewListPrograms200ResponseWithDefaults

`func NewListPrograms200ResponseWithDefaults() *ListPrograms200Response`

NewListPrograms200ResponseWithDefaults instantiates a new ListPrograms200Response object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetSuccess

`func (o *ListPrograms200Response) GetSuccess() bool`

GetSuccess returns the Success field if non-nil, zero value otherwise.

### GetSuccessOk

`func (o *ListPrograms200Response) GetSuccessOk() (*bool, bool)`

GetSuccessOk returns a tuple with the Success field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSuccess

`func (o *ListPrograms200Response) SetSuccess(v bool)`

SetSuccess sets Success field to given value.


### GetMessage

`func (o *ListPrograms200Response) GetMessage() string`

GetMessage returns the Message field if non-nil, zero value otherwise.

### GetMessageOk

`func (o *ListPrograms200Response) GetMessageOk() (*string, bool)`

GetMessageOk returns a tuple with the Message field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMessage

`func (o *ListPrograms200Response) SetMessage(v string)`

SetMessage sets Message field to given value.

### HasMessage

`func (o *ListPrograms200Response) HasMessage() bool`

HasMessage returns a boolean if a field has been set.

### GetData

`func (o *ListPrograms200Response) GetData() interface{}`

GetData returns the Data field if non-nil, zero value otherwise.

### GetDataOk

`func (o *ListPrograms200Response) GetDataOk() (*interface{}, bool)`

GetDataOk returns a tuple with the Data field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetData

`func (o *ListPrograms200Response) SetData(v interface{})`

SetData sets Data field to given value.

### HasData

`func (o *ListPrograms200Response) HasData() bool`

HasData returns a boolean if a field has been set.

### SetDataNil

`func (o *ListPrograms200Response) SetDataNil(b bool)`

 SetDataNil sets the value for Data to be an explicit nil

### UnsetData
`func (o *ListPrograms200Response) UnsetData()`

UnsetData ensures that no value is present for Data, not even an explicit nil
### GetPagination

`func (o *ListPrograms200Response) GetPagination() Pagination`

GetPagination returns the Pagination field if non-nil, zero value otherwise.

### GetPaginationOk

`func (o *ListPrograms200Response) GetPaginationOk() (*Pagination, bool)`

GetPaginationOk returns a tuple with the Pagination field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPagination

`func (o *ListPrograms200Response) SetPagination(v Pagination)`

SetPagination sets Pagination field to given value.

### HasPagination

`func (o *ListPrograms200Response) HasPagination() bool`

HasPagination returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


