# DtoRecordSetResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CreatedAt** | Pointer to **string** |  | [optional] 
**DomainId** | Pointer to **string** |  | [optional] 
**Fingerprint** | Pointer to **string** |  | [optional] 
**Id** | Pointer to **string** |  | [optional] 
**LastError** | Pointer to **string** |  | [optional] 
**Name** | Pointer to **string** |  | [optional] 
**Owner** | Pointer to **string** |  | [optional] 
**Status** | Pointer to **string** |  | [optional] 
**Ttl** | Pointer to **int32** |  | [optional] 
**Type** | Pointer to **string** |  | [optional] 
**UpdatedAt** | Pointer to **string** |  | [optional] 
**Values** | Pointer to **map[string]interface{}** | []string JSON | [optional] 

## Methods

### NewDtoRecordSetResponse

`func NewDtoRecordSetResponse() *DtoRecordSetResponse`

NewDtoRecordSetResponse instantiates a new DtoRecordSetResponse object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewDtoRecordSetResponseWithDefaults

`func NewDtoRecordSetResponseWithDefaults() *DtoRecordSetResponse`

NewDtoRecordSetResponseWithDefaults instantiates a new DtoRecordSetResponse object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetCreatedAt

`func (o *DtoRecordSetResponse) GetCreatedAt() string`

GetCreatedAt returns the CreatedAt field if non-nil, zero value otherwise.

### GetCreatedAtOk

`func (o *DtoRecordSetResponse) GetCreatedAtOk() (*string, bool)`

GetCreatedAtOk returns a tuple with the CreatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCreatedAt

`func (o *DtoRecordSetResponse) SetCreatedAt(v string)`

SetCreatedAt sets CreatedAt field to given value.

### HasCreatedAt

`func (o *DtoRecordSetResponse) HasCreatedAt() bool`

HasCreatedAt returns a boolean if a field has been set.

### GetDomainId

`func (o *DtoRecordSetResponse) GetDomainId() string`

GetDomainId returns the DomainId field if non-nil, zero value otherwise.

### GetDomainIdOk

`func (o *DtoRecordSetResponse) GetDomainIdOk() (*string, bool)`

GetDomainIdOk returns a tuple with the DomainId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDomainId

`func (o *DtoRecordSetResponse) SetDomainId(v string)`

SetDomainId sets DomainId field to given value.

### HasDomainId

`func (o *DtoRecordSetResponse) HasDomainId() bool`

HasDomainId returns a boolean if a field has been set.

### GetFingerprint

`func (o *DtoRecordSetResponse) GetFingerprint() string`

GetFingerprint returns the Fingerprint field if non-nil, zero value otherwise.

### GetFingerprintOk

`func (o *DtoRecordSetResponse) GetFingerprintOk() (*string, bool)`

GetFingerprintOk returns a tuple with the Fingerprint field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetFingerprint

`func (o *DtoRecordSetResponse) SetFingerprint(v string)`

SetFingerprint sets Fingerprint field to given value.

### HasFingerprint

`func (o *DtoRecordSetResponse) HasFingerprint() bool`

HasFingerprint returns a boolean if a field has been set.

### GetId

`func (o *DtoRecordSetResponse) GetId() string`

GetId returns the Id field if non-nil, zero value otherwise.

### GetIdOk

`func (o *DtoRecordSetResponse) GetIdOk() (*string, bool)`

GetIdOk returns a tuple with the Id field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetId

`func (o *DtoRecordSetResponse) SetId(v string)`

SetId sets Id field to given value.

### HasId

`func (o *DtoRecordSetResponse) HasId() bool`

HasId returns a boolean if a field has been set.

### GetLastError

`func (o *DtoRecordSetResponse) GetLastError() string`

GetLastError returns the LastError field if non-nil, zero value otherwise.

### GetLastErrorOk

`func (o *DtoRecordSetResponse) GetLastErrorOk() (*string, bool)`

GetLastErrorOk returns a tuple with the LastError field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetLastError

`func (o *DtoRecordSetResponse) SetLastError(v string)`

SetLastError sets LastError field to given value.

### HasLastError

`func (o *DtoRecordSetResponse) HasLastError() bool`

HasLastError returns a boolean if a field has been set.

### GetName

`func (o *DtoRecordSetResponse) GetName() string`

GetName returns the Name field if non-nil, zero value otherwise.

### GetNameOk

`func (o *DtoRecordSetResponse) GetNameOk() (*string, bool)`

GetNameOk returns a tuple with the Name field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetName

`func (o *DtoRecordSetResponse) SetName(v string)`

SetName sets Name field to given value.

### HasName

`func (o *DtoRecordSetResponse) HasName() bool`

HasName returns a boolean if a field has been set.

### GetOwner

`func (o *DtoRecordSetResponse) GetOwner() string`

GetOwner returns the Owner field if non-nil, zero value otherwise.

### GetOwnerOk

`func (o *DtoRecordSetResponse) GetOwnerOk() (*string, bool)`

GetOwnerOk returns a tuple with the Owner field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetOwner

`func (o *DtoRecordSetResponse) SetOwner(v string)`

SetOwner sets Owner field to given value.

### HasOwner

`func (o *DtoRecordSetResponse) HasOwner() bool`

HasOwner returns a boolean if a field has been set.

### GetStatus

`func (o *DtoRecordSetResponse) GetStatus() string`

GetStatus returns the Status field if non-nil, zero value otherwise.

### GetStatusOk

`func (o *DtoRecordSetResponse) GetStatusOk() (*string, bool)`

GetStatusOk returns a tuple with the Status field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetStatus

`func (o *DtoRecordSetResponse) SetStatus(v string)`

SetStatus sets Status field to given value.

### HasStatus

`func (o *DtoRecordSetResponse) HasStatus() bool`

HasStatus returns a boolean if a field has been set.

### GetTtl

`func (o *DtoRecordSetResponse) GetTtl() int32`

GetTtl returns the Ttl field if non-nil, zero value otherwise.

### GetTtlOk

`func (o *DtoRecordSetResponse) GetTtlOk() (*int32, bool)`

GetTtlOk returns a tuple with the Ttl field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTtl

`func (o *DtoRecordSetResponse) SetTtl(v int32)`

SetTtl sets Ttl field to given value.

### HasTtl

`func (o *DtoRecordSetResponse) HasTtl() bool`

HasTtl returns a boolean if a field has been set.

### GetType

`func (o *DtoRecordSetResponse) GetType() string`

GetType returns the Type field if non-nil, zero value otherwise.

### GetTypeOk

`func (o *DtoRecordSetResponse) GetTypeOk() (*string, bool)`

GetTypeOk returns a tuple with the Type field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetType

`func (o *DtoRecordSetResponse) SetType(v string)`

SetType sets Type field to given value.

### HasType

`func (o *DtoRecordSetResponse) HasType() bool`

HasType returns a boolean if a field has been set.

### GetUpdatedAt

`func (o *DtoRecordSetResponse) GetUpdatedAt() string`

GetUpdatedAt returns the UpdatedAt field if non-nil, zero value otherwise.

### GetUpdatedAtOk

`func (o *DtoRecordSetResponse) GetUpdatedAtOk() (*string, bool)`

GetUpdatedAtOk returns a tuple with the UpdatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUpdatedAt

`func (o *DtoRecordSetResponse) SetUpdatedAt(v string)`

SetUpdatedAt sets UpdatedAt field to given value.

### HasUpdatedAt

`func (o *DtoRecordSetResponse) HasUpdatedAt() bool`

HasUpdatedAt returns a boolean if a field has been set.

### GetValues

`func (o *DtoRecordSetResponse) GetValues() map[string]interface{}`

GetValues returns the Values field if non-nil, zero value otherwise.

### GetValuesOk

`func (o *DtoRecordSetResponse) GetValuesOk() (*map[string]interface{}, bool)`

GetValuesOk returns a tuple with the Values field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetValues

`func (o *DtoRecordSetResponse) SetValues(v map[string]interface{})`

SetValues sets Values field to given value.

### HasValues

`func (o *DtoRecordSetResponse) HasValues() bool`

HasValues returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


