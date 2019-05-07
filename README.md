###SmartClass API Documentation

All requests should be sent to the school instance url which might be something like below.
https://schoolid.smartclass.school/public/v1/

All requests should include API version number like v1 in the url.
All requests should include Authorization Token and schoolId of the token in the Header part.
All responses are in JSON format unless otherwise mentioned.

For Development: https://dev.smartclass.tech 
For Demo: https://demo.smartclass.tech

General Usage
$apiUrl = “https://dev.smartclass.tech”;
$apiVersion = “v1”;
$apiName = “authentication”;

$apiFullUrl = $apiUrl  .  "/public/"  .  $apiVersion  .  "/"  . $apiName
