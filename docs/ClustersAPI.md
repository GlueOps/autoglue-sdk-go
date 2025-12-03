# \ClustersAPI

All URIs are relative to *https://autoglue.glueopshosted.com/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**AttachAppsLoadBalancer**](ClustersAPI.md#AttachAppsLoadBalancer) | **Post** /clusters/{clusterID}/apps-load-balancer | Attach an apps load balancer to a cluster
[**AttachBastionServer**](ClustersAPI.md#AttachBastionServer) | **Post** /clusters/{clusterID}/bastion | Attach a bastion server to a cluster
[**AttachCaptainDomain**](ClustersAPI.md#AttachCaptainDomain) | **Post** /clusters/{clusterID}/captain-domain | Attach a captain domain to a cluster
[**AttachControlPlaneRecordSet**](ClustersAPI.md#AttachControlPlaneRecordSet) | **Post** /clusters/{clusterID}/control-plane-record-set | Attach a control plane record set to a cluster
[**AttachGlueOpsLoadBalancer**](ClustersAPI.md#AttachGlueOpsLoadBalancer) | **Post** /clusters/{clusterID}/glueops-load-balancer | Attach a GlueOps/control-plane load balancer to a cluster
[**AttachNodePool**](ClustersAPI.md#AttachNodePool) | **Post** /clusters/{clusterID}/node-pools | Attach a node pool to a cluster
[**ClearClusterKubeconfig**](ClustersAPI.md#ClearClusterKubeconfig) | **Delete** /clusters/{clusterID}/kubeconfig | Clear the kubeconfig for a cluster
[**CreateCluster**](ClustersAPI.md#CreateCluster) | **Post** /clusters | Create cluster (org scoped)
[**DeleteCluster**](ClustersAPI.md#DeleteCluster) | **Delete** /clusters/{clusterID} | Delete a cluster (org scoped)
[**DetachAppsLoadBalancer**](ClustersAPI.md#DetachAppsLoadBalancer) | **Delete** /clusters/{clusterID}/apps-load-balancer | Detach the apps load balancer from a cluster
[**DetachBastionServer**](ClustersAPI.md#DetachBastionServer) | **Delete** /clusters/{clusterID}/bastion | Detach the bastion server from a cluster
[**DetachCaptainDomain**](ClustersAPI.md#DetachCaptainDomain) | **Delete** /clusters/{clusterID}/captain-domain | Detach the captain domain from a cluster
[**DetachControlPlaneRecordSet**](ClustersAPI.md#DetachControlPlaneRecordSet) | **Delete** /clusters/{clusterID}/control-plane-record-set | Detach the control plane record set from a cluster
[**DetachGlueOpsLoadBalancer**](ClustersAPI.md#DetachGlueOpsLoadBalancer) | **Delete** /clusters/{clusterID}/glueops-load-balancer | Detach the GlueOps/control-plane load balancer from a cluster
[**DetachNodePool**](ClustersAPI.md#DetachNodePool) | **Delete** /clusters/{clusterID}/node-pools/{nodePoolID} | Detach a node pool from a cluster
[**GetCluster**](ClustersAPI.md#GetCluster) | **Get** /clusters/{clusterID} | Get a single cluster by ID (org scoped)
[**ListClusters**](ClustersAPI.md#ListClusters) | **Get** /clusters | List clusters (org scoped)
[**SetClusterKubeconfig**](ClustersAPI.md#SetClusterKubeconfig) | **Post** /clusters/{clusterID}/kubeconfig | Set (or replace) the kubeconfig for a cluster
[**UpdateCluster**](ClustersAPI.md#UpdateCluster) | **Patch** /clusters/{clusterID} | Update basic cluster details (org scoped)



## AttachAppsLoadBalancer

> DtoClusterResponse AttachAppsLoadBalancer(ctx, clusterID).DtoAttachLoadBalancerRequest(dtoAttachLoadBalancerRequest).XOrgID(xOrgID).Execute()

Attach an apps load balancer to a cluster



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
	clusterID := "clusterID_example" // string | Cluster ID
	dtoAttachLoadBalancerRequest := *openapiclient.NewDtoAttachLoadBalancerRequest() // DtoAttachLoadBalancerRequest | payload
	xOrgID := "xOrgID_example" // string | Organization UUID (optional)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.ClustersAPI.AttachAppsLoadBalancer(context.Background(), clusterID).DtoAttachLoadBalancerRequest(dtoAttachLoadBalancerRequest).XOrgID(xOrgID).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ClustersAPI.AttachAppsLoadBalancer``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `AttachAppsLoadBalancer`: DtoClusterResponse
	fmt.Fprintf(os.Stdout, "Response from `ClustersAPI.AttachAppsLoadBalancer`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**clusterID** | **string** | Cluster ID | 

### Other Parameters

Other parameters are passed through a pointer to a apiAttachAppsLoadBalancerRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **dtoAttachLoadBalancerRequest** | [**DtoAttachLoadBalancerRequest**](DtoAttachLoadBalancerRequest.md) | payload | 
 **xOrgID** | **string** | Organization UUID | 

### Return type

[**DtoClusterResponse**](DtoClusterResponse.md)

### Authorization

[OrgKeyAuth](../README.md#OrgKeyAuth), [OrgSecretAuth](../README.md#OrgSecretAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## AttachBastionServer

> DtoClusterResponse AttachBastionServer(ctx, clusterID).DtoAttachBastionRequest(dtoAttachBastionRequest).XOrgID(xOrgID).Execute()

Attach a bastion server to a cluster



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
	clusterID := "clusterID_example" // string | Cluster ID
	dtoAttachBastionRequest := *openapiclient.NewDtoAttachBastionRequest() // DtoAttachBastionRequest | payload
	xOrgID := "xOrgID_example" // string | Organization UUID (optional)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.ClustersAPI.AttachBastionServer(context.Background(), clusterID).DtoAttachBastionRequest(dtoAttachBastionRequest).XOrgID(xOrgID).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ClustersAPI.AttachBastionServer``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `AttachBastionServer`: DtoClusterResponse
	fmt.Fprintf(os.Stdout, "Response from `ClustersAPI.AttachBastionServer`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**clusterID** | **string** | Cluster ID | 

### Other Parameters

Other parameters are passed through a pointer to a apiAttachBastionServerRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **dtoAttachBastionRequest** | [**DtoAttachBastionRequest**](DtoAttachBastionRequest.md) | payload | 
 **xOrgID** | **string** | Organization UUID | 

### Return type

[**DtoClusterResponse**](DtoClusterResponse.md)

### Authorization

[OrgKeyAuth](../README.md#OrgKeyAuth), [OrgSecretAuth](../README.md#OrgSecretAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## AttachCaptainDomain

> DtoClusterResponse AttachCaptainDomain(ctx, clusterID).DtoAttachCaptainDomainRequest(dtoAttachCaptainDomainRequest).XOrgID(xOrgID).Execute()

Attach a captain domain to a cluster



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
	clusterID := "clusterID_example" // string | Cluster ID
	dtoAttachCaptainDomainRequest := *openapiclient.NewDtoAttachCaptainDomainRequest() // DtoAttachCaptainDomainRequest | payload
	xOrgID := "xOrgID_example" // string | Organization UUID (optional)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.ClustersAPI.AttachCaptainDomain(context.Background(), clusterID).DtoAttachCaptainDomainRequest(dtoAttachCaptainDomainRequest).XOrgID(xOrgID).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ClustersAPI.AttachCaptainDomain``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `AttachCaptainDomain`: DtoClusterResponse
	fmt.Fprintf(os.Stdout, "Response from `ClustersAPI.AttachCaptainDomain`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**clusterID** | **string** | Cluster ID | 

### Other Parameters

Other parameters are passed through a pointer to a apiAttachCaptainDomainRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **dtoAttachCaptainDomainRequest** | [**DtoAttachCaptainDomainRequest**](DtoAttachCaptainDomainRequest.md) | payload | 
 **xOrgID** | **string** | Organization UUID | 

### Return type

[**DtoClusterResponse**](DtoClusterResponse.md)

### Authorization

[OrgKeyAuth](../README.md#OrgKeyAuth), [OrgSecretAuth](../README.md#OrgSecretAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## AttachControlPlaneRecordSet

> DtoClusterResponse AttachControlPlaneRecordSet(ctx, clusterID).DtoAttachRecordSetRequest(dtoAttachRecordSetRequest).XOrgID(xOrgID).Execute()

Attach a control plane record set to a cluster



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
	clusterID := "clusterID_example" // string | Cluster ID
	dtoAttachRecordSetRequest := *openapiclient.NewDtoAttachRecordSetRequest() // DtoAttachRecordSetRequest | payload
	xOrgID := "xOrgID_example" // string | Organization UUID (optional)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.ClustersAPI.AttachControlPlaneRecordSet(context.Background(), clusterID).DtoAttachRecordSetRequest(dtoAttachRecordSetRequest).XOrgID(xOrgID).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ClustersAPI.AttachControlPlaneRecordSet``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `AttachControlPlaneRecordSet`: DtoClusterResponse
	fmt.Fprintf(os.Stdout, "Response from `ClustersAPI.AttachControlPlaneRecordSet`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**clusterID** | **string** | Cluster ID | 

### Other Parameters

Other parameters are passed through a pointer to a apiAttachControlPlaneRecordSetRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **dtoAttachRecordSetRequest** | [**DtoAttachRecordSetRequest**](DtoAttachRecordSetRequest.md) | payload | 
 **xOrgID** | **string** | Organization UUID | 

### Return type

[**DtoClusterResponse**](DtoClusterResponse.md)

### Authorization

[OrgKeyAuth](../README.md#OrgKeyAuth), [OrgSecretAuth](../README.md#OrgSecretAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## AttachGlueOpsLoadBalancer

> DtoClusterResponse AttachGlueOpsLoadBalancer(ctx, clusterID).DtoAttachLoadBalancerRequest(dtoAttachLoadBalancerRequest).XOrgID(xOrgID).Execute()

Attach a GlueOps/control-plane load balancer to a cluster



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
	clusterID := "clusterID_example" // string | Cluster ID
	dtoAttachLoadBalancerRequest := *openapiclient.NewDtoAttachLoadBalancerRequest() // DtoAttachLoadBalancerRequest | payload
	xOrgID := "xOrgID_example" // string | Organization UUID (optional)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.ClustersAPI.AttachGlueOpsLoadBalancer(context.Background(), clusterID).DtoAttachLoadBalancerRequest(dtoAttachLoadBalancerRequest).XOrgID(xOrgID).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ClustersAPI.AttachGlueOpsLoadBalancer``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `AttachGlueOpsLoadBalancer`: DtoClusterResponse
	fmt.Fprintf(os.Stdout, "Response from `ClustersAPI.AttachGlueOpsLoadBalancer`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**clusterID** | **string** | Cluster ID | 

### Other Parameters

Other parameters are passed through a pointer to a apiAttachGlueOpsLoadBalancerRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **dtoAttachLoadBalancerRequest** | [**DtoAttachLoadBalancerRequest**](DtoAttachLoadBalancerRequest.md) | payload | 
 **xOrgID** | **string** | Organization UUID | 

### Return type

[**DtoClusterResponse**](DtoClusterResponse.md)

### Authorization

[OrgKeyAuth](../README.md#OrgKeyAuth), [OrgSecretAuth](../README.md#OrgSecretAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## AttachNodePool

> DtoClusterResponse AttachNodePool(ctx, clusterID).DtoAttachNodePoolRequest(dtoAttachNodePoolRequest).XOrgID(xOrgID).Execute()

Attach a node pool to a cluster



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
	clusterID := "clusterID_example" // string | Cluster ID
	dtoAttachNodePoolRequest := *openapiclient.NewDtoAttachNodePoolRequest() // DtoAttachNodePoolRequest | payload
	xOrgID := "xOrgID_example" // string | Organization UUID (optional)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.ClustersAPI.AttachNodePool(context.Background(), clusterID).DtoAttachNodePoolRequest(dtoAttachNodePoolRequest).XOrgID(xOrgID).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ClustersAPI.AttachNodePool``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `AttachNodePool`: DtoClusterResponse
	fmt.Fprintf(os.Stdout, "Response from `ClustersAPI.AttachNodePool`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**clusterID** | **string** | Cluster ID | 

### Other Parameters

Other parameters are passed through a pointer to a apiAttachNodePoolRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **dtoAttachNodePoolRequest** | [**DtoAttachNodePoolRequest**](DtoAttachNodePoolRequest.md) | payload | 
 **xOrgID** | **string** | Organization UUID | 

### Return type

[**DtoClusterResponse**](DtoClusterResponse.md)

### Authorization

[OrgKeyAuth](../README.md#OrgKeyAuth), [OrgSecretAuth](../README.md#OrgSecretAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ClearClusterKubeconfig

> DtoClusterResponse ClearClusterKubeconfig(ctx, clusterID).XOrgID(xOrgID).Execute()

Clear the kubeconfig for a cluster



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
	clusterID := "clusterID_example" // string | Cluster ID
	xOrgID := "xOrgID_example" // string | Organization UUID (optional)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.ClustersAPI.ClearClusterKubeconfig(context.Background(), clusterID).XOrgID(xOrgID).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ClustersAPI.ClearClusterKubeconfig``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ClearClusterKubeconfig`: DtoClusterResponse
	fmt.Fprintf(os.Stdout, "Response from `ClustersAPI.ClearClusterKubeconfig`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**clusterID** | **string** | Cluster ID | 

### Other Parameters

Other parameters are passed through a pointer to a apiClearClusterKubeconfigRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xOrgID** | **string** | Organization UUID | 

### Return type

[**DtoClusterResponse**](DtoClusterResponse.md)

### Authorization

[OrgKeyAuth](../README.md#OrgKeyAuth), [OrgSecretAuth](../README.md#OrgSecretAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## CreateCluster

> DtoClusterResponse CreateCluster(ctx).DtoCreateClusterRequest(dtoCreateClusterRequest).XOrgID(xOrgID).Execute()

Create cluster (org scoped)



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
	dtoCreateClusterRequest := *openapiclient.NewDtoCreateClusterRequest() // DtoCreateClusterRequest | payload
	xOrgID := "xOrgID_example" // string | Organization UUID (optional)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.ClustersAPI.CreateCluster(context.Background()).DtoCreateClusterRequest(dtoCreateClusterRequest).XOrgID(xOrgID).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ClustersAPI.CreateCluster``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `CreateCluster`: DtoClusterResponse
	fmt.Fprintf(os.Stdout, "Response from `ClustersAPI.CreateCluster`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiCreateClusterRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **dtoCreateClusterRequest** | [**DtoCreateClusterRequest**](DtoCreateClusterRequest.md) | payload | 
 **xOrgID** | **string** | Organization UUID | 

### Return type

[**DtoClusterResponse**](DtoClusterResponse.md)

### Authorization

[OrgKeyAuth](../README.md#OrgKeyAuth), [OrgSecretAuth](../README.md#OrgSecretAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## DeleteCluster

> string DeleteCluster(ctx, clusterID).XOrgID(xOrgID).Execute()

Delete a cluster (org scoped)



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
	clusterID := "clusterID_example" // string | Cluster ID
	xOrgID := "xOrgID_example" // string | Organization UUID (optional)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.ClustersAPI.DeleteCluster(context.Background(), clusterID).XOrgID(xOrgID).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ClustersAPI.DeleteCluster``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `DeleteCluster`: string
	fmt.Fprintf(os.Stdout, "Response from `ClustersAPI.DeleteCluster`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**clusterID** | **string** | Cluster ID | 

### Other Parameters

Other parameters are passed through a pointer to a apiDeleteClusterRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xOrgID** | **string** | Organization UUID | 

### Return type

**string**

### Authorization

[OrgKeyAuth](../README.md#OrgKeyAuth), [OrgSecretAuth](../README.md#OrgSecretAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## DetachAppsLoadBalancer

> DtoClusterResponse DetachAppsLoadBalancer(ctx, clusterID).XOrgID(xOrgID).Execute()

Detach the apps load balancer from a cluster



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
	clusterID := "clusterID_example" // string | Cluster ID
	xOrgID := "xOrgID_example" // string | Organization UUID (optional)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.ClustersAPI.DetachAppsLoadBalancer(context.Background(), clusterID).XOrgID(xOrgID).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ClustersAPI.DetachAppsLoadBalancer``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `DetachAppsLoadBalancer`: DtoClusterResponse
	fmt.Fprintf(os.Stdout, "Response from `ClustersAPI.DetachAppsLoadBalancer`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**clusterID** | **string** | Cluster ID | 

### Other Parameters

Other parameters are passed through a pointer to a apiDetachAppsLoadBalancerRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xOrgID** | **string** | Organization UUID | 

### Return type

[**DtoClusterResponse**](DtoClusterResponse.md)

### Authorization

[OrgKeyAuth](../README.md#OrgKeyAuth), [OrgSecretAuth](../README.md#OrgSecretAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## DetachBastionServer

> DtoClusterResponse DetachBastionServer(ctx, clusterID).XOrgID(xOrgID).Execute()

Detach the bastion server from a cluster



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
	clusterID := "clusterID_example" // string | Cluster ID
	xOrgID := "xOrgID_example" // string | Organization UUID (optional)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.ClustersAPI.DetachBastionServer(context.Background(), clusterID).XOrgID(xOrgID).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ClustersAPI.DetachBastionServer``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `DetachBastionServer`: DtoClusterResponse
	fmt.Fprintf(os.Stdout, "Response from `ClustersAPI.DetachBastionServer`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**clusterID** | **string** | Cluster ID | 

### Other Parameters

Other parameters are passed through a pointer to a apiDetachBastionServerRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xOrgID** | **string** | Organization UUID | 

### Return type

[**DtoClusterResponse**](DtoClusterResponse.md)

### Authorization

[OrgKeyAuth](../README.md#OrgKeyAuth), [OrgSecretAuth](../README.md#OrgSecretAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## DetachCaptainDomain

> DtoClusterResponse DetachCaptainDomain(ctx, clusterID).XOrgID(xOrgID).Execute()

Detach the captain domain from a cluster



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
	clusterID := "clusterID_example" // string | Cluster ID
	xOrgID := "xOrgID_example" // string | Organization UUID (optional)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.ClustersAPI.DetachCaptainDomain(context.Background(), clusterID).XOrgID(xOrgID).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ClustersAPI.DetachCaptainDomain``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `DetachCaptainDomain`: DtoClusterResponse
	fmt.Fprintf(os.Stdout, "Response from `ClustersAPI.DetachCaptainDomain`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**clusterID** | **string** | Cluster ID | 

### Other Parameters

Other parameters are passed through a pointer to a apiDetachCaptainDomainRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xOrgID** | **string** | Organization UUID | 

### Return type

[**DtoClusterResponse**](DtoClusterResponse.md)

### Authorization

[OrgKeyAuth](../README.md#OrgKeyAuth), [OrgSecretAuth](../README.md#OrgSecretAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## DetachControlPlaneRecordSet

> DtoClusterResponse DetachControlPlaneRecordSet(ctx, clusterID).XOrgID(xOrgID).Execute()

Detach the control plane record set from a cluster



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
	clusterID := "clusterID_example" // string | Cluster ID
	xOrgID := "xOrgID_example" // string | Organization UUID (optional)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.ClustersAPI.DetachControlPlaneRecordSet(context.Background(), clusterID).XOrgID(xOrgID).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ClustersAPI.DetachControlPlaneRecordSet``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `DetachControlPlaneRecordSet`: DtoClusterResponse
	fmt.Fprintf(os.Stdout, "Response from `ClustersAPI.DetachControlPlaneRecordSet`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**clusterID** | **string** | Cluster ID | 

### Other Parameters

Other parameters are passed through a pointer to a apiDetachControlPlaneRecordSetRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xOrgID** | **string** | Organization UUID | 

### Return type

[**DtoClusterResponse**](DtoClusterResponse.md)

### Authorization

[OrgKeyAuth](../README.md#OrgKeyAuth), [OrgSecretAuth](../README.md#OrgSecretAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## DetachGlueOpsLoadBalancer

> DtoClusterResponse DetachGlueOpsLoadBalancer(ctx, clusterID).XOrgID(xOrgID).Execute()

Detach the GlueOps/control-plane load balancer from a cluster



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
	clusterID := "clusterID_example" // string | Cluster ID
	xOrgID := "xOrgID_example" // string | Organization UUID (optional)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.ClustersAPI.DetachGlueOpsLoadBalancer(context.Background(), clusterID).XOrgID(xOrgID).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ClustersAPI.DetachGlueOpsLoadBalancer``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `DetachGlueOpsLoadBalancer`: DtoClusterResponse
	fmt.Fprintf(os.Stdout, "Response from `ClustersAPI.DetachGlueOpsLoadBalancer`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**clusterID** | **string** | Cluster ID | 

### Other Parameters

Other parameters are passed through a pointer to a apiDetachGlueOpsLoadBalancerRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xOrgID** | **string** | Organization UUID | 

### Return type

[**DtoClusterResponse**](DtoClusterResponse.md)

### Authorization

[OrgKeyAuth](../README.md#OrgKeyAuth), [OrgSecretAuth](../README.md#OrgSecretAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## DetachNodePool

> DtoClusterResponse DetachNodePool(ctx, clusterID, nodePoolID).XOrgID(xOrgID).Execute()

Detach a node pool from a cluster



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
	clusterID := "clusterID_example" // string | Cluster ID
	nodePoolID := "nodePoolID_example" // string | Node Pool ID
	xOrgID := "xOrgID_example" // string | Organization UUID (optional)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.ClustersAPI.DetachNodePool(context.Background(), clusterID, nodePoolID).XOrgID(xOrgID).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ClustersAPI.DetachNodePool``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `DetachNodePool`: DtoClusterResponse
	fmt.Fprintf(os.Stdout, "Response from `ClustersAPI.DetachNodePool`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**clusterID** | **string** | Cluster ID | 
**nodePoolID** | **string** | Node Pool ID | 

### Other Parameters

Other parameters are passed through a pointer to a apiDetachNodePoolRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **xOrgID** | **string** | Organization UUID | 

### Return type

[**DtoClusterResponse**](DtoClusterResponse.md)

### Authorization

[OrgKeyAuth](../README.md#OrgKeyAuth), [OrgSecretAuth](../README.md#OrgSecretAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetCluster

> DtoClusterResponse GetCluster(ctx, clusterID).XOrgID(xOrgID).Execute()

Get a single cluster by ID (org scoped)



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
	clusterID := "clusterID_example" // string | Cluster ID
	xOrgID := "xOrgID_example" // string | Organization UUID (optional)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.ClustersAPI.GetCluster(context.Background(), clusterID).XOrgID(xOrgID).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ClustersAPI.GetCluster``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetCluster`: DtoClusterResponse
	fmt.Fprintf(os.Stdout, "Response from `ClustersAPI.GetCluster`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**clusterID** | **string** | Cluster ID | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetClusterRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **xOrgID** | **string** | Organization UUID | 

### Return type

[**DtoClusterResponse**](DtoClusterResponse.md)

### Authorization

[OrgKeyAuth](../README.md#OrgKeyAuth), [OrgSecretAuth](../README.md#OrgSecretAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ListClusters

> []DtoClusterResponse ListClusters(ctx).XOrgID(xOrgID).Q(q).Execute()

List clusters (org scoped)



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
	q := "q_example" // string | Name contains (case-insensitive) (optional)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.ClustersAPI.ListClusters(context.Background()).XOrgID(xOrgID).Q(q).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ClustersAPI.ListClusters``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListClusters`: []DtoClusterResponse
	fmt.Fprintf(os.Stdout, "Response from `ClustersAPI.ListClusters`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiListClustersRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **xOrgID** | **string** | Organization UUID | 
 **q** | **string** | Name contains (case-insensitive) | 

### Return type

[**[]DtoClusterResponse**](DtoClusterResponse.md)

### Authorization

[OrgKeyAuth](../README.md#OrgKeyAuth), [OrgSecretAuth](../README.md#OrgSecretAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## SetClusterKubeconfig

> DtoClusterResponse SetClusterKubeconfig(ctx, clusterID).DtoSetKubeconfigRequest(dtoSetKubeconfigRequest).XOrgID(xOrgID).Execute()

Set (or replace) the kubeconfig for a cluster



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
	clusterID := "clusterID_example" // string | Cluster ID
	dtoSetKubeconfigRequest := *openapiclient.NewDtoSetKubeconfigRequest() // DtoSetKubeconfigRequest | payload
	xOrgID := "xOrgID_example" // string | Organization UUID (optional)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.ClustersAPI.SetClusterKubeconfig(context.Background(), clusterID).DtoSetKubeconfigRequest(dtoSetKubeconfigRequest).XOrgID(xOrgID).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ClustersAPI.SetClusterKubeconfig``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `SetClusterKubeconfig`: DtoClusterResponse
	fmt.Fprintf(os.Stdout, "Response from `ClustersAPI.SetClusterKubeconfig`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**clusterID** | **string** | Cluster ID | 

### Other Parameters

Other parameters are passed through a pointer to a apiSetClusterKubeconfigRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **dtoSetKubeconfigRequest** | [**DtoSetKubeconfigRequest**](DtoSetKubeconfigRequest.md) | payload | 
 **xOrgID** | **string** | Organization UUID | 

### Return type

[**DtoClusterResponse**](DtoClusterResponse.md)

### Authorization

[OrgKeyAuth](../README.md#OrgKeyAuth), [OrgSecretAuth](../README.md#OrgSecretAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## UpdateCluster

> DtoClusterResponse UpdateCluster(ctx, clusterID).DtoUpdateClusterRequest(dtoUpdateClusterRequest).XOrgID(xOrgID).Execute()

Update basic cluster details (org scoped)



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
	clusterID := "clusterID_example" // string | Cluster ID
	dtoUpdateClusterRequest := *openapiclient.NewDtoUpdateClusterRequest() // DtoUpdateClusterRequest | payload
	xOrgID := "xOrgID_example" // string | Organization UUID (optional)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.ClustersAPI.UpdateCluster(context.Background(), clusterID).DtoUpdateClusterRequest(dtoUpdateClusterRequest).XOrgID(xOrgID).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ClustersAPI.UpdateCluster``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `UpdateCluster`: DtoClusterResponse
	fmt.Fprintf(os.Stdout, "Response from `ClustersAPI.UpdateCluster`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**clusterID** | **string** | Cluster ID | 

### Other Parameters

Other parameters are passed through a pointer to a apiUpdateClusterRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **dtoUpdateClusterRequest** | [**DtoUpdateClusterRequest**](DtoUpdateClusterRequest.md) | payload | 
 **xOrgID** | **string** | Organization UUID | 

### Return type

[**DtoClusterResponse**](DtoClusterResponse.md)

### Authorization

[OrgKeyAuth](../README.md#OrgKeyAuth), [OrgSecretAuth](../README.md#OrgSecretAuth), [BearerAuth](../README.md#BearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)

