# Authentication
(*Authentication*)

## Overview

The authentication endpoints.

### Available Operations

* [Authenticate](#authenticate) - Authenticate with the API by providing a username and password.

## Authenticate

Authenticate with the API by providing a username and password.

### Example Usage

```go
package main

import(
	"context"
	"log"
	templatespeakeasybar "github.com/speakeasy-sdks/template-speakeasy-bar"
	"github.com/speakeasy-sdks/template-speakeasy-bar/pkg/models/shared"
	"github.com/speakeasy-sdks/template-speakeasy-bar/pkg/models/operations"
)

func main() {
    s := templatespeakeasybar.New(
        templatespeakeasybar.WithSecurity(""),
    )

    ctx := context.Background()
    res, err := s.Authentication.Authenticate(ctx, operations.AuthenticateRequestBody{})
    if err != nil {
        log.Fatal(err)
    }

    if res.Authenticate200ApplicationJSONObject != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                                | Type                                                                                     | Required                                                                                 | Description                                                                              |
| ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- |
| `ctx`                                                                                    | [context.Context](https://pkg.go.dev/context#Context)                                    | :heavy_check_mark:                                                                       | The context to use for the request.                                                      |
| `request`                                                                                | [operations.AuthenticateRequestBody](../../models/operations/authenticaterequestbody.md) | :heavy_check_mark:                                                                       | The request object to use for the request.                                               |


### Response

**[*operations.AuthenticateResponse](../../models/operations/authenticateresponse.md), error**

