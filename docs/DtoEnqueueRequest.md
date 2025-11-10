# DtoEnqueueRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Payload** | Pointer to **map[string]interface{}** |  | [optional] 
**Queue** | Pointer to **string** |  | [optional] 
**RunAt** | Pointer to **string** |  | [optional] 
**Type** | Pointer to **string** |  | [optional] 

## Methods

### NewDtoEnqueueRequest

`func NewDtoEnqueueRequest() *DtoEnqueueRequest`

NewDtoEnqueueRequest instantiates a new DtoEnqueueRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewDtoEnqueueRequestWithDefaults

`func NewDtoEnqueueRequestWithDefaults() *DtoEnqueueRequest`

NewDtoEnqueueRequestWithDefaults instantiates a new DtoEnqueueRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetPayload

`func (o *DtoEnqueueRequest) GetPayload() map[string]interface{}`

GetPayload returns the Payload field if non-nil, zero value otherwise.

### GetPayloadOk

`func (o *DtoEnqueueRequest) GetPayloadOk() (*map[string]interface{}, bool)`

GetPayloadOk returns a tuple with the Payload field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPayload

`func (o *DtoEnqueueRequest) SetPayload(v map[string]interface{})`

SetPayload sets Payload field to given value.

### HasPayload

`func (o *DtoEnqueueRequest) HasPayload() bool`

HasPayload returns a boolean if a field has been set.

### GetQueue

`func (o *DtoEnqueueRequest) GetQueue() string`

GetQueue returns the Queue field if non-nil, zero value otherwise.

### GetQueueOk

`func (o *DtoEnqueueRequest) GetQueueOk() (*string, bool)`

GetQueueOk returns a tuple with the Queue field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetQueue

`func (o *DtoEnqueueRequest) SetQueue(v string)`

SetQueue sets Queue field to given value.

### HasQueue

`func (o *DtoEnqueueRequest) HasQueue() bool`

HasQueue returns a boolean if a field has been set.

### GetRunAt

`func (o *DtoEnqueueRequest) GetRunAt() string`

GetRunAt returns the RunAt field if non-nil, zero value otherwise.

### GetRunAtOk

`func (o *DtoEnqueueRequest) GetRunAtOk() (*string, bool)`

GetRunAtOk returns a tuple with the RunAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRunAt

`func (o *DtoEnqueueRequest) SetRunAt(v string)`

SetRunAt sets RunAt field to given value.

### HasRunAt

`func (o *DtoEnqueueRequest) HasRunAt() bool`

HasRunAt returns a boolean if a field has been set.

### GetType

`func (o *DtoEnqueueRequest) GetType() string`

GetType returns the Type field if non-nil, zero value otherwise.

### GetTypeOk

`func (o *DtoEnqueueRequest) GetTypeOk() (*string, bool)`

GetTypeOk returns a tuple with the Type field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetType

`func (o *DtoEnqueueRequest) SetType(v string)`

SetType sets Type field to given value.

### HasType

`func (o *DtoEnqueueRequest) HasType() bool`

HasType returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


