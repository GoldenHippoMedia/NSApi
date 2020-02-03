# 1SC Continuity

<aside>

These functions are located in the GH_1scContinuityFunctions library.

</aside>

## Update Continuity Record

This function locates an existing recurring order, or creates one if it doesn't exist. It does not contact 1SC directly unless a new record is required.

```javascript
//Include in imports
import {updateRecurringOrder} from './GH_1scContinuityFunctions'

//Sample of in use
var recurringUpdate = updateRecurringOrder(recurringObject)
```


```typescript
//Include in imports
import {updateRecurringOrder} from './GH_1scContinuityFunctions'

//Sample of in use
let recurringUpdate = updateRecurringOrder(recurringObject)
```

> The above requires a recurringObject that is structured as such:

```json
{
    id: 123,
    brand: 456,
    mid: "midValue",
    apiKey: "apiKeyValue",
    status: "statusValue"
}
```
#### Recurring Object Parameters

Parameter | Type | Description
--------- | ------- | -----------
id | number | This is the 1SC ID of the recurring record.
brand | number | This is the internal ID of the brand record that this record belongs to.
mid | string | The MID of the 1ShoppingCart cart this belongs to.
apiKey | string | The API Key generated from 1ShoppingCart for this cart listener.
status | string | (Optional) The status of the recurring record, required for update function.


## Create Continuity Record

This function creates a new 1SC Continuity Record by calling 1SC directly.

```javascript
//Include in imports
import {importRecurringOrder} from './GH_1scContinuityFunctions'

//Sample of in use
var importRecurring = importRecurringOrder(recurringObject)
```


```typescript
//Include in imports
import {importRecurringOrder} from './GH_1scContinuityFunctions'

//Sample of in use
let importRecurring = importRecurringOrder(recurringObject)
```

> The above requires a recurringObject that is structured as such:

```json
{
    id: 123,
    brand: 456,
    mid: "midValue",
    apiKey: "apiKeyValue",
    status: "statusValue"
}
```
#### Recurring Object Parameters

Parameter | Type | Description
--------- | ------- | -----------
id | number | This is the 1SC ID of the recurring record.
brand | number | This is the internal ID of the brand record that this record belongs to.
mid | string | The MID of the 1ShoppingCart cart this belongs to.
apiKey | string | The API Key generated from 1ShoppingCart for this cart listener.
status | string | (Optional) The status of the recurring record, required for update function.

## Locate Recurring Record
This function allows you to locate a recurring record by providing a search string.

It will return false if no record is found, otherwise it will return the internal ID of the record.

```javascript
//Include in imports
import {locateRecurringRecord} from './GH_1scContinuityFunctions'

//Sample of use
var recurringId = locateRecurringRecord(string)
```

```typescript
//Include in imports
import {locateRecurringRecord} from './GH_1scContinuityFunctions'

//Sample of use
var recurringId = locateRecurringRecord(string)
```

> Ensure that the string is formatted properly.

The search string needs to be in the form of 1scRecurringId-mid (e.g. `123456-654321`)


