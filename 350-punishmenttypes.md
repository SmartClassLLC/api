# Punishment Types
List punishment types.

Header | Required/Optional | Data Type | Explanation
------ | ----------------- | --------- | -----------
Authorization | Required | string | Authorization Token
schoolId | Required | string | School ID of the Authorization Token


## Get Punishment Types

**GET: https://schoolid.smartclass.school/public/v1/punishmenttypes**

### Sample Successful Response
```
{
    "message": {
        "success": "Loaded!"
    },
    "punishmentTypes": [
        {
            "ID": 1,
            "type": "Written Warning",
        }
    ]
}
```
