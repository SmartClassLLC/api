# Payments
List, create, update, and delete student payments.

Header | Required/Optional | Data Type | Explanation
------ | ----------------- | --------- | -----------
Authorization | Required | string | Authorization Token
schoolId | Required | string | School ID of the Authorization Token


## Get Payments

**GET: https://schoolid.smartclass.school/public/v1/payments**

Parameter | Required/Optional | Data Type | Explanation
------ | ----------------- | --------- | -----------
stdId | Required | string | Student ID


### Sample Successful Response
```
[
    {
    "message": {
        "success": "Loaded!"
    },
    "payments": [
        {
            "paymentAmount": "4500.000",
            "paymentDateTime": "2019-05-29 01:10:00",
            "paymentTypeId": 0,
            "paymentType": null,
            "paymentReceiver": "simsek"
        },
        {
            "paymentAmount": "4500.000",
            "paymentDateTime": "2019-05-30 17:40:00",
            "paymentTypeId": 0,
            "paymentType": null,
            "paymentReceiver": "simsek"
        },
        {
            "paymentAmount": "4500.000",
            "paymentDateTime": "2019-06-10 05:55:32",
            "paymentTypeId": 0,
            "paymentType": null,
            "paymentReceiver": "simsek"
        },
        {
            "paymentAmount": "4500.000",
            "paymentDateTime": "2019-05-30 17:40:00",
            "paymentTypeId": 0,
            "paymentType": null,
            "paymentReceiver": "simsek"
        }
    ],
    "nofPayments": 4
}
]
```
## Create Payments

**POST: https://schoolid.smartclass.school/public/v1/payments**

Body Parameter | Required/Optional | Data Type | Explanation
------ | ----------------- | --------- | -----------
stdId | Required | string | Student ID
schoolId | Required | string | School ID
paymentAmount | Required | string | Payment Amount
notes | Required | string | Payment Notes
isDownPayment | Required | string | is Down Payment

### Sample Successful Response
```
[
    {
    "message": {
        "success": "Saved."
        }
    }
]
```

## Update Payments

**PUT: https://schoolid.smartclass.school/public/v1/payments**

Path Parameter | Required/Optional | Data Type | Explanation
------ | ----------------- | --------- | -----------
stdId | Required | string | Student ID
paymentId | Required | string | Payment ID

Body Parameter | Required/Optional | Data Type | Explanation
------ | ----------------- | --------- | -----------
paymentAmount | Required | string | Payment Amount
notes | Required | string | Payment Notes
isDownPayment | Required | string | is Down Payment

### Sample Successful Response
```
[
    {
    "message": {
        "success": "Saved."
        }
    }
]
```

## Delete Payments

**DELETE: https://schoolid.smartclass.school/public/v1/payments**

Path Parameter | Required/Optional | Data Type | Explanation
------ | ----------------- | --------- | -----------
stdId | Required | string | Student ID
paymentId | Required | string | Payment ID

### Sample Successful Response
```
[
    {
    "message": {
        "success": "Deleted"
        }
    }
]
```
