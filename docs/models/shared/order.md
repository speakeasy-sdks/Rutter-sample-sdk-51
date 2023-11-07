# Order

An order for a drink or ingredient.


## Fields

| Field                                                    | Type                                                     | Required                                                 | Description                                              | Example                                                  |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `ProductCode`                                            | *string*                                                 | :heavy_check_mark:                                       | The product code of the drink or ingredient.             | AC-A2DF3                                                 |
| `Quantity`                                               | *int64*                                                  | :heavy_check_mark:                                       | The number of units of the drink or ingredient to order. |                                                          |
| `Status`                                                 | [shared.Status](../../models/shared/status.md)           | :heavy_check_mark:                                       | The status of the order.                                 |                                                          |
| `Type`                                                   | [shared.OrderType](../../models/shared/ordertype.md)     | :heavy_check_mark:                                       | The type of order.                                       |                                                          |