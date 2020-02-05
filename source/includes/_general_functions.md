# General Functions
## Overview
This section contains the general functions that have been developed for the Golden Hippo custom environment.
They may rely on custom fields that are prevalent throughout the environment, but those areas will be noted in the examples.

## Get Subsidiary by Brand
```javascript
//Include in defines
define(["../ghmfiles/gh_generalFunctions"], function (gh) {
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
