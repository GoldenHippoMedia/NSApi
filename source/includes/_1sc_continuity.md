# 1SC Continuity

<aside class="success">

These functions are located in the GH_1scContinuityFunctions library.

</aside>

## Update Continuity Record

```javascript
//Include in defines
define(["../ghmfiles/GH_1scContinuityFunctions"], function (GH_1scContinuityFunctions){

//Sample in use
var recurringUpdate = GH_1scContinuityFunctions.updateRecurringOrder(recurringObject)
};
```


```typescript
//Include in imports
import {updateRecurringOrder} from '../ghmfiles/GH_1scContinuityFunctions'

//Sample in use
let recurringUpdate = updateRecurringOrder(recurringObject)
```

> recurringObject is a JSON object that is structured as such:

```json
{
    id: 123,
    brand: 456,
    mid: "midValue",
    apiKey: "apiKeyValue",
    status: "statusValue"
}
```

This function locates an existing recurring order, or creates one if it doesn't exist. It does not contact 1SC directly unless a new record is required.


 * 6 Governance Units
 
 * @param recurringRecord
 
#### Recurring Object Parameters

Parameter | Type | Description
--------- | ------- | -----------
id | number | This is the 1SC ID of the recurring record.
brand | number | This is the internal ID of the brand record that this record belongs to.
mid | string | The MID of the 1ShoppingCart cart this belongs to.
apiKey | string | The API Key generated from 1ShoppingCart for this cart listener.
status | string | (Optional) The status of the recurring record, required for update function.


## Create Continuity Record

```javascript
//Include in defines
define(["../ghmfiles/GH_1scContinuityFunctions"], function (GH_1scContinuityFunctions)

//Sample in use
var importRecurring = GH_1scContinuityFunctions.importRecurringOrder(recurringObject)
```


```typescript
//Include in imports
import {importRecurringOrder} from '../ghmfiles/GH_1scContinuityFunctions'

//Sample in use
let importRecurring = importRecurringOrder(recurringObject)
```

> recurringObject is a JSON object that is structured as such:

```json
{
    id: 123,
    brand: 456,
    mid: "midValue",
    apiKey: "apiKeyValue",
    status: "statusValue"
}
```

This function creates a new 1SC Continuity Record by calling 1SC directly.

 * 6 Governance Units
 
 * @param recurringRecord

#### Recurring Object Parameters

Parameter | Type | Description
--------- | ------- | -----------
id | number | This is the 1SC ID of the recurring record.
brand | number | This is the internal ID of the brand record that this record belongs to.
mid | string | The MID of the 1ShoppingCart cart this belongs to.
apiKey | string | The API Key generated from 1ShoppingCart for this cart listener.
status | string | (Optional) The status of the recurring record, required for update function.


## Locate Recurring Record
> Ensure that the string is formatted properly.

```javascript
//Include in defines
define(["../ghmfiles/GH_1scContinuityFunctions"], function (GH_1scContinuityFunctions)

//Sample in use
var recurringId = GH_1scContinuityFunctions.locateRecurringRecord(externalId)
```

```typescript
//Include in imports
import {locateRecurringRecord} from '../ghmfiles/GH_1scContinuityFunctions'

//Sample in use
let recurringId = locateRecurringRecord(externalId)
```

This function allows you to locate a recurring record in NetSuite by providing a search string. It will return false if no record is found, otherwise it will return the internal ID of the record.

 * 10 Governance Units
 
 * @param externalId
 
<aside class='notice'>The search string needs to be in the form of 1scRecurringId-mid (e.g. `123456-654321`)</aside>


