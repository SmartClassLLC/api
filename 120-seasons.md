# Seasons
Campuses, schools and seasons of the user.

Header | Required/Optional | Data Type | Explanation
------ | ----------------- | --------- | -----------
Authorization | Required | string | Authorization Token
schoolId | Required | string | School ID of the Authorization Token


## Get List

**GET: https://schoolid.smartclass.school/public/v1/seasons**

Path Parameter | Required/Optional | Data Type | Explanation
-------------- | ----------------- | --------- | -----------
userId | Required | string | User ID of the user that will be authenticated
userLanguage | Optional | string | Language of the user. If not sent, school default language will be considered.

### Sample Successful Response
```
{
    "currentSchool": {
        "schoolId": 0,
        "schoolName": "Headquarters"
    },
    "campuses": [
        {
            "Id": 1,
            "campusTitle": "Maslak",
            "schools": [
                {
                    "schoolId": 1,
                    "schoolName": "Primary"
                },
                {
                    "schoolId": 2,
                    "schoolName": "Secondary"
                }
            ]
        },
        {
            "Id": 2,
            "campusTitle": "Maryland",
            "schools": []
        },
        {
            "Id": 12,
            "campusTitle": "Washington",
            "schools": [
                {
                    "schoolId": 3,
                    "schoolName": "Kindergarten"
                },
                {
                    "schoolId": 19,
                    "schoolName": "A College"
                }
            ]
        }
    ],
    "schools": [],
    "seasons": [
        {
            "season": "2018-2019",
            "database": "dev_2018_2019"
        },
        {
            "season": "2017-2018",
            "database": "dev_2017_2018"
        },
        {
            "season": "2016-2017",
            "database": "dev_2016_2017"
        },
        {
            "season": "2015-2016",
            "database": "dev_2015_2016"
        }
    ]
}
```
