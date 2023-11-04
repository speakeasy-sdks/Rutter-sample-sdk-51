# Drinks
(*Drinks*)

## Overview

The drinks endpoints.

### Available Operations

* [GetDrink](#getdrink) - Get a drink.
* [ListDrinks](#listdrinks) - Get a list of drinks.

## GetDrink

Get a drink by name, if authenticated this will include stock levels and product codes otherwise it will only include public information.

### Example Usage

```go
package main

import(
	"context"
	"log"
	templatespeakeasybar "github.com/speakeasy-sdks/template-speakeasy-bar"
	"github.com/speakeasy-sdks/template-speakeasy-bar/pkg/models/shared"
)

func main() {
    s := templatespeakeasybar.New(
        templatespeakeasybar.WithSecurity(""),
    )


    var name string = "string"

    ctx := context.Background()
    res, err := s.Drinks.GetDrink(ctx, name)
    if err != nil {
        log.Fatal(err)
    }

    if res.Drink != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                             | Type                                                  | Required                                              | Description                                           |
| ----------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- |
| `ctx`                                                 | [context.Context](https://pkg.go.dev/context#Context) | :heavy_check_mark:                                    | The context to use for the request.                   |
| `name`                                                | *string*                                              | :heavy_check_mark:                                    | N/A                                                   |


### Response

**[*operations.GetDrinkResponse](../../models/operations/getdrinkresponse.md), error**


## ListDrinks

Get a list of drinks, if authenticated this will include stock levels and product codes otherwise it will only include public information.

### Example Usage

```go
package main

import(
	"context"
	"log"
	templatespeakeasybar "github.com/speakeasy-sdks/template-speakeasy-bar"
	"github.com/speakeasy-sdks/template-speakeasy-bar/pkg/models/shared"
)

func main() {
    s := templatespeakeasybar.New(
        templatespeakeasybar.WithSecurity(""),
    )


    var drinkType *shared.DrinkType = shared.DrinkTypeSpirit

    ctx := context.Background()
    res, err := s.Drinks.ListDrinks(ctx, drinkType)
    if err != nil {
        log.Fatal(err)
    }

    if res.Drinks != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                    | Type                                                                         | Required                                                                     | Description                                                                  |
| ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| `ctx`                                                                        | [context.Context](https://pkg.go.dev/context#Context)                        | :heavy_check_mark:                                                           | The context to use for the request.                                          |
| `drinkType`                                                                  | [*shared.DrinkType](../../models/shared/drinktype.md)                        | :heavy_minus_sign:                                                           | The type of drink to filter by. If not provided all drinks will be returned. |


### Response

**[*operations.ListDrinksResponse](../../models/operations/listdrinksresponse.md), error**

