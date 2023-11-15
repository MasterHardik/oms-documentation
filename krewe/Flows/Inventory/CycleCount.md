# Cycle Count

This document includes mappings and configurations related to the cycle count sync from HotWax to NetSuite

## Default Mappings
These are the default values that are sent to NetSuite unless a flow overrides them.
| Variable Name               | Value                            |
|-----------------------------|----------------------------------|
| default.adjustmentAccount   | 927                              |
| default.subsidiary          | 1                                |
| #{default.memo}             | Inventory cycle count by HotWax  |

## FTP locations
These are the FTP locations where cycle count files are placed when exported from HotWax
| Variable Name                                 | Value                                            |
|-----------------------------------------------|--------------------------------------------------|
| destination.inv.cycle.count.feed.sftp.path     | netsuite/inventoryadjustment/csv                 |
| destination.log.inv.cycle.count.feed.sftp.path | nifi-feed-logs/netsuite/inventorycyclecountvariance |
| feed.fileName.withPrefix                       | Krewe_InventoryCycleCountVarianceFeed_            |
| hotwax.inv.cycle.count.feed.sftp.path          | hotwax/InventoryCycleCountVariance                |
| hotwax.inv.cycle.count.feed.sftp.path.archive  | hotwax/InventoryCycleCountVariance/archive        |

These are the FTP locations for pushing inventory variances recorded in store to NetSuite from HotWax
| Variable Name                                      | Value                                            |
|----------------------------------------------------|--------------------------------------------------|
| destination.inv.item.variance.feed.sftp.path        | netsuite/inventoryadjustment/csv                 |
| destination.log.inv.item.variance.feed.sftp.path    | nifi-feed-logs/netsuite/inventoryadjustment/csv |
| feed.fileName.withPrefix                            | Krewe_InventoryItemVarianceFeed_                 |
| hotwax.inv.item.variance.feed.sftp.path             | hotwax/InventoryItemVarianceFeed                 |
| hotwax.inv.item.variance.feed.sftp.path.archive     | hotwax/InventoryItemVarianceFeed/archive         |