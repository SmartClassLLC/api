# Payment Types
List payment types.

Header | Required/Optional | Data Type | Explanation
------ | ----------------- | --------- | -----------
Authorization | Required | string | Authorization Token
schoolId | Required | string | School ID of the Authorization Token


## Get Payment Types

**GET: https://schoolid.smartclass.school/public/v1/paymenttypes**

### Sample Successful Response
```
{
    "message": {
        "success": "Loaded!"
    },
    "paymentTypes": [
        {
            "paymentID": 1,
            "paymentType": "Cash"
        },
        {
            "paymentID": 2,
            "paymentType": "Credit Card"
        }
    ]
}
```
