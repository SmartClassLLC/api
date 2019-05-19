# Notifications
List, create, update, delete notifications

Header | Required/Optional | Data Type | Explanation
------ | ----------------- | --------- | -----------
Authorization | Required | string | Authorization Token
schoolId | Required | string | School ID of the Authorization Token


## List Notifications

**GET: https://schoolid.smartclass.school/public/v1/notifications**

Path Parameter | Required/Optional | Data Type | Explanation
-------------- | ----------------- | --------- | -----------
userId | Required | string | User ID of the user that will be authenticated
userLanguage | Optional | string | Language of the user. If not sent, school default language will be considered.

### Sample Successful Response
```
{
    "notifications": [
        {
            "id": 8482,
            "subject": "Şifre Değiştirme",
            "msgBody": "Sayın Şimşek, Kullanıcı şifreniz değiştirilmiştir.<br><br>Eğer siz değiştirmediyseniz lütfen sistem yöneticinize haber veriniz.",
            "fromUser": "support@smartclass.email",
            "sentTime": "19.04.2019 04:34",
            "msgRead": "0"
        },
        {
            "id": 6613,
            "subject": "Görev Atandı",
            "msgBody": "Görev Atandı [Toplantı Kararları [deneme toplantısı]]",
            "fromUser": "345232345",
            "sentTime": "13.10.2018 21:49",
            "msgRead": "0"
        }
    ],
    "nodataText": "Hepsi bu kadar!<br>Yeni bildirim yok."
}
```
