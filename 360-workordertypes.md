# Work Order Types
List work order types.

Header | Required/Optional | Data Type | Explanation
------ | ----------------- | --------- | -----------
Authorization | Required | string | Authorization Token
schoolId | Required | string | School ID of the Authorization Token


## Get Work Order Types

**GET: https://schoolid.smartclass.school/public/v1/workordertypes**

### Sample Successful Response
```
{
    "message": {
        "success": "Loaded!"
    },
    "workOrderTypes": [
        {
            "ID": 1,
            "type": "Transportation",
            "parameter": "transportation"
        }
    ]
}
```
