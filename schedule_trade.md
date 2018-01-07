
Schedule Trading
======

`/schedule-trade`

This is where you convert your prediction to trade

### Methods

Method | URL | Description
--- | --- | ---
**[GET](/documentation/endpoint/schedule_trade#get-all-of-your-current-schedule)** | `schedule-trade` | GET ALL OF YOUR CURRENT SCHEDULE
**[PUT](/documentation/endpoint/schedule_trade#update-your-schedule)** | `schedule_trade_update` | UPDATE YOUR SCHEDULE
**[POST](/documentation/endpoint/schedule_trade#insert-new-schedule)** | `schedule-trade` | INSERT NEW Schedule

### Object Attributes

Attribute | Type | Readonly | Nullable | Has Default
--- | --- | --- | --- | ---
`budget` | numeric | &nbsp; | &nbsp; | &nbsp;
`business_id` | integer | &nbsp; | &nbsp; | &nbsp;
`buy_angle` | numeric | &nbsp; | &bullet; | &nbsp;
`buy_angle_hold` | numeric | &nbsp; | &bullet; | &nbsp;
`buy_angle_xa` | numeric | &nbsp; | &bullet; | &nbsp;
`buy_executed_id` | integer | &nbsp; | &bullet; | &nbsp;
`buy_price` | numeric | &nbsp; | &nbsp; | &nbsp;
`created` | timestamp | &nbsp; | &nbsp; | &bullet;
`id` | integer | &nbsp; | &nbsp; | &bullet;
`sell_angle` | numeric | &nbsp; | &bullet; | &nbsp;
`sell_angle_hold` | numeric | &nbsp; | &bullet; | &nbsp;
`sell_executed_id` | integer | &nbsp; | &bullet; | &nbsp;
`sell_price` | numeric | &nbsp; | &nbsp; | &nbsp;
`symbol` | text | &nbsp; | &nbsp; | &nbsp;
`type` | text | &nbsp; | &nbsp; | &bullet;

GET ALL OF YOUR CURRENT SCHEDULE
------
<code request-method="GET">**GET** schedule-trade</code>

Get all schedule

### Example
```http
GET http://localhost:6789/schedule-trade
Authorization: Basic YW5kcmVpOmFuZHJlaTEyMzQ1IQ==
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
Date: Sun, 07 Jan 2018 15:06:34 GMT
Expires: 0
Server: TwistedWeb/17.1.0
Transfer-Encoding: chunked
Vary: Origin

[
    {
        "budget": 1000.0, 
        "business_id": 5, 
        "buy_angle": 15.0, 
        "buy_angle_hold": -50.0, 
        "buy_angle_xa": -50.0, 
        "buy_executed_id": null, 
        "buy_price": 13.0, 
        "created": "2018-01-07T15:03:29.272396", 
        "id": 3, 
        "sell_angle": 15.0, 
        "sell_angle_hold": 50.0, 
        "sell_executed_id": null, 
        "sell_price": 13.5, 
        "symbol": "AMD", 
        "type": "calls"
    }
]
```


UPDATE YOUR SCHEDULE
------
<code request-method="PUT">**PUT** schedule_trade_update</code>

This where you can update schedule due to thing change

### Example
```http
PUT http://localhost:6789/schedule-trade
Authorization: Basic YW5kcmVpOmFuZHJlaTEyMzQ1IQ==
Content-Length: 384
Content-Type: application/json
Host: localhost:6789
Origin: http://localhost:6789

{
    "budget": 1000, 
    "business_id": 1, 
    "buy_angle": 15, 
    "buy_angle_hold": -50, 
    "buy_angle_xa": -50, 
    "buy_executed_id": null, 
    "buy_price": 13, 
    "created": "2018-01-07T14:47:07.754055", 
    "id": 4, 
    "sell_angle": 15, 
    "sell_angle_hold": 50, 
    "sell_executed_id": null, 
    "sell_price": 13.5, 
    "symbol": "AMD", 
    "type": "calls"
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
Date: Sun, 07 Jan 2018 15:06:34 GMT
Expires: 0
Server: TwistedWeb/17.1.0
Transfer-Encoding: chunked
Vary: Origin

{
    "budget": 1000.0, 
    "business_id": 1, 
    "buy_angle": 15.0, 
    "buy_angle_hold": -50.0, 
    "buy_angle_xa": -50.0, 
    "buy_executed_id": null, 
    "buy_price": 13.0, 
    "created": "2018-01-07T14:47:07.754055", 
    "id": 4, 
    "sell_angle": 15.0, 
    "sell_angle_hold": 50.0, 
    "sell_executed_id": null, 
    "sell_price": 13.5, 
    "symbol": "AMD", 
    "type": "calls"
}
```


INSERT NEW Schedule
------
<code request-method="POST">**POST** schedule-trade</code>

You can insert new stock or COIN to monitor

### Example
```http
POST http://localhost:6789/schedule-trade
Authorization: Basic YW5kcmVpOmFuZHJlaTEyMzQ1IQ==
Content-Length: 270
Content-Type: application/json
Host: localhost:6789
Origin: http://localhost:6789

{
    "budget": 1000, 
    "buy_angle": 15, 
    "buy_angle_hold": -50, 
    "buy_angle_xa": -50, 
    "buy_executed_id": null, 
    "buy_price": 13, 
    "sell_angle": 15, 
    "sell_angle_hold": 50, 
    "sell_price": 13.5, 
    "symbol": "AMD", 
    "type": "calls"
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
Date: Sun, 07 Jan 2018 15:06:35 GMT
Expires: 0
Server: TwistedWeb/17.1.0
Transfer-Encoding: chunked
Vary: Origin

{
    "budget": 1000.0, 
    "business_id": 5, 
    "buy_angle": 15.0, 
    "buy_angle_hold": -50.0, 
    "buy_angle_xa": -50.0, 
    "buy_executed_id": null, 
    "buy_price": 13.0, 
    "created": "2018-01-07T15:06:35.323591", 
    "id": 5, 
    "sell_angle": 15.0, 
    "sell_angle_hold": 50.0, 
    "sell_executed_id": null, 
    "sell_price": 13.5, 
    "symbol": "AMD", 
    "type": "calls"
}
```

