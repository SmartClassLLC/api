# User Types
List user types.

Header | Required/Optional | Data Type | Explanation
------ | ----------------- | --------- | -----------
Authorization | Required | string | Authorization Token
schoolId | Required | string | School ID of the Authorization Token


## Get User Types

**GET: https://schoolid.smartclass.school/public/v1/usertypes**

### Sample Successful Response
```
{
    "message": {
        "success": "Loaded!"
    },
    "userTypes": [
        {
            "userTypeID": 1,
            "userType": "_SYSTEM_ADMIN"
        },
        {
            "userTypeID": 2,
            "userType": "_GENERAL_MANAGER"
        }
    ]
}
```
