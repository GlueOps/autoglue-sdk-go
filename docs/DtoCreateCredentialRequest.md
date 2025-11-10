# DtoCreateCredentialRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | Pointer to **string** |  | [optional] 
**Kind** | **string** | aws_access_key, api_token, basic_auth, oauth2 | 
**Name** | Pointer to **string** | human label | [optional] 
**Provider** | **string** |  | 
**Region** | Pointer to **string** |  | [optional] 
**SchemaVersion** | **int32** | secret schema version | 
**Scope** | **map[string]interface{}** | {\&quot;service\&quot;:\&quot;route53\&quot;} or {\&quot;arn\&quot;:\&quot;...\&quot;} | 
**ScopeKind** | **string** |  | 
**ScopeVersion** | **int32** | scope schema version | 
**Secret** | **map[string]interface{}** | encrypted later | 

## Methods

### NewDtoCreateCredentialRequest

`func NewDtoCreateCredentialRequest(kind string, provider string, schemaVersion int32, scope map[string]interface{}, scopeKind string, scopeVersion int32, secret map[string]interface{}, ) *DtoCreateCredentialRequest`

NewDtoCreateCredentialRequest instantiates a new DtoCreateCredentialRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewDtoCreateCredentialRequestWithDefaults

`func NewDtoCreateCredentialRequestWithDefaults() *DtoCreateCredentialRequest`

NewDtoCreateCredentialRequestWithDefaults instantiates a new DtoCreateCredentialRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetAccountId

`func (o *DtoCreateCredentialRequest) GetAccountId() string`

GetAccountId returns the AccountId field if non-nil, zero value otherwise.

### GetAccountIdOk

`func (o *DtoCreateCredentialRequest) GetAccountIdOk() (*string, bool)`

GetAccountIdOk returns a tuple with the AccountId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetAccountId

`func (o *DtoCreateCredentialRequest) SetAccountId(v string)`

SetAccountId sets AccountId field to given value.

### HasAccountId

`func (o *DtoCreateCredentialRequest) HasAccountId() bool`

HasAccountId returns a boolean if a field has been set.

### GetKind

`func (o *DtoCreateCredentialRequest) GetKind() string`

GetKind returns the Kind field if non-nil, zero value otherwise.

### GetKindOk

`func (o *DtoCreateCredentialRequest) GetKindOk() (*string, bool)`

GetKindOk returns a tuple with the Kind field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetKind

`func (o *DtoCreateCredentialRequest) SetKind(v string)`

SetKind sets Kind field to given value.


### GetName

`func (o *DtoCreateCredentialRequest) GetName() string`

GetName returns the Name field if non-nil, zero value otherwise.

### GetNameOk

`func (o *DtoCreateCredentialRequest) GetNameOk() (*string, bool)`

GetNameOk returns a tuple with the Name field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetName

`func (o *DtoCreateCredentialRequest) SetName(v string)`

SetName sets Name field to given value.

### HasName

`func (o *DtoCreateCredentialRequest) HasName() bool`

HasName returns a boolean if a field has been set.

### GetProvider

`func (o *DtoCreateCredentialRequest) GetProvider() string`

GetProvider returns the Provider field if non-nil, zero value otherwise.

### GetProviderOk

`func (o *DtoCreateCredentialRequest) GetProviderOk() (*string, bool)`

GetProviderOk returns a tuple with the Provider field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetProvider

`func (o *DtoCreateCredentialRequest) SetProvider(v string)`

SetProvider sets Provider field to given value.


### GetRegion

`func (o *DtoCreateCredentialRequest) GetRegion() string`

GetRegion returns the Region field if non-nil, zero value otherwise.

### GetRegionOk

`func (o *DtoCreateCredentialRequest) GetRegionOk() (*string, bool)`

GetRegionOk returns a tuple with the Region field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRegion

`func (o *DtoCreateCredentialRequest) SetRegion(v string)`

SetRegion sets Region field to given value.

### HasRegion

`func (o *DtoCreateCredentialRequest) HasRegion() bool`

HasRegion returns a boolean if a field has been set.

### GetSchemaVersion

`func (o *DtoCreateCredentialRequest) GetSchemaVersion() int32`

GetSchemaVersion returns the SchemaVersion field if non-nil, zero value otherwise.

### GetSchemaVersionOk

`func (o *DtoCreateCredentialRequest) GetSchemaVersionOk() (*int32, bool)`

GetSchemaVersionOk returns a tuple with the SchemaVersion field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSchemaVersion

`func (o *DtoCreateCredentialRequest) SetSchemaVersion(v int32)`

SetSchemaVersion sets SchemaVersion field to given value.


### GetScope

`func (o *DtoCreateCredentialRequest) GetScope() map[string]interface{}`

GetScope returns the Scope field if non-nil, zero value otherwise.

### GetScopeOk

`func (o *DtoCreateCredentialRequest) GetScopeOk() (*map[string]interface{}, bool)`

GetScopeOk returns a tuple with the Scope field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetScope

`func (o *DtoCreateCredentialRequest) SetScope(v map[string]interface{})`

SetScope sets Scope field to given value.


### GetScopeKind

`func (o *DtoCreateCredentialRequest) GetScopeKind() string`

GetScopeKind returns the ScopeKind field if non-nil, zero value otherwise.

### GetScopeKindOk

`func (o *DtoCreateCredentialRequest) GetScopeKindOk() (*string, bool)`

GetScopeKindOk returns a tuple with the ScopeKind field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetScopeKind

`func (o *DtoCreateCredentialRequest) SetScopeKind(v string)`

SetScopeKind sets ScopeKind field to given value.


### GetScopeVersion

`func (o *DtoCreateCredentialRequest) GetScopeVersion() int32`

GetScopeVersion returns the ScopeVersion field if non-nil, zero value otherwise.

### GetScopeVersionOk

`func (o *DtoCreateCredentialRequest) GetScopeVersionOk() (*int32, bool)`

GetScopeVersionOk returns a tuple with the ScopeVersion field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetScopeVersion

`func (o *DtoCreateCredentialRequest) SetScopeVersion(v int32)`

SetScopeVersion sets ScopeVersion field to given value.


### GetSecret

`func (o *DtoCreateCredentialRequest) GetSecret() map[string]interface{}`

GetSecret returns the Secret field if non-nil, zero value otherwise.

### GetSecretOk

`func (o *DtoCreateCredentialRequest) GetSecretOk() (*map[string]interface{}, bool)`

GetSecretOk returns a tuple with the Secret field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSecret

`func (o *DtoCreateCredentialRequest) SetSecret(v map[string]interface{})`

SetSecret sets Secret field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


