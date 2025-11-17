# DtoUpdateRecordSetRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | Pointer to **string** | Any change flips status back to pending (worker will UPSERT) | [optional] 
**Status** | Pointer to **string** |  | [optional] 
**Ttl** | Pointer to **int32** |  | [optional] 
**Type** | Pointer to **string** |  | [optional] 
**Values** | Pointer to **[]string** |  | [optional] 

## Methods

### NewDtoUpdateRecordSetRequest

`func NewDtoUpdateRecordSetRequest() *DtoUpdateRecordSetRequest`

NewDtoUpdateRecordSetRequest instantiates a new DtoUpdateRecordSetRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewDtoUpdateRecordSetRequestWithDefaults

`func NewDtoUpdateRecordSetRequestWithDefaults() *DtoUpdateRecordSetRequest`

NewDtoUpdateRecordSetRequestWithDefaults instantiates a new DtoUpdateRecordSetRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetName

`func (o *DtoUpdateRecordSetRequest) GetName() string`

GetName returns the Name field if non-nil, zero value otherwise.

### GetNameOk

`func (o *DtoUpdateRecordSetRequest) GetNameOk() (*string, bool)`

GetNameOk returns a tuple with the Name field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetName

`func (o *DtoUpdateRecordSetRequest) SetName(v string)`

SetName sets Name field to given value.

### HasName

`func (o *DtoUpdateRecordSetRequest) HasName() bool`

HasName returns a boolean if a field has been set.

### GetStatus

`func (o *DtoUpdateRecordSetRequest) GetStatus() string`

GetStatus returns the Status field if non-nil, zero value otherwise.

### GetStatusOk

`func (o *DtoUpdateRecordSetRequest) GetStatusOk() (*string, bool)`

GetStatusOk returns a tuple with the Status field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetStatus

`func (o *DtoUpdateRecordSetRequest) SetStatus(v string)`

SetStatus sets Status field to given value.

### HasStatus

`func (o *DtoUpdateRecordSetRequest) HasStatus() bool`

HasStatus returns a boolean if a field has been set.

### GetTtl

`func (o *DtoUpdateRecordSetRequest) GetTtl() int32`

GetTtl returns the Ttl field if non-nil, zero value otherwise.

### GetTtlOk

`func (o *DtoUpdateRecordSetRequest) GetTtlOk() (*int32, bool)`

GetTtlOk returns a tuple with the Ttl field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTtl

`func (o *DtoUpdateRecordSetRequest) SetTtl(v int32)`

SetTtl sets Ttl field to given value.

### HasTtl

`func (o *DtoUpdateRecordSetRequest) HasTtl() bool`

HasTtl returns a boolean if a field has been set.

### GetType

`func (o *DtoUpdateRecordSetRequest) GetType() string`

GetType returns the Type field if non-nil, zero value otherwise.

### GetTypeOk

`func (o *DtoUpdateRecordSetRequest) GetTypeOk() (*string, bool)`

GetTypeOk returns a tuple with the Type field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetType

`func (o *DtoUpdateRecordSetRequest) SetType(v string)`

SetType sets Type field to given value.

### HasType

`func (o *DtoUpdateRecordSetRequest) HasType() bool`

HasType returns a boolean if a field has been set.

### GetValues

`func (o *DtoUpdateRecordSetRequest) GetValues() []string`

GetValues returns the Values field if non-nil, zero value otherwise.

### GetValuesOk

`func (o *DtoUpdateRecordSetRequest) GetValuesOk() (*[]string, bool)`

GetValuesOk returns a tuple with the Values field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetValues

`func (o *DtoUpdateRecordSetRequest) SetValues(v []string)`

SetValues sets Values field to given value.

### HasValues

`func (o *DtoUpdateRecordSetRequest) HasValues() bool`

HasValues returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


