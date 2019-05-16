# Seasons
Get, update of user credentials

Header | Required/Optional | Data Type | Explanation
------ | ----------------- | --------- | -----------
Authorization | Required | string | Authorization Token
schoolId | Required | string | School ID of the Authorization Token


## Update School

**GET: https://schoolid.smartclass.school/public/v1/credentials/school**

Path Parameter | Required/Optional | Data Type | Explanation
-------------- | ----------------- | --------- | -----------
userId | Required | string | User ID of the current user
campusId | Required if schoolId is not sent | string | campus ID to change to
schoolId | Required if campusId is not sent | string | school ID to change to
seasonId | Required | string | Current season ID
userLanguage | Optional | string | Language of the user. If not sent, school default language will be considered.

### Sample Successful Response
```
{
    "message": {
        "success": "School has been changed!"
    },
    "admin": "ITpzaW1zOiEhOnNpbXM6A"
}
```
