
Stock OPTIONS Monitor
======

`/monitor/<id>/options`

This is where the options for the stock that you are interested is saved

### Methods

Method | URL | Description
--- | --- | ---
**[GET](/documentation/endpoint/options_monitor#get-all-of-your-stocks-options)** | `/monitor/35/options` | GET ALL OF YOUR STOCKS OPTIONS
**[GET](/documentation/endpoint/options_monitor#check-by-options-id)** | `/monitor/<id>/options/<options_id>` | CHECK BY OPTIONS ID
**[GET](/documentation/endpoint/options_monitor#check-current-market-price-for-the-options)** | `/monitor/<id>/options/<options_id>/current` | CHECK CURRENT MARKET PRICE FOR THE OPTIONS
**[PUT](/documentation/endpoint/options_monitor#update-your-options-status)** | `/monitor/35/options` | UPDATE YOUR OPTIONS STATUS
**[GET](/documentation/endpoint/options_monitor#check-all-available-strikes-of-the-stock-options)** | `/monitor/<id>/strikes` | CHECK ALL AVAILABLE STRIKES OF THE STOCK OPTIONS
**[GET](/documentation/endpoint/options_monitor#check-all-available-expirations-of-the-stock-options)** | `/monitor/<id>/expirations` | CHECK ALL AVAILABLE EXPIRATIONS OF THE STOCK OPTIONS
**[POST](/documentation/endpoint/options_monitor#insert-new-options)** | `/monitor/35/options` | INSERT NEW OPTIONS

### Object Attributes

Attribute | Type | Readonly | Nullable | Has Default
--- | --- | --- | --- | ---
`active` | boolean | &nbsp; | &nbsp; | &bullet;
`created` | timestamp | &nbsp; | &nbsp; | &bullet;
`expired` | timestamp | &nbsp; | &nbsp; | &nbsp;
`id` | integer | &nbsp; | &nbsp; | &bullet;
`open_interest` | integer | &nbsp; | &bullet; | &nbsp;
`opt_high` | numeric | &nbsp; | &bullet; | &nbsp;
`opt_low` | numeric | &nbsp; | &bullet; | &nbsp;
`opt_type` | text | &nbsp; | &nbsp; | &nbsp;
`stock_monitor_id` | integer | &nbsp; | &nbsp; | &nbsp;
`strike` | numeric | &nbsp; | &nbsp; | &nbsp;
`volume` | integer | &nbsp; | &bullet; | &nbsp;

GET ALL OF YOUR STOCKS OPTIONS
------
<code request-method="GET">**GET** /monitor/35/options</code>

Get all options

### Example
```http
GET http://localhost:6789/monitor/35/options
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
Date: Sat, 09 Dec 2017 15:56:01 GMT
Expires: 0
Server: TwistedWeb/17.1.0
Transfer-Encoding: chunked
Vary: Origin

[
    {
        "active": true, 
        "created": "2017-12-09T14:41:29.652782", 
        "expired": "2017-12-15", 
        "id": 16, 
        "open_interest": null, 
        "opt_high": 1.0, 
        "opt_low": 0.5, 
        "opt_type": "calls", 
        "stock_monitor_id": 35, 
        "strike": 85.0, 
        "volume": null
    }
]
```


CHECK BY OPTIONS ID
------
<code request-method="GET">**GET** /monitor/&lt;id&gt;/options/&lt;options_id&gt;</code>

Get the options id

### Example
```http
GET http://localhost:6789/monitor/35/options/16
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
Date: Sat, 09 Dec 2017 15:56:01 GMT
Expires: 0
Server: TwistedWeb/17.1.0
Transfer-Encoding: chunked
Vary: Origin

{
    "active": true, 
    "created": "2017-12-09T14:41:29.652782", 
    "expired": "2017-12-15", 
    "id": 16, 
    "open_interest": null, 
    "opt_high": 1.0, 
    "opt_low": 0.5, 
    "opt_type": "calls", 
    "stock_monitor_id": 35, 
    "strike": 85.0, 
    "volume": null
}
```


CHECK CURRENT MARKET PRICE FOR THE OPTIONS
------
<code request-method="GET">**GET** /monitor/&lt;id&gt;/options/&lt;options_id&gt;/current</code>

Get current options price

### Example
```http
GET http://localhost:6789/monitor/35/options/16/current
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
Date: Sat, 09 Dec 2017 15:56:01 GMT
Expires: 0
Server: TwistedWeb/17.1.0
Transfer-Encoding: chunked
Vary: Origin

{
    "ask": {
        "fmt": "0.40", 
        "raw": 0.4
    }, 
    "bid": {
        "fmt": "0.36", 
        "raw": 0.36
    }, 
    "change": {
        "fmt": "0.26", 
        "raw": 0.26
    }, 
    "contractSize": "REGULAR", 
    "contractSymbol": "MSFT171215C00085000", 
    "currency": "USD", 
    "expiration": {
        "fmt": "2017-12-15", 
        "longFmt": "2017-12-15T00:00", 
        "raw": 1513296000
    }, 
    "impliedVolatility": {
        "fmt": "15.97%", 
        "raw": 0.1596763720703125
    }, 
    "inTheMoney": false, 
    "lastPrice": {
        "fmt": "0.38", 
        "raw": 0.38
    }, 
    "lastTradeDate": {
        "fmt": "2017-12-08", 
        "longFmt": "2017-12-08T20:59", 
        "raw": 1512766780
    }, 
    "openInterest": {
        "fmt": "20,524", 
        "longFmt": "20,524", 
        "raw": 20524
    }, 
    "percentChange": {
        "fmt": "216.67%", 
        "raw": 216.66667
    }, 
    "strike": {
        "fmt": "85.00", 
        "raw": 85.0
    }, 
    "volume": {
        "fmt": "8,375", 
        "longFmt": "8,375", 
        "raw": 8375
    }
}
```


UPDATE YOUR OPTIONS STATUS
------
<code request-method="PUT">**PUT** /monitor/35/options</code>

This Indicators are very important for reporting, monitor id must be included

### Example
```http
PUT http://localhost:6789/monitor/35/options
Authorization: Basic YW5kcmVpOmFuZHJlaTEyMzQ1IQ==
Content-Length: 177
Content-Type: application/json
Host: localhost:6789
Origin: http://localhost:6789

{
    "active": false, 
    "expired": "2017-12-15", 
    "id": 16, 
    "opt_high": 1.2, 
    "opt_low": 0.5, 
    "opt_type": "calls", 
    "strike": 85, 
    "volume": null
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
Date: Sat, 09 Dec 2017 15:56:02 GMT
Expires: 0
Server: TwistedWeb/17.1.0
Transfer-Encoding: chunked
Vary: Origin

{
    "active": false, 
    "created": "2017-12-09T14:41:29.652782", 
    "expired": "2017-12-15", 
    "id": 16, 
    "open_interest": null, 
    "opt_high": 1.2, 
    "opt_low": 0.5, 
    "opt_type": "calls", 
    "stock_monitor_id": 35, 
    "strike": 85.0, 
    "volume": null
}
```


CHECK ALL AVAILABLE STRIKES OF THE STOCK OPTIONS
------
<code request-method="GET">**GET** /monitor/&lt;id&gt;/strikes</code>

Get strikes for the options

### Example
```http
GET http://localhost:6789/monitor/35/strikes
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
Date: Sat, 09 Dec 2017 15:56:02 GMT
Expires: 0
Server: TwistedWeb/17.1.0
Transfer-Encoding: chunked
Vary: Origin

[
    42.5, 
    45.0, 
    47.5, 
    50.0, 
    55.0, 
    60.0, 
    62.5, 
    65.0, 
    67.5, 
    69.0, 
    70.0, 
    71.0, 
    71.5, 
    72.0, 
    72.5, 
    73.0, 
    73.5, 
    74.0, 
    74.5, 
    75.0, 
    75.5, 
    76.0, 
    76.5, 
    77.0, 
    77.5, 
    78.0, 
    78.5, 
    79.0, 
    79.5, 
    80.0, 
    80.5, 
    81.0, 
    81.5, 
    82.0, 
    82.5, 
    83.0, 
    83.5, 
    84.0, 
    84.5, 
    85.0, 
    85.5, 
    86.0, 
    86.5, 
    87.0, 
    87.5, 
    88.0, 
    88.5, 
    89.0, 
    89.5, 
    90.0, 
    90.5, 
    91.0, 
    91.5, 
    92.5, 
    95.0, 
    100.0, 
    105.0, 
    110.0
]
```


CHECK ALL AVAILABLE EXPIRATIONS OF THE STOCK OPTIONS
------
<code request-method="GET">**GET** /monitor/&lt;id&gt;/expirations</code>

Get expired date for the options

### Example
```http
GET http://localhost:6789/monitor/35/expirations
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
Date: Sat, 09 Dec 2017 15:56:03 GMT
Expires: 0
Server: TwistedWeb/17.1.0
Transfer-Encoding: chunked
Vary: Origin

{
    "2017-12-15 00:00:00": 1513296000, 
    "2017-12-22 00:00:00": 1513900800, 
    "2017-12-29 00:00:00": 1514505600, 
    "2018-01-05 00:00:00": 1515110400, 
    "2018-01-12 00:00:00": 1515715200, 
    "2018-01-19 00:00:00": 1516320000, 
    "2018-01-26 00:00:00": 1516924800, 
    "2018-02-16 00:00:00": 1518739200, 
    "2018-03-16 00:00:00": 1521158400, 
    "2018-04-20 00:00:00": 1524182400, 
    "2018-06-15 00:00:00": 1529020800, 
    "2018-07-20 00:00:00": 1532044800, 
    "2018-09-21 00:00:00": 1537488000, 
    "2019-01-18 00:00:00": 1547769600, 
    "2020-01-17 00:00:00": 1579219200
}
```


INSERT NEW OPTIONS
------
<code request-method="POST">**POST** /monitor/35/options</code>

You can insert new options for a certain stock

### Example
```http
POST http://localhost:6789/monitor/35/options
Authorization: Basic YW5kcmVpOmFuZHJlaTEyMzQ1IQ==
Content-Length: 161
Content-Type: application/json
Host: localhost:6789
Origin: http://localhost:6789

{
    "active": false, 
    "expired": "2017-12-15", 
    "opt_high": 1.2, 
    "opt_low": 0.5, 
    "opt_type": "puts", 
    "strike": 85, 
    "volume": null
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
Date: Sat, 09 Dec 2017 15:56:03 GMT
Expires: 0
Server: TwistedWeb/17.1.0
Transfer-Encoding: chunked
Vary: Origin

{
    "active": false, 
    "created": "2017-12-09T15:56:03.748363", 
    "expired": "2017-12-15", 
    "id": 17, 
    "open_interest": null, 
    "opt_high": 1.2, 
    "opt_low": 0.5, 
    "opt_type": "puts", 
    "stock_monitor_id": 35, 
    "strike": 85.0, 
    "volume": null
}
```

