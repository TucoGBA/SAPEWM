## Define Packing Profile for Warehouse Order Creation
### Use

In this IMG activity, you define packing profiles for warehouse order creation. This enables you to control how warehouse order creation determines pick-handling units for a warehouse order. The system uses the data from the warehouse tasks (WTs) of a warehouse order (such as weight, volume, or dimensions) in order to perform this determination. It compares this data with the possible packaging materials, and determines the number and category of the required pick-handling units. In addition to these values, when determining the pick-handling units, the system also considers the following additional values from your definition of limit values for the size of a warehouse order:

- Maximum number of different deconsolidation groups in a pick-handling unit
- Maximum number of pick-handling units
- Maximum number of items for each handling unit
- Minimum number of items for each handling unit

The following modes are available for determining the pick-handling units:

- Simple algorithm
- Complex algorithm
- BAdI

### Prerequisites

If you enter Simple algorithm or Complex algorithm as the mode, you must also define the relevant packaging specifications in the system. There you specify the desired packaging material and can, if required, manually overwrite the capacity data. In addition, when determining the packing specification, you must indicate the sequence number of the conditions according to the size of the packaging material (from small to large). For the simple algorithm, you can only define one packaging specification with one packaging material per packing profile.

In the area menu, choose ```Extended Warehouse Management -> Master Data > Packaging Specifications -> Maintain Packaging Specifications.```

### Activities

Define the required packing profile for warehouse order creation.

If you use the simple algorithm or packing specifications to determine the pick-handling units for a warehouse order, the following parameters are available for more detailed definition:

- Use Sorting to specify the sorting that you previously defined in Define Sort Rules for Warehouse Tasks. Before determining the pick-handling units, warehouse order creation sorts the WTs according to this predefined sort sequence.
- Set Create HUs as required.
- Set Assign WTs to HUs as required.
- Choose Split WT as required, in order to permit splitting of WTs.
 -Choose Split AUoM to let the system split WTs with regards to the alternative UoM of the WT. If you choose this, the system will split WTs only with integer values in the quantity in alternative UoM. In other words, if a WT has a carton as alternative UoM it will not force the picker to open this carton and remove individual pieces.
- Set Skip WT as required, in order that warehouse order creation should skip a WT if it no longer fits into the pick-handling unit.
- Set Check LWH as required, if warehouse order creation should also consider the length, width, and height when determining the pick-handling units.
