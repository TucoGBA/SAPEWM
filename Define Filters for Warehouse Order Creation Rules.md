## Define Filters for Warehouse Order Creation Rules
### Use

You can define filters for warehouse order creation rules. In this way, you specify whether warehouse order creation uses a rule to process a warehouse task. Warehouse order creation uses the filters on all warehouse tasks that you haven't yet assigned to a warehouse order, and which it should process.

### Standard settings

In the standard system, filters are already defined for warehouse number 0001.

### Activities

#### Define your filters.

Choose the warehouse number and enter a filter for warehouse order creation.
Select the filter type and define your item filters or subtotal filters.
Item Filter
Some possible filter criteria for the item filter at item level:
Minimum volume to maximum volume
Minimum weight to maximum weight
Minimum processing time to maximum processing time
Alternative unit of measure
Warehouse process category
Route
Wave category
Full pallet withdrawal
If you don't want warehouse order creation to use the current warehouse order creation rule to process warehouse tasks containing one of the transfer types "putaway", "stock removal", "internal stock transfer", or "physical inventory", set the relevant indicator in the filter definition, that is, No Putaway, No Stock Removal, No Internal Stock Movement, or No Physical Inventory.
Warehouse order creation processes the warehouse order creation rules for this warehouse task according to the search sequence for warehouse order creation rules for each activity area. If your filter criteria don't match the warehouse task to process, then warehouse order creation doesn't continue processing. Instead, if you've defined other rules, then it checks the filters using the next rule.
Subtotal Filter
Some possible filter criteria for the subtotal filter:
Minimum volume to maximum volume
Minimum weight to maximum weight
Minimum processing time to maximum processing time
Minimum number of items to maximum number of items
If you enter values for the forbidden filter criteria, warehouse order creation doesn't take them into account.
If you want to define subtotal filters, you must have defined consolidation groups, because warehouse order creation calculates the subtotal for each consolidation group.
Warehouse order creation processes the warehouse order creation rules for these warehouse tasks for the subtotal, according to the search sequence for warehouse order creation rules for each activity area. If your filter criteria don't match the item filter or subtotal filter for the warehouse tasks to process, warehouse order creation doesn't continue processing. Depending on your settings, it checks whether it should use a different warehouse order creation rule for the warehouse tasks that have not yet been processed.
