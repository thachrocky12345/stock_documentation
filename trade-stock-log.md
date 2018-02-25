
Trade Stock Log
======

`/trade-stock-log`

This save log stock trade transactions that user made

### Methods

Method | URL | Description
--- | --- | ---
**[GET](/documentation/endpoint/trade-stock-log#get-log-of-all-transaction-that-user-did)** | `/trade-stock-log` | Get log of all transaction that user did

### Object Attributes

Attribute | Type | Readonly | Nullable | Has Default
--- | --- | --- | --- | ---
`bought` | numeric | &nbsp; | &bullet; | &nbsp;
`business_id` | integer | &nbsp; | &nbsp; | &nbsp;
`created` | timestamp | &nbsp; | &nbsp; | &bullet;
`id` | integer | &nbsp; | &nbsp; | &bullet;
`sold` | numeric | &nbsp; | &bullet; | &nbsp;
`symbol` | text | &nbsp; | &nbsp; | &nbsp;
`total_shares` | integer | &nbsp; | &nbsp; | &nbsp;
`type` | text | &nbsp; | &nbsp; | &nbsp;

Get log of all transaction that user did
------
<code request-method="GET">**GET** /trade-stock-log</code>

This endpoint can check all the log transactions that users made

### Query Parameters

Parameter | Type | Description
--- | --- | ---
`business-id` | int | business_id or user-id that made the trade
`symbol` | string | stock symbol, example AAPL
`trade-date` | string | date that trade, example 2018-02-18
`type` | string | trade can be long/short, type can only UP/DOWN



### Example
```http
GET http://localhost:6789/trade-stock-log
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
        "bought": 172.0, 
        "business_id": 7, 
        "created": "2018-02-23T23:34:15.744459-05:00", 
        "id": 1, 
        "sold": null, 
        "symbol": "AAPL", 
        "total_shares": 50, 
        "type": "DOWN"
    }, 
    {
        "bought": 172.0, 
        "business_id": 7, 
        "created": "2018-02-23T23:35:41.299184-05:00", 
        "id": 2, 
        "sold": 175.465, 
        "symbol": "AAPL", 
        "total_shares": 50, 
        "type": "DOWN"
    }, 
    {
        "bought": 12.0, 
        "business_id": 7, 
        "created": "2018-02-25T11:13:22.578120-05:00", 
        "id": 3, 
        "sold": null, 
        "symbol": "AMD", 
        "total_shares": 100, 
        "type": "UP"
    }, 
    {
        "bought": 12.0, 
        "business_id": 7, 
        "created": "2018-02-25T11:17:02.554565-05:00", 
        "id": 4, 
        "sold": null, 
        "symbol": "AMD", 
        "total_shares": 100, 
        "type": "UP"
    }, 
    {
        "bought": 12.0, 
        "business_id": 7, 
        "created": "2018-02-25T11:17:37.653441-05:00", 
        "id": 5, 
        "sold": null, 
        "symbol": "AMD", 
        "total_shares": 100, 
        "type": "UP"
    }, 
    {
        "bought": 11.333333333333334, 
        "business_id": 7, 
        "created": "2018-02-25T11:22:11.824327-05:00", 
        "id": 6, 
        "sold": 12.1, 
        "symbol": "AMD", 
        "total_shares": 300, 
        "type": "UP"
    }, 
    {
        "bought": 12.0, 
        "business_id": 7, 
        "created": "2018-02-25T11:25:43.274293-05:00", 
        "id": 7, 
        "sold": null, 
        "symbol": "AMD", 
        "total_shares": 100, 
        "type": "UP"
    }, 
    {
        "bought": 11.333333333333334, 
        "business_id": 7, 
        "created": "2018-02-25T11:25:44.005808-05:00", 
        "id": 8, 
        "sold": 12.1, 
        "symbol": "AMD", 
        "total_shares": 300, 
        "type": "UP"
    }
]
```

