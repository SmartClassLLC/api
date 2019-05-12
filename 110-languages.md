# Languages
Language lists and language replacements.

Header | Required/Optional | Data Type | Explanation
------ | ----------------- | --------- | -----------
Authorization | Required | string | Authorization Token
schoolId | Required | string | School ID of the Authorization Token


## Get Languages List

**GET: https://schoolid.smartclass.school/public/v1/languages**

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


## Get Language Replacements for a Language

**GET: https://schoolid.smartclass.school/public/v1/languages/:id**

Path Parameter | Required/Optional | Data Type | Explanation
-------------- | ----------------- | --------- | -----------
id | Required | string | Id should be a key from the array that is gotten from languages api. Ie: english, spanish


### Sample Successful Response
GET: https://schoolid.smartclass.school/public/v1/languages/english
```
{
    "english": {
        "LangTitle": "English",
        "SetYourSchool": "Set Your School",
        "Language": "Language",
        "Select Language": "Select Language",
        "School": "School",
        "SearchSchool": "Search for your school by typing.",
        "SaveSchool": "Save My School",
        "SmartClass": "2004 © SmartClass: School Operating System",
        "PickSchool": "Please pick your school!",
        "Loading": "Loading...",
        "ChangeSchool": "Change the School"
    }
}
```
