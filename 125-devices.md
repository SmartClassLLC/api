# Devices
List, create, update, delete user devices

Header | Required/Optional | Data Type | Explanation
------ | ----------------- | --------- | -----------
Authorization | Required | string | Authorization Token
schoolId | Required | string | School ID of the Authorization Token


## Create A Device

**POST: https://schoolid.smartclass.school/public/v1/devices**

Path Parameter | Required/Optional | Data Type | Explanation
-------------- | ----------------- | --------- | -----------
userId | Required | string | User ID
userLanguage | Optional | string | Language of the user. If not sent, school default language will be considered.

Post Parameter | Required/Optional | Data Type | Explanation
-------------- | ----------------- | --------- | -----------
deviceId | Required | string | Device ID of the device to be added

### Sample Successful Response
```
{
    "message": {
        "success": "Saved"
    },
}
```
