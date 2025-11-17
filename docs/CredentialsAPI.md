# \CredentialsAPI

All URIs are relative to *https://autoglue.onglueops.rocks/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**CreateCredential**](CredentialsAPI.md#CreateCredential) | **Post** /credentials | Create a credential (encrypts secret)
[**DeleteCredential**](CredentialsAPI.md#DeleteCredential) | **Delete** /credentials/{id} | Delete credential
[**GetCredential**](CredentialsAPI.md#GetCredential) | **Get** /credentials/{id} | Get credential by ID (metadata only)
[**ListCredentials**](CredentialsAPI.md#ListCredentials) | **Get** /credentials | List credentials (metadata only)
[**RevealCredential**](CredentialsAPI.md#RevealCredential) | **Post** /credentials/{id}/reveal | Reveal decrypted secret (one-time read)
[**UpdateCredential**](CredentialsAPI.md#UpdateCredential) | **Patch** /credentials/{id} | Update credential metadata and/or rotate secret



## CreateCredential

> DtoCredentialOut CreateCredential(ctx).DtoCreateCredentialRequest(dtoCreateCredentialRequest).XOrgID(xOrgID).Execute()

Create a credential (encrypts secret)

### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
	openapiclient "github.com/glueops/autoglue-sdk-go"
)

func main() {
	dtoCreateCredentialRequest := *openapiclient.NewDtoCreateCredentialRequest("Kind_example", "Provider_example", int32(123), map[string]interface{}(123), "ScopeKind_example", int32(123), map[string]interface{}(123)) // DtoCreateCredentialRequest | Credential payload
	xOrgID := "xOrgID_example" // string | Organization ID (UUID) (optional)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.CredentialsAPI.CreateCredential(context.Background()).DtoCreateCredentialRequest(dtoCreateCredentialRequest).XOrgID(xOrgID).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `CredentialsAPI.CreateCredential``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `CreateCredential`: DtoCredentialOut
	fmt.Fprintf(os.Stdout, "Response from `CredentialsAPI.CreateCredential`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiCreateCredentialRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **dtoCreateCredentialRequest** | [**DtoCreateCredentialRequest**](DtoCreateCredentialRequest.md) | Credential payload | 
 **xOrgID** | **string** | Organization ID (UUID) | 

### Return type

[**DtoCredentialOut**](DtoCredentialOut.md)

### Authorization

[OrgKeyAuth](../README.md#OrgKeyAuth), [OrgSecretAuth](../README.md#OrgSecretAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## DeleteCredential

> DeleteCredential(ctx, id).XOrgID(xOrgID).Execute()

Delete credential

### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
	openapiclient "github.com/glueops/autoglue-sdk-go"
)

func main() {
	id := "id_example" // string | Credential ID (UUID)
	xOrgID := "xOrgID_example" // string | Organization ID (UUID) (optional)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	r, err := apiClient.CredentialsAPI.DeleteCredential(context.Background(), id).XOrgID(xOrgID).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `CredentialsAPI.DeleteCredential``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Credential ID (UUID) | 

### Other Parameters

Other parameters are passed through a pointer to a apiDeleteCredentialRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xOrgID** | **string** | Organization ID (UUID) | 

### Return type

 (empty response body)

### Authorization

[OrgKeyAuth](../README.md#OrgKeyAuth), [OrgSecretAuth](../README.md#OrgSecretAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetCredential

> DtoCredentialOut GetCredential(ctx, id).XOrgID(xOrgID).Execute()

Get credential by ID (metadata only)

### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
	openapiclient "github.com/glueops/autoglue-sdk-go"
)

func main() {
	id := "id_example" // string | Credential ID (UUID)
	xOrgID := "xOrgID_example" // string | Organization ID (UUID) (optional)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.CredentialsAPI.GetCredential(context.Background(), id).XOrgID(xOrgID).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `CredentialsAPI.GetCredential``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetCredential`: DtoCredentialOut
	fmt.Fprintf(os.Stdout, "Response from `CredentialsAPI.GetCredential`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Credential ID (UUID) | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetCredentialRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xOrgID** | **string** | Organization ID (UUID) | 

### Return type

[**DtoCredentialOut**](DtoCredentialOut.md)

### Authorization

[OrgKeyAuth](../README.md#OrgKeyAuth), [OrgSecretAuth](../README.md#OrgSecretAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ListCredentials

> []DtoCredentialOut ListCredentials(ctx).XOrgID(xOrgID).Provider(provider).Kind(kind).ScopeKind(scopeKind).Execute()

List credentials (metadata only)



### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
	openapiclient "github.com/glueops/autoglue-sdk-go"
)

func main() {
	xOrgID := "xOrgID_example" // string | Organization ID (UUID) (optional)
	provider := "provider_example" // string | Filter by provider (e.g., aws) (optional)
	kind := "kind_example" // string | Filter by kind (e.g., aws_access_key) (optional)
	scopeKind := "scopeKind_example" // string | Filter by scope kind (provider/service/resource) (optional)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.CredentialsAPI.ListCredentials(context.Background()).XOrgID(xOrgID).Provider(provider).Kind(kind).ScopeKind(scopeKind).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `CredentialsAPI.ListCredentials``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListCredentials`: []DtoCredentialOut
	fmt.Fprintf(os.Stdout, "Response from `CredentialsAPI.ListCredentials`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiListCredentialsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xOrgID** | **string** | Organization ID (UUID) | 
 **provider** | **string** | Filter by provider (e.g., aws) | 
 **kind** | **string** | Filter by kind (e.g., aws_access_key) | 
 **scopeKind** | **string** | Filter by scope kind (provider/service/resource) | 

### Return type

[**[]DtoCredentialOut**](DtoCredentialOut.md)

### Authorization

[OrgKeyAuth](../README.md#OrgKeyAuth), [OrgSecretAuth](../README.md#OrgSecretAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## RevealCredential

> map[string]interface{} RevealCredential(ctx, id).XOrgID(xOrgID).Body(body).Execute()

Reveal decrypted secret (one-time read)

### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
	openapiclient "github.com/glueops/autoglue-sdk-go"
)

func main() {
	id := "id_example" // string | Credential ID (UUID)
	xOrgID := "xOrgID_example" // string | Organization ID (UUID) (optional)
	body := map[string]interface{}{ ... } // map[string]interface{} |  (optional)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.CredentialsAPI.RevealCredential(context.Background(), id).XOrgID(xOrgID).Body(body).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `CredentialsAPI.RevealCredential``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `RevealCredential`: map[string]interface{}
	fmt.Fprintf(os.Stdout, "Response from `CredentialsAPI.RevealCredential`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Credential ID (UUID) | 

### Other Parameters

Other parameters are passed through a pointer to a apiRevealCredentialRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xOrgID** | **string** | Organization ID (UUID) | 
 **body** | **map[string]interface{}** |  | 

### Return type

**map[string]interface{}**

### Authorization

[OrgKeyAuth](../README.md#OrgKeyAuth), [OrgSecretAuth](../README.md#OrgSecretAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## UpdateCredential

> DtoCredentialOut UpdateCredential(ctx, id).DtoUpdateCredentialRequest(dtoUpdateCredentialRequest).XOrgID(xOrgID).Execute()

Update credential metadata and/or rotate secret

### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
	openapiclient "github.com/glueops/autoglue-sdk-go"
)

func main() {
	id := "id_example" // string | Credential ID (UUID)
	dtoUpdateCredentialRequest := *openapiclient.NewDtoUpdateCredentialRequest() // DtoUpdateCredentialRequest | Fields to update
	xOrgID := "xOrgID_example" // string | Organization ID (UUID) (optional)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.CredentialsAPI.UpdateCredential(context.Background(), id).DtoUpdateCredentialRequest(dtoUpdateCredentialRequest).XOrgID(xOrgID).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `CredentialsAPI.UpdateCredential``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `UpdateCredential`: DtoCredentialOut
	fmt.Fprintf(os.Stdout, "Response from `CredentialsAPI.UpdateCredential`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Credential ID (UUID) | 

### Other Parameters

Other parameters are passed through a pointer to a apiUpdateCredentialRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **dtoUpdateCredentialRequest** | [**DtoUpdateCredentialRequest**](DtoUpdateCredentialRequest.md) | Fields to update | 
 **xOrgID** | **string** | Organization ID (UUID) | 

### Return type

[**DtoCredentialOut**](DtoCredentialOut.md)

### Authorization

[OrgKeyAuth](../README.md#OrgKeyAuth), [OrgSecretAuth](../README.md#OrgSecretAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)

