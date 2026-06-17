# SuccessEnvelope

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Success** | **bool** |  | 
**Message** | Pointer to **string** |  | [optional] 
**Data** | Pointer to **interface{}** |  | [optional] 

## Methods

### NewSuccessEnvelope

`func NewSuccessEnvelope(success bool, ) *SuccessEnvelope`

NewSuccessEnvelope instantiates a new SuccessEnvelope object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewSuccessEnvelopeWithDefaults

`func NewSuccessEnvelopeWithDefaults() *SuccessEnvelope`

NewSuccessEnvelopeWithDefaults instantiates a new SuccessEnvelope object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetSuccess

`func (o *SuccessEnvelope) GetSuccess() bool`

GetSuccess returns the Success field if non-nil, zero value otherwise.

### GetSuccessOk

`func (o *SuccessEnvelope) GetSuccessOk() (*bool, bool)`

GetSuccessOk returns a tuple with the Success field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSuccess

`func (o *SuccessEnvelope) SetSuccess(v bool)`

SetSuccess sets Success field to given value.


### GetMessage

`func (o *SuccessEnvelope) GetMessage() string`

GetMessage returns the Message field if non-nil, zero value otherwise.

### GetMessageOk

`func (o *SuccessEnvelope) GetMessageOk() (*string, bool)`

GetMessageOk returns a tuple with the Message field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMessage

`func (o *SuccessEnvelope) SetMessage(v string)`

SetMessage sets Message field to given value.

### HasMessage

`func (o *SuccessEnvelope) HasMessage() bool`

HasMessage returns a boolean if a field has been set.

### GetData

`func (o *SuccessEnvelope) GetData() interface{}`

GetData returns the Data field if non-nil, zero value otherwise.

### GetDataOk

`func (o *SuccessEnvelope) GetDataOk() (*interface{}, bool)`

GetDataOk returns a tuple with the Data field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetData

`func (o *SuccessEnvelope) SetData(v interface{})`

SetData sets Data field to given value.

### HasData

`func (o *SuccessEnvelope) HasData() bool`

HasData returns a boolean if a field has been set.

### SetDataNil

`func (o *SuccessEnvelope) SetDataNil(b bool)`

 SetDataNil sets the value for Data to be an explicit nil

### UnsetData
`func (o *SuccessEnvelope) UnsetData()`

UnsetData ensures that no value is present for Data, not even an explicit nil

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


