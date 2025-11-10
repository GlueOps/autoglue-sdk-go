# \MetaAPI

All URIs are relative to */api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**VersionOperationId**](MetaAPI.md#VersionOperationId) | **Get** /version | Service version information



## VersionOperationId

> HandlersVersionResponse VersionOperationId(ctx).Execute()

Service version information



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

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.MetaAPI.VersionOperationId(context.Background()).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `MetaAPI.VersionOperationId``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `VersionOperationId`: HandlersVersionResponse
	fmt.Fprintf(os.Stdout, "Response from `MetaAPI.VersionOperationId`: %v\n", resp)
}
```

### Path Parameters

This endpoint does not need any parameter.

### Other Parameters

Other parameters are passed through a pointer to a apiVersionOperationIdRequest struct via the builder pattern


### Return type

[**HandlersVersionResponse**](HandlersVersionResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)

