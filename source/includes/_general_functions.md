# General Functions
## Overview

<aside class="success">
These functions are located in the gh_generalFunctions library.
</aside>

This section contains the general functions that have been developed for the Golden Hippo custom environment.
They may rely on custom fields that are prevalent throughout the environment, but those areas will be noted in the examples.

## Get Subsidiary by Brand
 > This function requires the custom record 'customrecord_ghm_brand_subs_list'

```javascript
//Include in defines
define(["../ghmfiles/gh_generalFunctions"], function (gh) {

//Sample in use
    var brandId = 1;
    var returnedSubId = gh.lookupSubByBrand(brandId)
};
```
```typescript
//Include in imports
import {lookupSubByBrand} from ("../ghmfiles/gh_generalFunctions");

//Sample in use
let brandId = 1
let returnedSubId = lookupSubByBrand(brandId as number);
```

Lookup subsidiary internal ID by providing the brand ID as an integer (number)
 
 * 1 Governance Unit
 
 * @param brandId
 
 This will return the internal ID as a number.
