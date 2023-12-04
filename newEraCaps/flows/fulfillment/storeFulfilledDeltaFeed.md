# Store Fulfilled Feed

The Store Fulfilled Feed is generated by the OMS and consumed by Flagship to ensure that inventory is accurately deducted in the POS after an order is packed for pickup or shipping.

While initially it was expected that this feed would be generated using the out of the box store fulfilled feed, that is now only being generated after order completion. Updating in store inventory is much more time sensitive so this feed is now generated separately at a higher frequency.

| Order Id | Product Id      | Facility Id | Quantity | Status Date      |
|----------|-----------------|-------------|----------|------------------|
| 90003910 | 4550538264826   | 5           | 1.000000 | 1701311309612    |
| 90003910 | 4550538173968   | 5           | 1.000000 | 1701311309612    |
| 90003910 | 4550538173968   | 5           | 1.000000 | 1701311309612    |
| 90003911 | 4550538138363   | 5           | 1.000000 | 1701311309621    |
| 90003912 | 4550236199499   | 5           | 1.000000 | 1701311309630    |
| 90003912 | 4550236540260   | 5           | 1.000000 | 1701311309630    |
| 90003908 | 4550236199475   | 3           | 1.000000 | 1701311354307    |
| 90003909 | 4550538056384   | 3           | 1.000000 | 1701311354315    |
| 90003909 | 4550538056148   | 3           | 1.000000 | 1701311354315    |
| 90003910 | 4550538145347   | 20          | 1.000000 | 1701311462160    |
| 90003914 | 4550538056285   | 5           | 1.000000 | 1701311582579    |
| 90003913 | 4550538204877   | 5           | 1.000000 | 1701311585933    |

1. **Order Id:** Unique identifier for each order by Shopify order name.
2. **Product Id:** Identifies the specific product in the order using the Shopify product SKU.
3. **Facility Id:** Represents the identifier of the store or facility from which the product is fulfilled. For this to work the internal ID of the facilities in the OMS and Smaregi must be the same. Otherwise custom facility identification types would have to be used.
4. **Quantity:** The quantity of the product fulfilled from the store inventory for the given order.
5. **Status Date:** Timestamp indicating the date and time when the order fulfillment status was updated in the system in an absolute number.