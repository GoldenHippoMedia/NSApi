# Sales Order

## Update Commitment Status

```javascript
//Include in defines
define(["../ghmfiles/gh_salesOrderLib"], function (gh_salesOrderLib) {

//Sample in use
    var soId = 1;
    var commitStatus = 1;
    var commitResults = gh_salesOrderLib.updateAllCommitments(soId, commitStatus); //30 Units
})
```

```typescript
//Include in imports
import {updateAllCommitments} from "../ghmfiles/gh_salesOrderLib";

//Sample in use
let soId = 1;
let commitStatus = 1;
let commitResults = updateAllCommitments(soId, commitStatus);
```

Set the commitment value on all line items of an order. 

This requires providing the internal ID of the Sales Order as a number and the internal ID of the commitment status as a number (refer to table below)

* 30 Governance Units

* @param orderId

* @param commitStatus


### Commitment Status
Use this table to determine the commitment status you would like to pass.

Status  | Internal ID
--------- | ------- 
Available Quantity | 0
Complete Quantity | 1
Do Not Commit | 2

