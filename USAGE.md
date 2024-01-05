<!-- Start SDK Example Usage [usage] -->
```go
package main

import (
	"context"
	templatespeakeasybar "github.com/speakeasy-sdks/template-speakeasy-bar"
	"github.com/speakeasy-sdks/template-speakeasy-bar/pkg/models/shared"
	"log"
)

func main() {
	s := templatespeakeasybar.New()

	var drinkType *shared.DrinkType = shared.DrinkTypeSpirit

	ctx := context.Background()
	res, err := s.Drinks.ListDrinks(ctx, drinkType)
	if err != nil {
		log.Fatal(err)
	}

	if res.Classes != nil {
		// handle response
	}
}

```
<!-- End SDK Example Usage [usage] -->