# DtoCreateDomainRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CredentialId** | **string** |  | 
**DomainName** | **string** |  | 
**ZoneId** | Pointer to **string** |  | [optional] 

## Methods

### NewDtoCreateDomainRequest

`func NewDtoCreateDomainRequest(credentialId string, domainName string, ) *DtoCreateDomainRequest`

NewDtoCreateDomainRequest instantiates a new DtoCreateDomainRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewDtoCreateDomainRequestWithDefaults

`func NewDtoCreateDomainRequestWithDefaults() *DtoCreateDomainRequest`

NewDtoCreateDomainRequestWithDefaults instantiates a new DtoCreateDomainRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetCredentialId

`func (o *DtoCreateDomainRequest) GetCredentialId() string`

GetCredentialId returns the CredentialId field if non-nil, zero value otherwise.

### GetCredentialIdOk

`func (o *DtoCreateDomainRequest) GetCredentialIdOk() (*string, bool)`

GetCredentialIdOk returns a tuple with the CredentialId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCredentialId

`func (o *DtoCreateDomainRequest) SetCredentialId(v string)`

SetCredentialId sets CredentialId field to given value.


### GetDomainName

`func (o *DtoCreateDomainRequest) GetDomainName() string`

GetDomainName returns the DomainName field if non-nil, zero value otherwise.

### GetDomainNameOk

`func (o *DtoCreateDomainRequest) GetDomainNameOk() (*string, bool)`

GetDomainNameOk returns a tuple with the DomainName field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDomainName

`func (o *DtoCreateDomainRequest) SetDomainName(v string)`

SetDomainName sets DomainName field to given value.


### GetZoneId

`func (o *DtoCreateDomainRequest) GetZoneId() string`

GetZoneId returns the ZoneId field if non-nil, zero value otherwise.

### GetZoneIdOk

`func (o *DtoCreateDomainRequest) GetZoneIdOk() (*string, bool)`

GetZoneIdOk returns a tuple with the ZoneId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetZoneId

`func (o *DtoCreateDomainRequest) SetZoneId(v string)`

SetZoneId sets ZoneId field to given value.

### HasZoneId

`func (o *DtoCreateDomainRequest) HasZoneId() bool`

HasZoneId returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


