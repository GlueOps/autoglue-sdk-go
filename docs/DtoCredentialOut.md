# DtoCredentialOut

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | Pointer to **string** |  | [optional] 
**CreatedAt** | Pointer to **string** |  | [optional] 
**CredentialProvider** | Pointer to **string** |  | [optional] 
**Id** | Pointer to **string** |  | [optional] 
**Kind** | Pointer to **string** |  | [optional] 
**Name** | Pointer to **string** |  | [optional] 
**Region** | Pointer to **string** |  | [optional] 
**SchemaVersion** | Pointer to **int32** |  | [optional] 
**Scope** | Pointer to **map[string]interface{}** |  | [optional] 
**ScopeKind** | Pointer to **string** |  | [optional] 
**ScopeVersion** | Pointer to **int32** |  | [optional] 
**UpdatedAt** | Pointer to **string** |  | [optional] 

## Methods

### NewDtoCredentialOut

`func NewDtoCredentialOut() *DtoCredentialOut`

NewDtoCredentialOut instantiates a new DtoCredentialOut object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewDtoCredentialOutWithDefaults

`func NewDtoCredentialOutWithDefaults() *DtoCredentialOut`

NewDtoCredentialOutWithDefaults instantiates a new DtoCredentialOut object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetAccountId

`func (o *DtoCredentialOut) GetAccountId() string`

GetAccountId returns the AccountId field if non-nil, zero value otherwise.

### GetAccountIdOk

`func (o *DtoCredentialOut) GetAccountIdOk() (*string, bool)`

GetAccountIdOk returns a tuple with the AccountId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetAccountId

`func (o *DtoCredentialOut) SetAccountId(v string)`

SetAccountId sets AccountId field to given value.

### HasAccountId

`func (o *DtoCredentialOut) HasAccountId() bool`

HasAccountId returns a boolean if a field has been set.

### GetCreatedAt

`func (o *DtoCredentialOut) GetCreatedAt() string`

GetCreatedAt returns the CreatedAt field if non-nil, zero value otherwise.

### GetCreatedAtOk

`func (o *DtoCredentialOut) GetCreatedAtOk() (*string, bool)`

GetCreatedAtOk returns a tuple with the CreatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCreatedAt

`func (o *DtoCredentialOut) SetCreatedAt(v string)`

SetCreatedAt sets CreatedAt field to given value.

### HasCreatedAt

`func (o *DtoCredentialOut) HasCreatedAt() bool`

HasCreatedAt returns a boolean if a field has been set.

### GetCredentialProvider

`func (o *DtoCredentialOut) GetCredentialProvider() string`

GetCredentialProvider returns the CredentialProvider field if non-nil, zero value otherwise.

### GetCredentialProviderOk

`func (o *DtoCredentialOut) GetCredentialProviderOk() (*string, bool)`

GetCredentialProviderOk returns a tuple with the CredentialProvider field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCredentialProvider

`func (o *DtoCredentialOut) SetCredentialProvider(v string)`

SetCredentialProvider sets CredentialProvider field to given value.

### HasCredentialProvider

`func (o *DtoCredentialOut) HasCredentialProvider() bool`

HasCredentialProvider returns a boolean if a field has been set.

### GetId

`func (o *DtoCredentialOut) GetId() string`

GetId returns the Id field if non-nil, zero value otherwise.

### GetIdOk

`func (o *DtoCredentialOut) GetIdOk() (*string, bool)`

GetIdOk returns a tuple with the Id field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetId

`func (o *DtoCredentialOut) SetId(v string)`

SetId sets Id field to given value.

### HasId

`func (o *DtoCredentialOut) HasId() bool`

HasId returns a boolean if a field has been set.

### GetKind

`func (o *DtoCredentialOut) GetKind() string`

GetKind returns the Kind field if non-nil, zero value otherwise.

### GetKindOk

`func (o *DtoCredentialOut) GetKindOk() (*string, bool)`

GetKindOk returns a tuple with the Kind field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetKind

`func (o *DtoCredentialOut) SetKind(v string)`

SetKind sets Kind field to given value.

### HasKind

`func (o *DtoCredentialOut) HasKind() bool`

HasKind returns a boolean if a field has been set.

### GetName

`func (o *DtoCredentialOut) GetName() string`

GetName returns the Name field if non-nil, zero value otherwise.

### GetNameOk

`func (o *DtoCredentialOut) GetNameOk() (*string, bool)`

GetNameOk returns a tuple with the Name field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetName

`func (o *DtoCredentialOut) SetName(v string)`

SetName sets Name field to given value.

### HasName

`func (o *DtoCredentialOut) HasName() bool`

HasName returns a boolean if a field has been set.

### GetRegion

`func (o *DtoCredentialOut) GetRegion() string`

GetRegion returns the Region field if non-nil, zero value otherwise.

### GetRegionOk

`func (o *DtoCredentialOut) GetRegionOk() (*string, bool)`

GetRegionOk returns a tuple with the Region field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRegion

`func (o *DtoCredentialOut) SetRegion(v string)`

SetRegion sets Region field to given value.

### HasRegion

`func (o *DtoCredentialOut) HasRegion() bool`

HasRegion returns a boolean if a field has been set.

### GetSchemaVersion

`func (o *DtoCredentialOut) GetSchemaVersion() int32`

GetSchemaVersion returns the SchemaVersion field if non-nil, zero value otherwise.

### GetSchemaVersionOk

`func (o *DtoCredentialOut) GetSchemaVersionOk() (*int32, bool)`

GetSchemaVersionOk returns a tuple with the SchemaVersion field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSchemaVersion

`func (o *DtoCredentialOut) SetSchemaVersion(v int32)`

SetSchemaVersion sets SchemaVersion field to given value.

### HasSchemaVersion

`func (o *DtoCredentialOut) HasSchemaVersion() bool`

HasSchemaVersion returns a boolean if a field has been set.

### GetScope

`func (o *DtoCredentialOut) GetScope() map[string]interface{}`

GetScope returns the Scope field if non-nil, zero value otherwise.

### GetScopeOk

`func (o *DtoCredentialOut) GetScopeOk() (*map[string]interface{}, bool)`

GetScopeOk returns a tuple with the Scope field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetScope

`func (o *DtoCredentialOut) SetScope(v map[string]interface{})`

SetScope sets Scope field to given value.

### HasScope

`func (o *DtoCredentialOut) HasScope() bool`

HasScope returns a boolean if a field has been set.

### GetScopeKind

`func (o *DtoCredentialOut) GetScopeKind() string`

GetScopeKind returns the ScopeKind field if non-nil, zero value otherwise.

### GetScopeKindOk

`func (o *DtoCredentialOut) GetScopeKindOk() (*string, bool)`

GetScopeKindOk returns a tuple with the ScopeKind field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetScopeKind

`func (o *DtoCredentialOut) SetScopeKind(v string)`

SetScopeKind sets ScopeKind field to given value.

### HasScopeKind

`func (o *DtoCredentialOut) HasScopeKind() bool`

HasScopeKind returns a boolean if a field has been set.

### GetScopeVersion

`func (o *DtoCredentialOut) GetScopeVersion() int32`

GetScopeVersion returns the ScopeVersion field if non-nil, zero value otherwise.

### GetScopeVersionOk

`func (o *DtoCredentialOut) GetScopeVersionOk() (*int32, bool)`

GetScopeVersionOk returns a tuple with the ScopeVersion field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetScopeVersion

`func (o *DtoCredentialOut) SetScopeVersion(v int32)`

SetScopeVersion sets ScopeVersion field to given value.

### HasScopeVersion

`func (o *DtoCredentialOut) HasScopeVersion() bool`

HasScopeVersion returns a boolean if a field has been set.

### GetUpdatedAt

`func (o *DtoCredentialOut) GetUpdatedAt() string`

GetUpdatedAt returns the UpdatedAt field if non-nil, zero value otherwise.

### GetUpdatedAtOk

`func (o *DtoCredentialOut) GetUpdatedAtOk() (*string, bool)`

GetUpdatedAtOk returns a tuple with the UpdatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUpdatedAt

`func (o *DtoCredentialOut) SetUpdatedAt(v string)`

SetUpdatedAt sets UpdatedAt field to given value.

### HasUpdatedAt

`func (o *DtoCredentialOut) HasUpdatedAt() bool`

HasUpdatedAt returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


