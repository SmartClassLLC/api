# Installments
List, create, update, and delete student installments.

Header | Required/Optional | Data Type | Explanation
------ | ----------------- | --------- | -----------
Authorization | Required | string | Authorization Token
schoolId | Required | string | School ID of the Authorization Token


## Get Installments

**GET: https://schoolid.smartclass.school/public/v1/installments**

Parameter | Required/Optional | Data Type | Explanation
------ | ----------------- | --------- | -----------
stdId | Required | string | Student ID


### Sample Successful Response
```
{
    "message": {
        "success": "Loaded!"
    },
    "installments": [
        {
            "installmentAmount": "2000.000",
            "installmentDateTime": "2019-04-16",
            "installmentTypeId": 6,
            "installmentType": "Bank Transfer"
        },
        {
            "installmentAmount": "2600.000",
            "installmentDateTime": "2019-04-16",
            "installmentTypeId": 0,
            "installmentType": null
        },
        {
            "installmentAmount": "2600.000",
            "installmentDateTime": "2019-05-16",
            "installmentTypeId": 0,
            "installmentType": null
        },
        {
            "installmentAmount": "2600.000",
            "installmentDateTime": "2019-06-16",
            "installmentTypeId": 0,
            "installmentType": null
        },
        {
            "installmentAmount": "2600.000",
            "installmentDateTime": "2019-07-16",
            "installmentTypeId": 0,
            "installmentType": null
        },
        {
            "installmentAmount": "2600.000",
            "installmentDateTime": "2019-08-16",
            "installmentTypeId": 0,
            "installmentType": null
        }
    ],
    "nofInstallments": 6
}
```
## Create Payments

**POST: https://schoolid.smartclass.school/public/v1/installments**

Body Parameter | Required/Optional | Data Type | Explanation
------ | ----------------- | --------- | -----------
stdId | Required | string | Student ID
schoolId | Required | string | School ID
installmentAmount | Required | string | Installment Amount
notes | Required | string | Installment Notes
isDownPayment | Required | string | is Down Payment
installmentDateTime | Required | string | Installment Date

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

## Update Installments

**PUT: https://schoolid.smartclass.school/public/v1/installments**

Path Parameter | Required/Optional | Data Type | Explanation
------ | ----------------- | --------- | -----------
stdId | Required | string | Student ID
installmentId | Required | string | Installment ID

Body Parameter | Required/Optional | Data Type | Explanation
------ | ----------------- | --------- | -----------
installmentAmount | Required | string | Installment Amount
notes | Required | string | Installment Notes
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

## Delete Installments

**DELETE: https://schoolid.smartclass.school/public/v1/installments**

Path Parameter | Required/Optional | Data Type | Explanation
------ | ----------------- | --------- | -----------
stdId | Required | string | Student ID
installmentId | Required | string | Installment ID

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
