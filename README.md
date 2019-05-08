# SmartClass API Documentation

All requests should be sent to the school instance url which might be something like below.
https://schoolid.smartclass.school/public/v1/

All requests should include API version number like v1 in the url.
All requests should include Authorization Token and schoolId of the token in the Header part.
All responses are in JSON format unless otherwise mentioned.

For Development: https://dev.smartclass.tech 
For Demo: https://demo.smartclass.tech

### General Usage
```
$apiUrl = “https://dev.smartclass.tech”;
$apiVersion = “v1”;
$apiName = “authentication”;

$apiFullUrl = $apiUrl  .  "/public/"  .  $apiVersion  .  "/"  . $apiName
```

### Sample Codes
#### cURL
```
curl -X GET \
    'https://development.smartclass.tech/public/v1/authentication?userId=xxx&userPassword=xxx' \
    -H 'Authorization: Bearer c3pgvLKqqrGQTWOASriiIU8czlBAzrujw5hcuiogJC4' \
    -H 'Cache-Control: no-cache' \
    -H 'schoolId: 11'
```


#### jQuery
```
var settings = {
	"async": true,
	"crossDomain": true,
	"url": "https://dev.smartclass.tech/public/v1/authentication?userId=xxx&userPassword=xxx",
	"method": "GET",
	"headers": {
	"schoolId": "11",
	"Authorization": "Bearer c3pgvLKqqrGQTWOASriiIU8czlBAzrujw5hcuiogJC4",
	"Cache-Control": "no-cache",
}

$.ajax(settings).done(function (response) {
	console.log(response);
});
```

#### PHP
```
<?php

$curl = curl_init();

curl_setopt_array($curl, array(
		CURLOPT_URL => "https://development.smartclass.tech/public/v1/authentication?userId=xxx&userPassword=xxx",
		CURLOPT_RETURNTRANSFER => true,
		CURLOPT_ENCODING => "",
		CURLOPT_MAXREDIRS => 10,
		CURLOPT_TIMEOUT => 30,
		CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
		CURLOPT_CUSTOMREQUEST => "GET",
		CURLOPT_HTTPHEADER => array(
		"Authorization: Bearer c3pgvLKqqrGQTWOASriiIU8czlBAzrujw5hcuiogJC4",
		"Cache-Control: no-cache",
		"schoolId: 11"
	),
));

$response = curl_exec($curl);
$err = curl_error($curl);

curl_close($curl);

if ($err) {
	echo "cURL Error #:" . $err;
} else {
	echo $response;
}
```

#### Ruby
```
require 'uri'
require 'net/http'

url = URI("https://development.smartclass.tech/public/v1/authentication?userId=xxx&userPassword=xxx")

http = Net::HTTP.new(url.host, url.port)

request = Net::HTTP::Get.new(url)
request["schoolId"] = '11'
request["Authorization"] = 'Bearer c3pgvLKqqrGQTWOASriiIU8czlBAzrujw5hcuiogJC4'
request["Cache-Control"] = 'no-cache'

response = http.request(request)
puts response.read_body

#### Python Requests
import requests
url = "https://development.smartclass.tech/public/v1/authentication"

querystring = {"userId":"xxx","userPassword":"xxx"}
headers = {
'schoolId': "11",
'Authorization': "Bearer c3pgvLKqqrGQTWOASriiIU8czlBAzrujw5hcuiogJC4",
'Cache-Control': "no-cache",
}

response = requests.request("GET", url, headers=headers, params=querystring)
print(response.text)
```

#### Node.js
```
var http = require("https");
var options = {
	"method": "GET",
	"hostname": [
		"demo",
		"dmartclass",
		"tech"
	],
	"path": [
		"public",
		"v1",
		"authentication"
	],
	"headers": {
		"schoolId": "11",
		"Authorization": "Bearer c3pgvLKqqrGQTWOASriiIU8czlBAzrujw5hcuiogJC4",
		"Cache-Control": "no-cache",
	}
};
var req = http.request(options, function (res) {
var chunks = [];

res.on("data", function (chunk) {
	chunks.push(chunk);
});

res.on("end", function () {
	var body = Buffer.concat(chunks);
	console.log(body.toString());
	});
});

req.end();
```

#### Go
```
package main
import (
	"fmt"
	"net/http"
	"io/ioutil"
)
func main() {
	url := "https://development.smartclass.tech/public/v1/authentication?userId=xxx&userPassword=xxx"
	req, _ := http.NewRequest("GET", url, nil)
	req.Header.Add("schoolId", "11")
	req.Header.Add("Authorization", "Bearer c3pgvLKqqrGQTWOASriiIU8czlBAzrujw5hcuiogJC4")
	req.Header.Add("Cache-Control", "no-cache")
	res, _ := http.DefaultClient.Do(req)
	defer res.Body.Close()
	body, _ := ioutil.ReadAll(res.Body)
	fmt.Println(res)
	fmt.Println(string(body))
}
```

#### C#
```
var client = new RestClient("https://development.smartclass.tech/public/v1/authentication?userId=xxx&userPassword=xxx");
var request = new RestRequest(Method.GET);
request.AddHeader("Cache-Control", "no-cache");
request.AddHeader("Authorization", "Bearer c3pgvLKqqrGQTWOASriiIU8czlBAzrujw5hcuiogJC4");
request.AddHeader("schoolId", "11");
IRestResponse response = client.Execute(request);
```

#### Java
```
HttpResponse<String> response = Unirest.get("
https://dev.smartclass.tech/public/v1/authentication
")
.header("schoolId", "11")
.header("Authorization", "Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpZCI6NDQ2ODg2ODg2fQ.UEw0PxG4bl2BOV3FOkBRe6EoLb5aX6DLNOYDuubfS1L")
.asString();
```

- or -

```
OkHttpClient client = new OkHttpClient();

Request request = new Request.Builder()
.url("
https://dev.smartclass.tech/public/v1/authentication?userId=xxx&userPassword=xxx
")
.get()
.addHeader("schoolId", "11")
.addHeader("Authorization", "Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpZCI6NDQ2ODg2ODg2fQ.UEw0PxG4bl2BOV3FOkBRe6EoLb5aX6DLNOYDuubfS1L")

.build();

Response response = client.newCall(request).execute();
```
