---
title: Extracts Social API
language_tabs:
  - shell: Shell
  - http: HTTP
  - javascript: JavaScript
  - javascript--nodejs: Node.JS
  - ruby: Ruby
  - python: Python
  - java: Java
  - go: Go
toc_footers: []
includes: []
search: false
highlight_theme: darkula
headingLevel: 2

---

<h1 id="extracts-social-api">Extracts Social API v1.0.0</h1>

> Scroll down for code samples, example requests and responses. Select a language for code samples from the tabs above or the mobile navigation menu.

The Extracts Social API.

Base URLs:

* <a href="https://cvqtzfgnk3.execute-api.us-east-1.amazonaws.com/Production">https://cvqtzfgnk3.execute-api.us-east-1.amazonaws.com/Production</a>

Email: <a href="mailto:support@extracts.io">API Support</a> Web: <a href="http://extracts.io/support">API Support</a> 

# Authentication

- HTTP Authentication, scheme: bearer 

<h1 id="extracts-social-api-default">Default</h1>

## get__status

> Code samples

```shell
# You can also use wget
curl -X GET https://cvqtzfgnk3.execute-api.us-east-1.amazonaws.com/Production/status \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
GET https://cvqtzfgnk3.execute-api.us-east-1.amazonaws.com/Production/status HTTP/1.1
Host: cvqtzfgnk3.execute-api.us-east-1.amazonaws.com
Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json',
  'Authorization':'Bearer {access-token}'

};

$.ajax({
  url: 'https://cvqtzfgnk3.execute-api.us-east-1.amazonaws.com/Production/status',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const fetch = require('node-fetch');

const headers = {
  'Accept':'application/json',
  'Authorization':'Bearer {access-token}'

};

fetch('https://cvqtzfgnk3.execute-api.us-east-1.amazonaws.com/Production/status',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json',
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.get 'https://cvqtzfgnk3.execute-api.us-east-1.amazonaws.com/Production/status',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.get('https://cvqtzfgnk3.execute-api.us-east-1.amazonaws.com/Production/status', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://cvqtzfgnk3.execute-api.us-east-1.amazonaws.com/Production/status");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
        "Authorization": []string{"Bearer {access-token}"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://cvqtzfgnk3.execute-api.us-east-1.amazonaws.com/Production/status", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /status`

Gets the status of the server. You can use this to test the API.

> Example responses

> 200 Response

```json
{
  "message": "string"
}
```

<h3 id="get__status-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|A status response|[Status](#schemastatus)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
BearerAuth
</aside>

## post__offer-redemptions

> Code samples

```shell
# You can also use wget
curl -X POST https://cvqtzfgnk3.execute-api.us-east-1.amazonaws.com/Production/offer-redemptions \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {access-token}'

```

```http
POST https://cvqtzfgnk3.execute-api.us-east-1.amazonaws.com/Production/offer-redemptions HTTP/1.1
Host: cvqtzfgnk3.execute-api.us-east-1.amazonaws.com
Content-Type: application/json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json',
  'Accept':'application/json',
  'Authorization':'Bearer {access-token}'

};

$.ajax({
  url: 'https://cvqtzfgnk3.execute-api.us-east-1.amazonaws.com/Production/offer-redemptions',
  method: 'post',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const fetch = require('node-fetch');
const inputBody = '{
  "teamId": "39859716-6f25-11e9-ae22-28cfe91fa8f1",
  "offerCode": "SPRING_2019_50_PERCENT_OFF",
  "redeemedAt": "2019-05-05T11:11:57Z",
  "orderId": "O144232334",
  "currency": "USD",
  "value": "13.33",
  "contentIds": [
    "SKU22242"
  ]
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json',
  'Authorization':'Bearer {access-token}'

};

fetch('https://cvqtzfgnk3.execute-api.us-east-1.amazonaws.com/Production/offer-redemptions',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'Authorization' => 'Bearer {access-token}'
}

result = RestClient.post 'https://cvqtzfgnk3.execute-api.us-east-1.amazonaws.com/Production/offer-redemptions',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json',
  'Authorization': 'Bearer {access-token}'
}

r = requests.post('https://cvqtzfgnk3.execute-api.us-east-1.amazonaws.com/Production/offer-redemptions', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("https://cvqtzfgnk3.execute-api.us-east-1.amazonaws.com/Production/offer-redemptions");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
        "Authorization": []string{"Bearer {access-token}"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "https://cvqtzfgnk3.execute-api.us-east-1.amazonaws.com/Production/offer-redemptions", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /offer-redemptions`

Creates an Offer Redemption. "teamId" and "offerCode" are the only required fields.

> Body parameter

```json
{
  "teamId": "39859716-6f25-11e9-ae22-28cfe91fa8f1",
  "offerCode": "SPRING_2019_50_PERCENT_OFF",
  "redeemedAt": "2019-05-05T11:11:57Z",
  "orderId": "O144232334",
  "currency": "USD",
  "value": "13.33",
  "contentIds": [
    "SKU22242"
  ]
}
```

<h3 id="post__offer-redemptions-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[CreateOfferRedemption](#schemacreateofferredemption)|true|none|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": "string"
  }
}
```

<h3 id="post__offer-redemptions-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Create an Offer Campaign Redemption|Inline|

<h3 id="post__offer-redemptions-responseschema">Response Schema</h3>

Status Code **200**

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|» data|[OfferRedemption](#schemaofferredemption)|false|none|none|
|»» id|string|false|none|none|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
BearerAuth
</aside>

# Schemas

<h2 id="tocSstatus">Status</h2>

<a id="schemastatus"></a>

```json
{
  "message": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|message|string|false|none|none|

<h2 id="tocSofferredemption">OfferRedemption</h2>

<a id="schemaofferredemption"></a>

```json
{
  "id": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|string|false|none|none|

<h2 id="tocScreateofferredemption">CreateOfferRedemption</h2>

<a id="schemacreateofferredemption"></a>

```json
{
  "teamId": "39859716-6f25-11e9-ae22-28cfe91fa8f1",
  "offerCode": "SPRING_2019_50_PERCENT_OFF",
  "redeemedAt": "2019-05-05T11:11:57Z",
  "orderId": "O144232334",
  "currency": "USD",
  "value": "13.33",
  "contentIds": [
    "SKU22242"
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|teamId|string|true|none|none|
|offerCode|string|true|none|none|
|redeemedAt|string(date-time)|false|none|none|
|orderId|string|false|none|none|
|currency|string|false|none|none|
|value|string|false|none|The value of the total order|
|contentIds|[string]|false|none|none|

