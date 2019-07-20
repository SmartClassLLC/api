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
        "language": "english",
        "langTitle": "English",
        "flag": "https://schst.in/english"
    },
    {
        "language": "spanish",
        "langTitle": "Español",
        "flag": "https://schst.in/spanish"
    },
    {
        "language": "turkish",
        "langTitle": "Türkçe",
        "flag": "https://schst.in/turkish"
    },
    {
        "language": "arabic",
        "langTitle": "العربية",
        "flag": "https://schst.in/arabic"
    },
    {
        "language": "french",
        "langTitle": "Français",
        "flag": "https://schst.in/french"
    },
    {
        "language": "german",
        "langTitle": "Deutsch",
        "flag": "https://schst.in/german"
    },
    {
        "language": "chinese",
        "langTitle": "中文",
        "flag": "https://schst.in/chinese"
    },
    {
        "language": "russian",
        "langTitle": "Pусский",
        "flag": "https://schst.in/russian"
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
