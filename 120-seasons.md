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
userId | Required | string | Authorization Token

### Sample Successful Response
```
{
    "currentSchool": {
        "schoolId": 0,
        "schoolName": "Genel Müdürlük"
    },
    "campuses": [
        {
            "Id": 1,
            "campusTitle": "İstanbul Maslak",
            "schools": [
                {
                    "schoolId": 1,
                    "schoolName": "İlkokul"
                },
                {
                    "schoolId": 2,
                    "schoolName": "Ortaokul"
                }
            ]
        },
        {
            "Id": 2,
            "campusTitle": "İstanbul Çamlıca",
            "schools": []
        },
        {
            "Id": 5,
            "campusTitle": "İstanbul Kadıköy",
            "schools": []
        },
        {
            "Id": 12,
            "campusTitle": "Washington",
            "schools": [
                {
                    "schoolId": 3,
                    "schoolName": "NCCAKY"
                },
                {
                    "schoolId": 19,
                    "schoolName": "YMCA Quebec"
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
