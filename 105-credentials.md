# Credentials
Get, update of user credentials

Header | Required/Optional | Data Type | Explanation
------ | ----------------- | --------- | -----------
Authorization | Required | string | Authorization Token
schoolId | Required | string | School ID of the Authorization Token


## Update School

**PUT: https://schoolid.smartclass.school/public/v1/credentials/school**

Path Parameter | Required/Optional | Data Type | Explanation
-------------- | ----------------- | --------- | -----------
userId | Required | string | User ID of the current user
campusId | Required* | string | Campus ID to change to - required if schoolId is not sent
schoolId | Required* | string | School ID to change to - required if campusId is not sent
seasonId | Required | string | Current Season ID
userLanguage | Optional | string | Language of the user. If not sent, school default language will be considered.

### Sample Request URl
https://schoolid.smartclass.school/public/v1/credentials/school?userId=demo&schoolId=1&seasonId=2018-2019&userLanguage=english

### Sample Successful Response
```
{
    "message": {
        "success": "School has been changed!"
    },
    "admin": "ITpzaW1zOiEhOnNpbXM6A"
}
```

## Update Season

**PUT: https://schoolid.smartclass.school/public/v1/credentials/season**

Path Parameter | Required/Optional | Data Type | Explanation
-------------- | ----------------- | --------- | -----------
userId | Required | string | User ID of the current user
campusId | Required* | string | Current Campus ID - required if schoolId is not sent
schoolId | Required* | string | Current School ID - required if campusId is not sent
seasonId | Required | string | Season ID to change to
userLanguage | Optional | string | Language of the user. If not sent, school default language will be considered.

### Sample Request URl
https://schoolid.smartclass.school/public/v1/credentials/season?userId=demo&schoolId=1&seasonId=2018-2019&userLanguage=english

### Sample Successful Response
```
{
    "message": {
        "success": "Season has been changed!"
    },
    "admin": "ITpzaW1zOiEhOnNpbXM6A"
}
```

## Update Student

**PUT: https://schoolid.smartclass.school/public/v1/credentials/season**

Path Parameter | Required/Optional | Data Type | Explanation
-------------- | ----------------- | --------- | -----------
userId | Required | string | User ID of the current user
campusId | Required* | string | Current Campus ID - required if schoolId is not sent
schoolId | Required* | string | Current School ID - required if campusId is not sent
seasonId | Required | string | Current Season ID
stdId | Required | string | Student ID to change to
userLanguage | Optional | string | Language of the user. If not sent, school default language will be considered.

### Sample Request URl
https://schoolid.smartclass.school/public/v1/credentials/student?userId=demo&stdId=342&schoolId=1&seasonId=2018-2019&userLanguage=english

### Sample Successful Response
```
{
    "message": {
        "success": "Student has been changed!"
    },
    "ogrID": "342"
}
```
