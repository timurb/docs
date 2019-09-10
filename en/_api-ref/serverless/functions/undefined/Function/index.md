---
editable: false
---

# Function

## JSON Representation {#representation}
```json 
{
  "id": "string",
  "folderId": "string",
  "createdAt": "string",
  "name": "string",
  "description": "string",
  "labels": "object",
  "logGroupId": "string",
  "httpInvokeUrl": "string",
  "status": "string"
}
```
 
Field | Description
--- | ---
id | **string**<br>
folderId | **string**<br>
createdAt | **string** (date-time)<br><p>String in <a href="https://www.ietf.org/rfc/rfc3339.txt">RFC3339</a> text format.</p> 
name | **string**<br>
description | **string**<br>
labels | **object**<br>
logGroupId | **string**<br>
httpInvokeUrl | **string**<br>
status | **string**<br>

## Methods {#methods}
Method | Description
--- | ---
[create](create.md) | 
[createFunctionVersion](createFunctionVersion.md) | 
[delete](delete.md) | 
[get](get.md) | 
[getFunctionVersion](getFunctionVersion.md) | 
[getFunctionVersionByTag](getFunctionVersionByTag.md) | 
[list](list.md) | 
[listAccessBindings](listAccessBindings.md) | 
[listFunctionTagHistory](listFunctionTagHistory.md) | 
[listFunctionVersions](listFunctionVersions.md) | 
[listOperations](listOperations.md) | 
[listRuntimes](listRuntimes.md) | 
[removeTag](removeTag.md) | 
[setAccessBindings](setAccessBindings.md) | 
[setTag](setTag.md) | 
[update](update.md) | 
[updateAccessBindings](updateAccessBindings.md) | 