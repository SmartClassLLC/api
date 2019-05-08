## General
General information about the school like name, address, phone, logo, icon, etc.

**GET: https://schoolid.smartclass.school/public/v1/general**

Header | Required/Optional | Data Type | Explanation
------ | ----------------- | --------- | -----------
Authorization | Required | string | Authorization Token
schoolId | Required | string | School ID of the Authorization Token

## Sample Successful Response
```
{
    "sitename": "SmartClass [Development]",
    "slogan": "Herkes için teknoloji, herkes için eğitim",
    "address": "İstiklal Cad. İstanbul",
    "zipcode": "",
    "cityID": 41993,
    "stateID": 3499,
    "countryCode": "TR",
    "website": "",
    "email": "",
    "phone": "",
    "siteurl": "https://dev.smartclass.tech",
    "site_favicon": "https://schst.in/icon",
    "site_logo": "https://schst.in/smartclass",
    "timeZone": "Europe/Istanbul",
    "language": "turkish"
}
```
