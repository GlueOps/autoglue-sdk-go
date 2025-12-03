# \LoadBalancersAPI

All URIs are relative to *https://autoglue.glueopshosted.com/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**CreateLoadBalancer**](LoadBalancersAPI.md#CreateLoadBalancer) | **Post** /load-balancers | Create a load balancer
[**DeleteLoadBalancer**](LoadBalancersAPI.md#DeleteLoadBalancer) | **Delete** /load-balancers/{id} | Delete a load balancer
[**GetLoadBalancers**](LoadBalancersAPI.md#GetLoadBalancers) | **Get** /load-balancers/{id} | Get a load balancer (org scoped)
[**ListLoadBalancers**](LoadBalancersAPI.md#ListLoadBalancers) | **Get** /load-balancers | List load balancers (org scoped)
[**UpdateLoadBalancer**](LoadBalancersAPI.md#UpdateLoadBalancer) | **Patch** /load-balancers/{id} | Update a load balancer (org scoped)



## CreateLoadBalancer

> DtoLoadBalancerResponse CreateLoadBalancer(ctx).DtoCreateLoadBalancerRequest(dtoCreateLoadBalancerRequest).XOrgID(xOrgID).Execute()

Create a load balancer

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
	dtoCreateLoadBalancerRequest := *openapiclient.NewDtoCreateLoadBalancerRequest() // DtoCreateLoadBalancerRequest | Record set payload
	xOrgID := "xOrgID_example" // string | Organization UUID (optional)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.LoadBalancersAPI.CreateLoadBalancer(context.Background()).DtoCreateLoadBalancerRequest(dtoCreateLoadBalancerRequest).XOrgID(xOrgID).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `LoadBalancersAPI.CreateLoadBalancer``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `CreateLoadBalancer`: DtoLoadBalancerResponse
	fmt.Fprintf(os.Stdout, "Response from `LoadBalancersAPI.CreateLoadBalancer`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiCreateLoadBalancerRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **dtoCreateLoadBalancerRequest** | [**DtoCreateLoadBalancerRequest**](DtoCreateLoadBalancerRequest.md) | Record set payload | 
 **xOrgID** | **string** | Organization UUID | 

### Return type

[**DtoLoadBalancerResponse**](DtoLoadBalancerResponse.md)

### Authorization

[OrgKeyAuth](../README.md#OrgKeyAuth), [OrgSecretAuth](../README.md#OrgSecretAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## DeleteLoadBalancer

> DeleteLoadBalancer(ctx, id).XOrgID(xOrgID).Execute()

Delete a load balancer

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
	id := "id_example" // string | Load Balancer ID (UUID)
	xOrgID := "xOrgID_example" // string | Organization UUID (optional)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	r, err := apiClient.LoadBalancersAPI.DeleteLoadBalancer(context.Background(), id).XOrgID(xOrgID).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `LoadBalancersAPI.DeleteLoadBalancer``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Load Balancer ID (UUID) | 

### Other Parameters

Other parameters are passed through a pointer to a apiDeleteLoadBalancerRequest struct via the builder pattern


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


## GetLoadBalancers

> []DtoLoadBalancerResponse GetLoadBalancers(ctx, id).XOrgID(xOrgID).Execute()

Get a load balancer (org scoped)



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
	id := "id_example" // string | LoadBalancer ID (UUID)
	xOrgID := "xOrgID_example" // string | Organization UUID (optional)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.LoadBalancersAPI.GetLoadBalancers(context.Background(), id).XOrgID(xOrgID).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `LoadBalancersAPI.GetLoadBalancers``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetLoadBalancers`: []DtoLoadBalancerResponse
	fmt.Fprintf(os.Stdout, "Response from `LoadBalancersAPI.GetLoadBalancers`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | LoadBalancer ID (UUID) | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetLoadBalancersRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xOrgID** | **string** | Organization UUID | 

### Return type

[**[]DtoLoadBalancerResponse**](DtoLoadBalancerResponse.md)

### Authorization

[OrgKeyAuth](../README.md#OrgKeyAuth), [OrgSecretAuth](../README.md#OrgSecretAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ListLoadBalancers

> []DtoLoadBalancerResponse ListLoadBalancers(ctx).XOrgID(xOrgID).Execute()

List load balancers (org scoped)



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

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.LoadBalancersAPI.ListLoadBalancers(context.Background()).XOrgID(xOrgID).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `LoadBalancersAPI.ListLoadBalancers``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListLoadBalancers`: []DtoLoadBalancerResponse
	fmt.Fprintf(os.Stdout, "Response from `LoadBalancersAPI.ListLoadBalancers`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiListLoadBalancersRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xOrgID** | **string** | Organization UUID | 

### Return type

[**[]DtoLoadBalancerResponse**](DtoLoadBalancerResponse.md)

### Authorization

[OrgKeyAuth](../README.md#OrgKeyAuth), [OrgSecretAuth](../README.md#OrgSecretAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## UpdateLoadBalancer

> DtoLoadBalancerResponse UpdateLoadBalancer(ctx, id).DtoUpdateLoadBalancerRequest(dtoUpdateLoadBalancerRequest).XOrgID(xOrgID).Execute()

Update a load balancer (org scoped)

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
	id := "id_example" // string | Load Balancer ID (UUID)
	dtoUpdateLoadBalancerRequest := *openapiclient.NewDtoUpdateLoadBalancerRequest() // DtoUpdateLoadBalancerRequest | Fields to update
	xOrgID := "xOrgID_example" // string | Organization UUID (optional)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.LoadBalancersAPI.UpdateLoadBalancer(context.Background(), id).DtoUpdateLoadBalancerRequest(dtoUpdateLoadBalancerRequest).XOrgID(xOrgID).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `LoadBalancersAPI.UpdateLoadBalancer``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `UpdateLoadBalancer`: DtoLoadBalancerResponse
	fmt.Fprintf(os.Stdout, "Response from `LoadBalancersAPI.UpdateLoadBalancer`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Load Balancer ID (UUID) | 

### Other Parameters

Other parameters are passed through a pointer to a apiUpdateLoadBalancerRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **dtoUpdateLoadBalancerRequest** | [**DtoUpdateLoadBalancerRequest**](DtoUpdateLoadBalancerRequest.md) | Fields to update | 
 **xOrgID** | **string** | Organization UUID | 

### Return type

[**DtoLoadBalancerResponse**](DtoLoadBalancerResponse.md)

### Authorization

[OrgKeyAuth](../README.md#OrgKeyAuth), [OrgSecretAuth](../README.md#OrgSecretAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)

