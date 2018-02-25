
Trade stock endpoint
======

`/trade-stock`

This endpoint is use to place a trade POST or close the trade UP

### Methods

Method | URL | Description
--- | --- | ---
**[GET](/documentation/endpoint/trade-stock#get-current-uncompleted,-completed-trade-positions-as-well-current-daily-budget)** | `/trade-stock` | GET current uncompleted, completed trade positions as well current daily budget
**[POST](/documentation/endpoint/trade-stock#post-new-trade-position)** | `/trade-stock` | POST new trade position
**[GET](/documentation/endpoint/trade-stock#get-current-trade-position-by-its-id)** | `/trade-stock/<id>` | GET current trade position by its id
**[PUT](/documentation/endpoint/trade-stock#put-to-close-a-trade-position)** | `/trade-stock` | PUT to close a trade position
**[GET](/documentation/endpoint/trade-stock#get-all-traded-positions-that-user-did)** | `/trade-stock/history` | Get all traded positions that user did

### Object Attributes

Attribute | Type | Readonly | Nullable | Has Default
--- | --- | --- | --- | ---
`bought` | numeric | &nbsp; | &bullet; | &nbsp;
`bought_more` | integer | &nbsp; | &bullet; | &nbsp;
`business_id` | integer | &nbsp; | &nbsp; | &nbsp;
`completed` | timestamp | &nbsp; | &bullet; | &nbsp;
`created` | timestamp | &nbsp; | &nbsp; | &bullet;
`id` | integer | &nbsp; | &nbsp; | &bullet;
`profit` | numeric | &nbsp; | &bullet; | &nbsp;
`sold` | numeric | &nbsp; | &bullet; | &nbsp;
`symbol` | text | &nbsp; | &nbsp; | &nbsp;
`total_shares` | integer | &nbsp; | &nbsp; | &nbsp;
`trade_date` | timestamp | &nbsp; | &nbsp; | &bullet;
`type` | text | &nbsp; | &nbsp; | &nbsp;

GET current uncompleted, completed trade positions as well current daily budget
------
<code request-method="GET">**GET** /trade-stock</code>

GET current uncompleted, completed, daily budget

### Example
```http
GET http://localhost:6789/trade-stock
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
Date: Sun, 25 Feb 2018 16:25:42 GMT
Expires: 0
Server: TwistedWeb/16.6.0
Transfer-Encoding: chunked
Vary: Origin

{
    "completed_positions": [], 
    "current_budget": {
        "business_id": 7, 
        "completed": false, 
        "created": "2018-02-25T10:51:42.393931-05:00", 
        "cul_profit": 0.0, 
        "cul_trades": 1.0, 
        "daily_budget": 50030.0, 
        "id": 3, 
        "trade_date": "2018-02-25"
    }, 
    "holding_positions": []
}
```


POST new trade position
------
<code request-method="POST">**POST** /trade-stock</code>

POST new trade position, requires as minimum as total_shares, type, symbol, bought price

### Example
```http
POST http://localhost:6789/trade-stock
Authorization: Basic a2Vubnk6a2VubnkxMjM0NSE=
Content-Length: 87
Content-Type: application/json
Host: localhost:6789
Origin: http://localhost:6789

{
    "bought": 12, 
    "symbol": "AMD", 
    "total_shares": 100, 
    "type": "UP"
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
Date: Sun, 25 Feb 2018 16:25:43 GMT
Expires: 0
Server: TwistedWeb/16.6.0
Transfer-Encoding: chunked
Vary: Origin

{
    "bought": 12.0, 
    "bought_more": 0, 
    "business_id": 7, 
    "completed": null, 
    "created": "2018-02-25T11:25:43.563889-05:00", 
    "id": 5, 
    "profit": null, 
    "sold": null, 
    "symbol": "AMD", 
    "total_shares": 100, 
    "trade_date": "2018-02-25", 
    "type": "UP"
}
```


GET current trade position by its id
------
<code request-method="GET">**GET** /trade-stock/&lt;id&gt;</code>

GET current trade position by its id

### Example
```http
GET http://localhost:6789/trade-stock/1
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
Date: Sun, 25 Feb 2018 16:25:43 GMT
Expires: 0
Server: TwistedWeb/16.6.0
Transfer-Encoding: chunked
Vary: Origin

{
    "bought": 11.333333333333334, 
    "bought_more": 2, 
    "business_id": 7, 
    "completed": "2018-02-25T11:22:11.760653-05:00", 
    "created": "2018-02-23T22:11:02.621622-05:00", 
    "id": 1, 
    "profit": 230.0, 
    "sold": 12.1, 
    "symbol": "AMD", 
    "total_shares": 300, 
    "trade_date": "2018-02-24", 
    "type": "UP"
}
```


PUT to close a trade position
------
<code request-method="PUT">**PUT** /trade-stock</code>

Close the position requires minimum trade's id and total_shares, sold price

### Example
```http
PUT http://localhost:6789/trade-stock
Authorization: Basic a2Vubnk6a2VubnkxMjM0NSE=
Content-Length: 213
Content-Type: application/json
Host: localhost:6789
Origin: http://localhost:6789

{
    "bought": 11.333333333333334, 
    "bought_more": 2, 
    "id": 1, 
    "profit": null, 
    "sold": 12.1, 
    "symbol": "AMD", 
    "total_shares": 300, 
    "trade_date": "2018-02-24", 
    "type": "UP"
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
Date: Sun, 25 Feb 2018 16:25:43 GMT
Expires: 0
Server: TwistedWeb/16.6.0
Transfer-Encoding: chunked
Vary: Origin

{
    "bought": 11.333333333333334, 
    "bought_more": 2, 
    "business_id": 7, 
    "completed": "2018-02-25T11:25:43.943170-05:00", 
    "created": null, 
    "id": 1, 
    "profit": 230.0, 
    "sold": 12.1, 
    "symbol": "AMD", 
    "total_shares": 300, 
    "trade_date": "2018-02-23T19:00:00-05:00", 
    "type": "UP"
}
```


Get all traded positions that user did
------
<code request-method="GET">**GET** /trade-stock/history</code>

This endpoint can check all trade position that users made

### Query Parameters

Parameter | Type | Description
--- | --- | ---
`business-id` | int | business_id or user-id that made the trade
`completed` | string | date that trade completed, example 2018-02-18
`symbol` | string | stock symbol, example AAPL
`trade-date` | string | date that trade, example 2018-02-18
`type` | string | trade can be long/short, type can only UP/DOWN



### Example
```http
GET http://localhost:6789/trade-stock/history
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

[
    {
        "bought": 72.0, 
        "bought_more": 2, 
        "business_id": 7, 
        "completed": "2018-02-23T23:16:03.789824-05:00", 
        "created": "2018-02-23T22:39:31.931544-05:00", 
        "id": 2, 
        "profit": 2247.0, 
        "sold": 64.50999999999999, 
        "symbol": "CERN", 
        "total_shares": 300, 
        "trade_date": "2018-02-24", 
        "type": "DOWN"
    }, 
    {
        "bought": 72.0, 
        "bought_more": 0, 
        "business_id": 7, 
        "completed": "2018-02-23T23:19:58.844795-05:00", 
        "created": "2018-02-23T23:19:25.628849-05:00", 
        "id": 3, 
        "profit": 750.0, 
        "sold": 64.5, 
        "symbol": "CERN", 
        "total_shares": 100, 
        "trade_date": "2018-02-24", 
        "type": "DOWN"
    }, 
    {
        "bought": 172.0, 
        "bought_more": 0, 
        "business_id": 7, 
        "completed": "2018-02-23T23:35:41.230768-05:00", 
        "created": "2018-02-23T23:34:16.085244-05:00", 
        "id": 4, 
        "profit": -173.25, 
        "sold": 175.465, 
        "symbol": "AAPL", 
        "total_shares": 50, 
        "trade_date": "2018-02-24", 
        "type": "DOWN"
    }, 
    {
        "bought": 12.0, 
        "bought_more": 0, 
        "business_id": 7, 
        "completed": null, 
        "created": "2018-02-25T11:25:43.563889-05:00", 
        "id": 5, 
        "profit": null, 
        "sold": null, 
        "symbol": "AMD", 
        "total_shares": 100, 
        "trade_date": "2018-02-25", 
        "type": "UP"
    }, 
    {
        "bought": 11.333333333333334, 
        "bought_more": 2, 
        "business_id": 7, 
        "completed": "2018-02-25T11:25:43.943170-05:00", 
        "created": "2018-02-23T22:11:02.621622-05:00", 
        "id": 1, 
        "profit": 230.0, 
        "sold": 12.1, 
        "symbol": "AMD", 
        "total_shares": 300, 
        "trade_date": "2018-02-24", 
        "type": "UP"
    }
]
```

