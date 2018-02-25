
Daily Budget
======

`/budget`

This is current daily budget from user

### Methods

Method | URL | Description
--- | --- | ---
**[GET](/documentation/endpoint/budget#get-current-daily-budget)** | `/budget` | GET current daily budget
**[PUT](/documentation/endpoint/budget#update-budget)** | `/budget` | Update budget

### Object Attributes

Attribute | Type | Readonly | Nullable | Has Default
--- | --- | --- | --- | ---
`business_id` | integer | &nbsp; | &nbsp; | &nbsp;
`completed` | boolean | &nbsp; | &nbsp; | &bullet;
`created` | timestamp | &nbsp; | &nbsp; | &bullet;
`cul_profit` | numeric | &nbsp; | &nbsp; | &bullet;
`cul_trades` | numeric | &nbsp; | &nbsp; | &bullet;
`daily_budget` | numeric | &nbsp; | &nbsp; | &bullet;
`id` | integer | &nbsp; | &nbsp; | &bullet;
`trade_date` | timestamp | &nbsp; | &bullet; | &nbsp;

GET current daily budget
------
<code request-method="GET">**GET** /budget</code>

Get current daily budget

### Example
```http
GET http://localhost:6789/budget
Authorization: Basic a2Vubnk6a2VubnkxMjM0NSE=
Host: localhost:6789
Origin: http://localhost:6789
```

```http
HTTP/1.1 200 Ok
Access-Control-Allow-Credentials: true
Access-Control-Allow-Headers: Suppress-WWW-Authenticate, Content-Type, Authorization, Vary
Access-Control-Allow-Methods: GET, PUT, POST, DELETE, HEAD, OPTIONS
Access-Control-Allow-Origin: http://localhost:6789
Access-Control-Max-Age: 3600
Cache-Control: no-store, must-revalidate
Content-Type: application/json
Date: Sun, 25 Feb 2018 16:25:44 GMT
Expires: 0
Server: TwistedWeb/16.6.0
Transfer-Encoding: chunked
Vary: Origin

{
    "business_id": 7, 
    "completed": false, 
    "created": "2018-02-25T10:51:42.393931-05:00", 
    "cul_profit": 0.0, 
    "cul_trades": 2.0, 
    "daily_budget": 52460.0, 
    "id": 3, 
    "trade_date": "2018-02-25"
}
```


Update budget
------
<code request-method="PUT">**PUT** /budget</code>

Update budget

### Example
```http
PUT http://localhost:6789/budget
Authorization: Basic a2Vubnk6a2VubnkxMjM0NSE=
Content-Length: 220
Content-Type: application/json
Host: localhost:6789
Origin: http://localhost:6789

{
    "business_id": 7, 
    "completed": false, 
    "created": "2018-02-25T10:51:42.393931-05:00", 
    "cul_profit": 0, 
    "cul_trades": 0, 
    "daily_budget": 50000, 
    "id": 3, 
    "trade_date": "2018-02-25"
}
```

```http
HTTP/1.1 200 Ok
Access-Control-Allow-Credentials: true
Access-Control-Allow-Headers: Suppress-WWW-Authenticate, Content-Type, Authorization, Vary
Access-Control-Allow-Methods: GET, PUT, POST, DELETE, HEAD, OPTIONS
Access-Control-Allow-Origin: http://localhost:6789
Access-Control-Max-Age: 3600
Cache-Control: no-store, must-revalidate
Content-Type: application/json
Date: Sun, 25 Feb 2018 16:25:44 GMT
Expires: 0
Server: TwistedWeb/16.6.0
Transfer-Encoding: chunked
Vary: Origin

{
    "business_id": 7, 
    "completed": false, 
    "created": "2018-02-25T10:51:42.393931-05:00", 
    "cul_profit": 0.0, 
    "cul_trades": 0.0, 
    "daily_budget": 50000.0, 
    "id": 3, 
    "trade_date": "2018-02-25"
}
```

