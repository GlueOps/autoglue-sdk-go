# DtoCreateRecordSetRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** | Name relative to domain (\&quot;endpoint\&quot;) OR FQDN (\&quot;endpoint.example.com\&quot;). Server normalizes to relative. | 
**Ttl** | Pointer to **int32** |  | [optional] 
**Type** | **string** |  | 
**Values** | Pointer to **[]string** |  | [optional] 

## Methods

### NewDtoCreateRecordSetRequest

`func NewDtoCreateRecordSetRequest(name string, type_ string, ) *DtoCreateRecordSetRequest`

NewDtoCreateRecordSetRequest instantiates a new DtoCreateRecordSetRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewDtoCreateRecordSetRequestWithDefaults

`func NewDtoCreateRecordSetRequestWithDefaults() *DtoCreateRecordSetRequest`

NewDtoCreateRecordSetRequestWithDefaults instantiates a new DtoCreateRecordSetRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetName

`func (o *DtoCreateRecordSetRequest) GetName() string`

GetName returns the Name field if non-nil, zero value otherwise.

### GetNameOk

`func (o *DtoCreateRecordSetRequest) GetNameOk() (*string, bool)`

GetNameOk returns a tuple with the Name field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetName

`func (o *DtoCreateRecordSetRequest) SetName(v string)`

SetName sets Name field to given value.


### GetTtl

`func (o *DtoCreateRecordSetRequest) GetTtl() int32`

GetTtl returns the Ttl field if non-nil, zero value otherwise.

### GetTtlOk

`func (o *DtoCreateRecordSetRequest) GetTtlOk() (*int32, bool)`

GetTtlOk returns a tuple with the Ttl field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTtl

`func (o *DtoCreateRecordSetRequest) SetTtl(v int32)`

SetTtl sets Ttl field to given value.

### HasTtl

`func (o *DtoCreateRecordSetRequest) HasTtl() bool`

HasTtl returns a boolean if a field has been set.

### GetType

`func (o *DtoCreateRecordSetRequest) GetType() string`

GetType returns the Type field if non-nil, zero value otherwise.

### GetTypeOk

`func (o *DtoCreateRecordSetRequest) GetTypeOk() (*string, bool)`

GetTypeOk returns a tuple with the Type field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetType

`func (o *DtoCreateRecordSetRequest) SetType(v string)`

SetType sets Type field to given value.


### GetValues

`func (o *DtoCreateRecordSetRequest) GetValues() []string`

GetValues returns the Values field if non-nil, zero value otherwise.

### GetValuesOk

`func (o *DtoCreateRecordSetRequest) GetValuesOk() (*[]string, bool)`

GetValuesOk returns a tuple with the Values field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetValues

`func (o *DtoCreateRecordSetRequest) SetValues(v []string)`

SetValues sets Values field to given value.

### HasValues

`func (o *DtoCreateRecordSetRequest) HasValues() bool`

HasValues returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


