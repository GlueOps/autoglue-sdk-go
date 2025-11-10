# DtoUpdateCredentialRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | Pointer to **string** |  | [optional] 
**Name** | Pointer to **string** |  | [optional] 
**Region** | Pointer to **string** |  | [optional] 
**Scope** | Pointer to **map[string]interface{}** |  | [optional] 
**ScopeKind** | Pointer to **string** |  | [optional] 
**ScopeVersion** | Pointer to **int32** |  | [optional] 
**Secret** | Pointer to **map[string]interface{}** | set if rotating | [optional] 

## Methods

### NewDtoUpdateCredentialRequest

`func NewDtoUpdateCredentialRequest() *DtoUpdateCredentialRequest`

NewDtoUpdateCredentialRequest instantiates a new DtoUpdateCredentialRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewDtoUpdateCredentialRequestWithDefaults

`func NewDtoUpdateCredentialRequestWithDefaults() *DtoUpdateCredentialRequest`

NewDtoUpdateCredentialRequestWithDefaults instantiates a new DtoUpdateCredentialRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetAccountId

`func (o *DtoUpdateCredentialRequest) GetAccountId() string`

GetAccountId returns the AccountId field if non-nil, zero value otherwise.

### GetAccountIdOk

`func (o *DtoUpdateCredentialRequest) GetAccountIdOk() (*string, bool)`

GetAccountIdOk returns a tuple with the AccountId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetAccountId

`func (o *DtoUpdateCredentialRequest) SetAccountId(v string)`

SetAccountId sets AccountId field to given value.

### HasAccountId

`func (o *DtoUpdateCredentialRequest) HasAccountId() bool`

HasAccountId returns a boolean if a field has been set.

### GetName

`func (o *DtoUpdateCredentialRequest) GetName() string`

GetName returns the Name field if non-nil, zero value otherwise.

### GetNameOk

`func (o *DtoUpdateCredentialRequest) GetNameOk() (*string, bool)`

GetNameOk returns a tuple with the Name field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetName

`func (o *DtoUpdateCredentialRequest) SetName(v string)`

SetName sets Name field to given value.

### HasName

`func (o *DtoUpdateCredentialRequest) HasName() bool`

HasName returns a boolean if a field has been set.

### GetRegion

`func (o *DtoUpdateCredentialRequest) GetRegion() string`

GetRegion returns the Region field if non-nil, zero value otherwise.

### GetRegionOk

`func (o *DtoUpdateCredentialRequest) GetRegionOk() (*string, bool)`

GetRegionOk returns a tuple with the Region field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRegion

`func (o *DtoUpdateCredentialRequest) SetRegion(v string)`

SetRegion sets Region field to given value.

### HasRegion

`func (o *DtoUpdateCredentialRequest) HasRegion() bool`

HasRegion returns a boolean if a field has been set.

### GetScope

`func (o *DtoUpdateCredentialRequest) GetScope() map[string]interface{}`

GetScope returns the Scope field if non-nil, zero value otherwise.

### GetScopeOk

`func (o *DtoUpdateCredentialRequest) GetScopeOk() (*map[string]interface{}, bool)`

GetScopeOk returns a tuple with the Scope field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetScope

`func (o *DtoUpdateCredentialRequest) SetScope(v map[string]interface{})`

SetScope sets Scope field to given value.

### HasScope

`func (o *DtoUpdateCredentialRequest) HasScope() bool`

HasScope returns a boolean if a field has been set.

### GetScopeKind

`func (o *DtoUpdateCredentialRequest) GetScopeKind() string`

GetScopeKind returns the ScopeKind field if non-nil, zero value otherwise.

### GetScopeKindOk

`func (o *DtoUpdateCredentialRequest) GetScopeKindOk() (*string, bool)`

GetScopeKindOk returns a tuple with the ScopeKind field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetScopeKind

`func (o *DtoUpdateCredentialRequest) SetScopeKind(v string)`

SetScopeKind sets ScopeKind field to given value.

### HasScopeKind

`func (o *DtoUpdateCredentialRequest) HasScopeKind() bool`

HasScopeKind returns a boolean if a field has been set.

### GetScopeVersion

`func (o *DtoUpdateCredentialRequest) GetScopeVersion() int32`

GetScopeVersion returns the ScopeVersion field if non-nil, zero value otherwise.

### GetScopeVersionOk

`func (o *DtoUpdateCredentialRequest) GetScopeVersionOk() (*int32, bool)`

GetScopeVersionOk returns a tuple with the ScopeVersion field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetScopeVersion

`func (o *DtoUpdateCredentialRequest) SetScopeVersion(v int32)`

SetScopeVersion sets ScopeVersion field to given value.

### HasScopeVersion

`func (o *DtoUpdateCredentialRequest) HasScopeVersion() bool`

HasScopeVersion returns a boolean if a field has been set.

### GetSecret

`func (o *DtoUpdateCredentialRequest) GetSecret() map[string]interface{}`

GetSecret returns the Secret field if non-nil, zero value otherwise.

### GetSecretOk

`func (o *DtoUpdateCredentialRequest) GetSecretOk() (*map[string]interface{}, bool)`

GetSecretOk returns a tuple with the Secret field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSecret

`func (o *DtoUpdateCredentialRequest) SetSecret(v map[string]interface{})`

SetSecret sets Secret field to given value.

### HasSecret

`func (o *DtoUpdateCredentialRequest) HasSecret() bool`

HasSecret returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


