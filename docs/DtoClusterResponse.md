# DtoClusterResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AppsLoadBalancer** | Pointer to [**DtoLoadBalancerResponse**](DtoLoadBalancerResponse.md) |  | [optional] 
**BastionServer** | Pointer to [**DtoServerResponse**](DtoServerResponse.md) |  | [optional] 
**CaptainDomain** | Pointer to [**DtoDomainResponse**](DtoDomainResponse.md) |  | [optional] 
**CertificateKey** | Pointer to **string** |  | [optional] 
**ClusterProvider** | Pointer to **string** |  | [optional] 
**ControlPlaneFqdn** | Pointer to **string** |  | [optional] 
**ControlPlaneRecordSet** | Pointer to [**DtoRecordSetResponse**](DtoRecordSetResponse.md) |  | [optional] 
**CreatedAt** | Pointer to **string** |  | [optional] 
**DockerImage** | Pointer to **string** |  | [optional] 
**DockerTag** | Pointer to **string** |  | [optional] 
**GlueopsLoadBalancer** | Pointer to [**DtoLoadBalancerResponse**](DtoLoadBalancerResponse.md) |  | [optional] 
**Id** | Pointer to **string** |  | [optional] 
**LastError** | Pointer to **string** |  | [optional] 
**Name** | Pointer to **string** |  | [optional] 
**NodePools** | Pointer to [**[]DtoNodePoolResponse**](DtoNodePoolResponse.md) |  | [optional] 
**RandomToken** | Pointer to **string** |  | [optional] 
**Region** | Pointer to **string** |  | [optional] 
**Status** | Pointer to **string** |  | [optional] 
**UpdatedAt** | Pointer to **string** |  | [optional] 

## Methods

### NewDtoClusterResponse

`func NewDtoClusterResponse() *DtoClusterResponse`

NewDtoClusterResponse instantiates a new DtoClusterResponse object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewDtoClusterResponseWithDefaults

`func NewDtoClusterResponseWithDefaults() *DtoClusterResponse`

NewDtoClusterResponseWithDefaults instantiates a new DtoClusterResponse object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetAppsLoadBalancer

`func (o *DtoClusterResponse) GetAppsLoadBalancer() DtoLoadBalancerResponse`

GetAppsLoadBalancer returns the AppsLoadBalancer field if non-nil, zero value otherwise.

### GetAppsLoadBalancerOk

`func (o *DtoClusterResponse) GetAppsLoadBalancerOk() (*DtoLoadBalancerResponse, bool)`

GetAppsLoadBalancerOk returns a tuple with the AppsLoadBalancer field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetAppsLoadBalancer

`func (o *DtoClusterResponse) SetAppsLoadBalancer(v DtoLoadBalancerResponse)`

SetAppsLoadBalancer sets AppsLoadBalancer field to given value.

### HasAppsLoadBalancer

`func (o *DtoClusterResponse) HasAppsLoadBalancer() bool`

HasAppsLoadBalancer returns a boolean if a field has been set.

### GetBastionServer

`func (o *DtoClusterResponse) GetBastionServer() DtoServerResponse`

GetBastionServer returns the BastionServer field if non-nil, zero value otherwise.

### GetBastionServerOk

`func (o *DtoClusterResponse) GetBastionServerOk() (*DtoServerResponse, bool)`

GetBastionServerOk returns a tuple with the BastionServer field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetBastionServer

`func (o *DtoClusterResponse) SetBastionServer(v DtoServerResponse)`

SetBastionServer sets BastionServer field to given value.

### HasBastionServer

`func (o *DtoClusterResponse) HasBastionServer() bool`

HasBastionServer returns a boolean if a field has been set.

### GetCaptainDomain

`func (o *DtoClusterResponse) GetCaptainDomain() DtoDomainResponse`

GetCaptainDomain returns the CaptainDomain field if non-nil, zero value otherwise.

### GetCaptainDomainOk

`func (o *DtoClusterResponse) GetCaptainDomainOk() (*DtoDomainResponse, bool)`

GetCaptainDomainOk returns a tuple with the CaptainDomain field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCaptainDomain

`func (o *DtoClusterResponse) SetCaptainDomain(v DtoDomainResponse)`

SetCaptainDomain sets CaptainDomain field to given value.

### HasCaptainDomain

`func (o *DtoClusterResponse) HasCaptainDomain() bool`

HasCaptainDomain returns a boolean if a field has been set.

### GetCertificateKey

`func (o *DtoClusterResponse) GetCertificateKey() string`

GetCertificateKey returns the CertificateKey field if non-nil, zero value otherwise.

### GetCertificateKeyOk

`func (o *DtoClusterResponse) GetCertificateKeyOk() (*string, bool)`

GetCertificateKeyOk returns a tuple with the CertificateKey field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCertificateKey

`func (o *DtoClusterResponse) SetCertificateKey(v string)`

SetCertificateKey sets CertificateKey field to given value.

### HasCertificateKey

`func (o *DtoClusterResponse) HasCertificateKey() bool`

HasCertificateKey returns a boolean if a field has been set.

### GetClusterProvider

`func (o *DtoClusterResponse) GetClusterProvider() string`

GetClusterProvider returns the ClusterProvider field if non-nil, zero value otherwise.

### GetClusterProviderOk

`func (o *DtoClusterResponse) GetClusterProviderOk() (*string, bool)`

GetClusterProviderOk returns a tuple with the ClusterProvider field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetClusterProvider

`func (o *DtoClusterResponse) SetClusterProvider(v string)`

SetClusterProvider sets ClusterProvider field to given value.

### HasClusterProvider

`func (o *DtoClusterResponse) HasClusterProvider() bool`

HasClusterProvider returns a boolean if a field has been set.

### GetControlPlaneFqdn

`func (o *DtoClusterResponse) GetControlPlaneFqdn() string`

GetControlPlaneFqdn returns the ControlPlaneFqdn field if non-nil, zero value otherwise.

### GetControlPlaneFqdnOk

`func (o *DtoClusterResponse) GetControlPlaneFqdnOk() (*string, bool)`

GetControlPlaneFqdnOk returns a tuple with the ControlPlaneFqdn field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetControlPlaneFqdn

`func (o *DtoClusterResponse) SetControlPlaneFqdn(v string)`

SetControlPlaneFqdn sets ControlPlaneFqdn field to given value.

### HasControlPlaneFqdn

`func (o *DtoClusterResponse) HasControlPlaneFqdn() bool`

HasControlPlaneFqdn returns a boolean if a field has been set.

### GetControlPlaneRecordSet

`func (o *DtoClusterResponse) GetControlPlaneRecordSet() DtoRecordSetResponse`

GetControlPlaneRecordSet returns the ControlPlaneRecordSet field if non-nil, zero value otherwise.

### GetControlPlaneRecordSetOk

`func (o *DtoClusterResponse) GetControlPlaneRecordSetOk() (*DtoRecordSetResponse, bool)`

GetControlPlaneRecordSetOk returns a tuple with the ControlPlaneRecordSet field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetControlPlaneRecordSet

`func (o *DtoClusterResponse) SetControlPlaneRecordSet(v DtoRecordSetResponse)`

SetControlPlaneRecordSet sets ControlPlaneRecordSet field to given value.

### HasControlPlaneRecordSet

`func (o *DtoClusterResponse) HasControlPlaneRecordSet() bool`

HasControlPlaneRecordSet returns a boolean if a field has been set.

### GetCreatedAt

`func (o *DtoClusterResponse) GetCreatedAt() string`

GetCreatedAt returns the CreatedAt field if non-nil, zero value otherwise.

### GetCreatedAtOk

`func (o *DtoClusterResponse) GetCreatedAtOk() (*string, bool)`

GetCreatedAtOk returns a tuple with the CreatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCreatedAt

`func (o *DtoClusterResponse) SetCreatedAt(v string)`

SetCreatedAt sets CreatedAt field to given value.

### HasCreatedAt

`func (o *DtoClusterResponse) HasCreatedAt() bool`

HasCreatedAt returns a boolean if a field has been set.

### GetDockerImage

`func (o *DtoClusterResponse) GetDockerImage() string`

GetDockerImage returns the DockerImage field if non-nil, zero value otherwise.

### GetDockerImageOk

`func (o *DtoClusterResponse) GetDockerImageOk() (*string, bool)`

GetDockerImageOk returns a tuple with the DockerImage field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDockerImage

`func (o *DtoClusterResponse) SetDockerImage(v string)`

SetDockerImage sets DockerImage field to given value.

### HasDockerImage

`func (o *DtoClusterResponse) HasDockerImage() bool`

HasDockerImage returns a boolean if a field has been set.

### GetDockerTag

`func (o *DtoClusterResponse) GetDockerTag() string`

GetDockerTag returns the DockerTag field if non-nil, zero value otherwise.

### GetDockerTagOk

`func (o *DtoClusterResponse) GetDockerTagOk() (*string, bool)`

GetDockerTagOk returns a tuple with the DockerTag field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDockerTag

`func (o *DtoClusterResponse) SetDockerTag(v string)`

SetDockerTag sets DockerTag field to given value.

### HasDockerTag

`func (o *DtoClusterResponse) HasDockerTag() bool`

HasDockerTag returns a boolean if a field has been set.

### GetGlueopsLoadBalancer

`func (o *DtoClusterResponse) GetGlueopsLoadBalancer() DtoLoadBalancerResponse`

GetGlueopsLoadBalancer returns the GlueopsLoadBalancer field if non-nil, zero value otherwise.

### GetGlueopsLoadBalancerOk

`func (o *DtoClusterResponse) GetGlueopsLoadBalancerOk() (*DtoLoadBalancerResponse, bool)`

GetGlueopsLoadBalancerOk returns a tuple with the GlueopsLoadBalancer field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetGlueopsLoadBalancer

`func (o *DtoClusterResponse) SetGlueopsLoadBalancer(v DtoLoadBalancerResponse)`

SetGlueopsLoadBalancer sets GlueopsLoadBalancer field to given value.

### HasGlueopsLoadBalancer

`func (o *DtoClusterResponse) HasGlueopsLoadBalancer() bool`

HasGlueopsLoadBalancer returns a boolean if a field has been set.

### GetId

`func (o *DtoClusterResponse) GetId() string`

GetId returns the Id field if non-nil, zero value otherwise.

### GetIdOk

`func (o *DtoClusterResponse) GetIdOk() (*string, bool)`

GetIdOk returns a tuple with the Id field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetId

`func (o *DtoClusterResponse) SetId(v string)`

SetId sets Id field to given value.

### HasId

`func (o *DtoClusterResponse) HasId() bool`

HasId returns a boolean if a field has been set.

### GetLastError

`func (o *DtoClusterResponse) GetLastError() string`

GetLastError returns the LastError field if non-nil, zero value otherwise.

### GetLastErrorOk

`func (o *DtoClusterResponse) GetLastErrorOk() (*string, bool)`

GetLastErrorOk returns a tuple with the LastError field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetLastError

`func (o *DtoClusterResponse) SetLastError(v string)`

SetLastError sets LastError field to given value.

### HasLastError

`func (o *DtoClusterResponse) HasLastError() bool`

HasLastError returns a boolean if a field has been set.

### GetName

`func (o *DtoClusterResponse) GetName() string`

GetName returns the Name field if non-nil, zero value otherwise.

### GetNameOk

`func (o *DtoClusterResponse) GetNameOk() (*string, bool)`

GetNameOk returns a tuple with the Name field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetName

`func (o *DtoClusterResponse) SetName(v string)`

SetName sets Name field to given value.

### HasName

`func (o *DtoClusterResponse) HasName() bool`

HasName returns a boolean if a field has been set.

### GetNodePools

`func (o *DtoClusterResponse) GetNodePools() []DtoNodePoolResponse`

GetNodePools returns the NodePools field if non-nil, zero value otherwise.

### GetNodePoolsOk

`func (o *DtoClusterResponse) GetNodePoolsOk() (*[]DtoNodePoolResponse, bool)`

GetNodePoolsOk returns a tuple with the NodePools field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetNodePools

`func (o *DtoClusterResponse) SetNodePools(v []DtoNodePoolResponse)`

SetNodePools sets NodePools field to given value.

### HasNodePools

`func (o *DtoClusterResponse) HasNodePools() bool`

HasNodePools returns a boolean if a field has been set.

### GetRandomToken

`func (o *DtoClusterResponse) GetRandomToken() string`

GetRandomToken returns the RandomToken field if non-nil, zero value otherwise.

### GetRandomTokenOk

`func (o *DtoClusterResponse) GetRandomTokenOk() (*string, bool)`

GetRandomTokenOk returns a tuple with the RandomToken field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRandomToken

`func (o *DtoClusterResponse) SetRandomToken(v string)`

SetRandomToken sets RandomToken field to given value.

### HasRandomToken

`func (o *DtoClusterResponse) HasRandomToken() bool`

HasRandomToken returns a boolean if a field has been set.

### GetRegion

`func (o *DtoClusterResponse) GetRegion() string`

GetRegion returns the Region field if non-nil, zero value otherwise.

### GetRegionOk

`func (o *DtoClusterResponse) GetRegionOk() (*string, bool)`

GetRegionOk returns a tuple with the Region field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRegion

`func (o *DtoClusterResponse) SetRegion(v string)`

SetRegion sets Region field to given value.

### HasRegion

`func (o *DtoClusterResponse) HasRegion() bool`

HasRegion returns a boolean if a field has been set.

### GetStatus

`func (o *DtoClusterResponse) GetStatus() string`

GetStatus returns the Status field if non-nil, zero value otherwise.

### GetStatusOk

`func (o *DtoClusterResponse) GetStatusOk() (*string, bool)`

GetStatusOk returns a tuple with the Status field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetStatus

`func (o *DtoClusterResponse) SetStatus(v string)`

SetStatus sets Status field to given value.

### HasStatus

`func (o *DtoClusterResponse) HasStatus() bool`

HasStatus returns a boolean if a field has been set.

### GetUpdatedAt

`func (o *DtoClusterResponse) GetUpdatedAt() string`

GetUpdatedAt returns the UpdatedAt field if non-nil, zero value otherwise.

### GetUpdatedAtOk

`func (o *DtoClusterResponse) GetUpdatedAtOk() (*string, bool)`

GetUpdatedAtOk returns a tuple with the UpdatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUpdatedAt

`func (o *DtoClusterResponse) SetUpdatedAt(v string)`

SetUpdatedAt sets UpdatedAt field to given value.

### HasUpdatedAt

`func (o *DtoClusterResponse) HasUpdatedAt() bool`

HasUpdatedAt returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


