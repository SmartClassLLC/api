# Cause Of Absences
List cause of absences.

Header | Required/Optional | Data Type | Explanation
------ | ----------------- | --------- | -----------
Authorization | Required | string | Authorization Token
schoolId | Required | string | School ID of the Authorization Token


## Get Cause of Absences

**GET: https://schoolid.smartclass.school/public/v1/causeofabsences**

### Sample Successful Response
```
{
    "message": {
        "success": "Loaded!"
    },
    "subjects": [
        {
            "causeID": 1,
            "causeSymbol": "L",
            "causeName": "On Leave",
            "isLate": "0",
            "forTeacher": "1",
            "causeColour": null
        }
    ]
}
```
