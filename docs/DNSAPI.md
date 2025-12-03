# \DNSAPI

All URIs are relative to *https://autoglue.glueopshosted.com/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**CreateDomain**](DNSAPI.md#CreateDomain) | **Post** /dns/domains | Create a domain (org scoped)
[**CreateRecordSet**](DNSAPI.md#CreateRecordSet) | **Post** /dns/domains/{domain_id}/records | Create a record set (pending; Archer will UPSERT to Route 53)
[**DeleteDomain**](DNSAPI.md#DeleteDomain) | **Delete** /dns/domains/{id} | Delete a domain
[**DeleteRecordSet**](DNSAPI.md#DeleteRecordSet) | **Delete** /dns/records/{id} | Delete a record set (API removes row; worker can optionally handle external deletion policy)
[**GetDomain**](DNSAPI.md#GetDomain) | **Get** /dns/domains/{id} | Get a domain (org scoped)
[**ListDomains**](DNSAPI.md#ListDomains) | **Get** /dns/domains | List domains (org scoped)
[**ListRecordSets**](DNSAPI.md#ListRecordSets) | **Get** /dns/domains/{domain_id}/records | List record sets for a domain
[**UpdateDomain**](DNSAPI.md#UpdateDomain) | **Patch** /dns/domains/{id} | Update a domain (org scoped)
[**UpdateRecordSet**](DNSAPI.md#UpdateRecordSet) | **Patch** /dns/records/{id} | Update a record set (flips to pending for reconciliation)



## CreateDomain

> DtoDomainResponse CreateDomain(ctx).DtoCreateDomainRequest(dtoCreateDomainRequest).XOrgID(xOrgID).Execute()

Create a domain (org scoped)



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
	dtoCreateDomainRequest := *openapiclient.NewDtoCreateDomainRequest("CredentialId_example", "DomainName_example") // DtoCreateDomainRequest | Domain payload
	xOrgID := "xOrgID_example" // string | Organization UUID (optional)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.DNSAPI.CreateDomain(context.Background()).DtoCreateDomainRequest(dtoCreateDomainRequest).XOrgID(xOrgID).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `DNSAPI.CreateDomain``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `CreateDomain`: DtoDomainResponse
	fmt.Fprintf(os.Stdout, "Response from `DNSAPI.CreateDomain`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiCreateDomainRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **dtoCreateDomainRequest** | [**DtoCreateDomainRequest**](DtoCreateDomainRequest.md) | Domain payload | 
 **xOrgID** | **string** | Organization UUID | 

### Return type

[**DtoDomainResponse**](DtoDomainResponse.md)

### Authorization

[OrgKeyAuth](../README.md#OrgKeyAuth), [OrgSecretAuth](../README.md#OrgSecretAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## CreateRecordSet

> DtoRecordSetResponse CreateRecordSet(ctx, domainId).DtoCreateRecordSetRequest(dtoCreateRecordSetRequest).XOrgID(xOrgID).Execute()

Create a record set (pending; Archer will UPSERT to Route 53)

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
	domainId := "domainId_example" // string | Domain ID (UUID)
	dtoCreateRecordSetRequest := *openapiclient.NewDtoCreateRecordSetRequest("Name_example", "Type_example") // DtoCreateRecordSetRequest | Record set payload
	xOrgID := "xOrgID_example" // string | Organization UUID (optional)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.DNSAPI.CreateRecordSet(context.Background(), domainId).DtoCreateRecordSetRequest(dtoCreateRecordSetRequest).XOrgID(xOrgID).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `DNSAPI.CreateRecordSet``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `CreateRecordSet`: DtoRecordSetResponse
	fmt.Fprintf(os.Stdout, "Response from `DNSAPI.CreateRecordSet`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**domainId** | **string** | Domain ID (UUID) | 

### Other Parameters

Other parameters are passed through a pointer to a apiCreateRecordSetRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **dtoCreateRecordSetRequest** | [**DtoCreateRecordSetRequest**](DtoCreateRecordSetRequest.md) | Record set payload | 
 **xOrgID** | **string** | Organization UUID | 

### Return type

[**DtoRecordSetResponse**](DtoRecordSetResponse.md)

### Authorization

[OrgKeyAuth](../README.md#OrgKeyAuth), [OrgSecretAuth](../README.md#OrgSecretAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## DeleteDomain

> DeleteDomain(ctx, id).XOrgID(xOrgID).Execute()

Delete a domain

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
	id := "id_example" // string | Domain ID (UUID)
	xOrgID := "xOrgID_example" // string | Organization UUID (optional)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	r, err := apiClient.DNSAPI.DeleteDomain(context.Background(), id).XOrgID(xOrgID).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `DNSAPI.DeleteDomain``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Domain ID (UUID) | 

### Other Parameters

Other parameters are passed through a pointer to a apiDeleteDomainRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xOrgID** | **string** | Organization UUID | 

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


## DeleteRecordSet

> DeleteRecordSet(ctx, id).XOrgID(xOrgID).Execute()

Delete a record set (API removes row; worker can optionally handle external deletion policy)

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
	id := "id_example" // string | Record Set ID (UUID)
	xOrgID := "xOrgID_example" // string | Organization UUID (optional)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	r, err := apiClient.DNSAPI.DeleteRecordSet(context.Background(), id).XOrgID(xOrgID).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `DNSAPI.DeleteRecordSet``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Record Set ID (UUID) | 

### Other Parameters

Other parameters are passed through a pointer to a apiDeleteRecordSetRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xOrgID** | **string** | Organization UUID | 

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


## GetDomain

> DtoDomainResponse GetDomain(ctx, id).XOrgID(xOrgID).Execute()

Get a domain (org scoped)

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
	id := "id_example" // string | Domain ID (UUID)
	xOrgID := "xOrgID_example" // string | Organization UUID (optional)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.DNSAPI.GetDomain(context.Background(), id).XOrgID(xOrgID).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `DNSAPI.GetDomain``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetDomain`: DtoDomainResponse
	fmt.Fprintf(os.Stdout, "Response from `DNSAPI.GetDomain`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Domain ID (UUID) | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetDomainRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xOrgID** | **string** | Organization UUID | 

### Return type

[**DtoDomainResponse**](DtoDomainResponse.md)

### Authorization

[OrgKeyAuth](../README.md#OrgKeyAuth), [OrgSecretAuth](../README.md#OrgSecretAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ListDomains

> []DtoDomainResponse ListDomains(ctx).XOrgID(xOrgID).DomainName(domainName).Status(status).Q(q).Execute()

List domains (org scoped)



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
	xOrgID := "xOrgID_example" // string | Organization UUID (optional)
	domainName := "domainName_example" // string | Exact domain name (lowercase, no trailing dot) (optional)
	status := "status_example" // string | pending|provisioning|ready|failed (optional)
	q := "q_example" // string | Domain contains (case-insensitive) (optional)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.DNSAPI.ListDomains(context.Background()).XOrgID(xOrgID).DomainName(domainName).Status(status).Q(q).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `DNSAPI.ListDomains``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListDomains`: []DtoDomainResponse
	fmt.Fprintf(os.Stdout, "Response from `DNSAPI.ListDomains`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiListDomainsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xOrgID** | **string** | Organization UUID | 
 **domainName** | **string** | Exact domain name (lowercase, no trailing dot) | 
 **status** | **string** | pending|provisioning|ready|failed | 
 **q** | **string** | Domain contains (case-insensitive) | 

### Return type

[**[]DtoDomainResponse**](DtoDomainResponse.md)

### Authorization

[OrgKeyAuth](../README.md#OrgKeyAuth), [OrgSecretAuth](../README.md#OrgSecretAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ListRecordSets

> []DtoRecordSetResponse ListRecordSets(ctx, domainId).XOrgID(xOrgID).Name(name).Type_(type_).Status(status).Execute()

List record sets for a domain



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
	domainId := "domainId_example" // string | Domain ID (UUID)
	xOrgID := "xOrgID_example" // string | Organization UUID (optional)
	name := "name_example" // string | Exact relative name or FQDN (server normalizes) (optional)
	type_ := "type__example" // string | RR type (A, AAAA, CNAME, TXT, MX, NS, SRV, CAA) (optional)
	status := "status_example" // string | pending|provisioning|ready|failed (optional)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.DNSAPI.ListRecordSets(context.Background(), domainId).XOrgID(xOrgID).Name(name).Type_(type_).Status(status).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `DNSAPI.ListRecordSets``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListRecordSets`: []DtoRecordSetResponse
	fmt.Fprintf(os.Stdout, "Response from `DNSAPI.ListRecordSets`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**domainId** | **string** | Domain ID (UUID) | 

### Other Parameters

Other parameters are passed through a pointer to a apiListRecordSetsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xOrgID** | **string** | Organization UUID | 
 **name** | **string** | Exact relative name or FQDN (server normalizes) | 
 **type_** | **string** | RR type (A, AAAA, CNAME, TXT, MX, NS, SRV, CAA) | 
 **status** | **string** | pending|provisioning|ready|failed | 

### Return type

[**[]DtoRecordSetResponse**](DtoRecordSetResponse.md)

### Authorization

[OrgKeyAuth](../README.md#OrgKeyAuth), [OrgSecretAuth](../README.md#OrgSecretAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## UpdateDomain

> DtoDomainResponse UpdateDomain(ctx, id).DtoUpdateDomainRequest(dtoUpdateDomainRequest).XOrgID(xOrgID).Execute()

Update a domain (org scoped)

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
	id := "id_example" // string | Domain ID (UUID)
	dtoUpdateDomainRequest := *openapiclient.NewDtoUpdateDomainRequest() // DtoUpdateDomainRequest | Fields to update
	xOrgID := "xOrgID_example" // string | Organization UUID (optional)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.DNSAPI.UpdateDomain(context.Background(), id).DtoUpdateDomainRequest(dtoUpdateDomainRequest).XOrgID(xOrgID).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `DNSAPI.UpdateDomain``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `UpdateDomain`: DtoDomainResponse
	fmt.Fprintf(os.Stdout, "Response from `DNSAPI.UpdateDomain`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Domain ID (UUID) | 

### Other Parameters

Other parameters are passed through a pointer to a apiUpdateDomainRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **dtoUpdateDomainRequest** | [**DtoUpdateDomainRequest**](DtoUpdateDomainRequest.md) | Fields to update | 
 **xOrgID** | **string** | Organization UUID | 

### Return type

[**DtoDomainResponse**](DtoDomainResponse.md)

### Authorization

[OrgKeyAuth](../README.md#OrgKeyAuth), [OrgSecretAuth](../README.md#OrgSecretAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## UpdateRecordSet

> DtoRecordSetResponse UpdateRecordSet(ctx, id).DtoUpdateRecordSetRequest(dtoUpdateRecordSetRequest).XOrgID(xOrgID).Execute()

Update a record set (flips to pending for reconciliation)

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
	id := "id_example" // string | Record Set ID (UUID)
	dtoUpdateRecordSetRequest := *openapiclient.NewDtoUpdateRecordSetRequest() // DtoUpdateRecordSetRequest | Fields to update
	xOrgID := "xOrgID_example" // string | Organization UUID (optional)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.DNSAPI.UpdateRecordSet(context.Background(), id).DtoUpdateRecordSetRequest(dtoUpdateRecordSetRequest).XOrgID(xOrgID).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `DNSAPI.UpdateRecordSet``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `UpdateRecordSet`: DtoRecordSetResponse
	fmt.Fprintf(os.Stdout, "Response from `DNSAPI.UpdateRecordSet`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Record Set ID (UUID) | 

### Other Parameters

Other parameters are passed through a pointer to a apiUpdateRecordSetRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **dtoUpdateRecordSetRequest** | [**DtoUpdateRecordSetRequest**](DtoUpdateRecordSetRequest.md) | Fields to update | 
 **xOrgID** | **string** | Organization UUID | 

### Return type

[**DtoRecordSetResponse**](DtoRecordSetResponse.md)

### Authorization

[OrgKeyAuth](../README.md#OrgKeyAuth), [OrgSecretAuth](../README.md#OrgSecretAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)

