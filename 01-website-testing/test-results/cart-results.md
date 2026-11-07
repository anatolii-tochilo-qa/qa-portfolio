# Shopping Cart Test Results

| Test ID | Test Scenario | Expected Result | Actual Result | Status |
|---|---|---|---|---|
| CART-001 | Add Sauce Labs Backpack to cart | Cart badge shows 1; correct product, price and quantity are displayed | Badge: 1; Product: Sauce Labs Backpack; Price: $29.99; Quantity: 1 | PASS |
| CART-002 | Remove Sauce Labs Backpack from cart | Cart is empty; product page displays "Add to cart" | Cart is empty; product page displays "Add to cart" | PASS |
| CART-003 | Remove Sauce Labs Backpack from product details page | Product is removed from cart; button changes to "Add to cart" | Product was removed from cart; button changed to "Add to cart" | PASS |
| CART-004 | Add two different products to cart | Cart badge increases from 1 to 2 | Cart badge increased from 1 to 2 | PASS |
| CART-005 | Add product from product details page | Product is added to cart | Product was successfully added to cart | PASS |
| CART-006 | Remove product from catalog page | Product is removed from cart | Product was successfully removed from cart | PASS |
| CART-007 | Add and remove all six available products | All six products can be added and removed | All six products were successfully added and removed | PASS |
