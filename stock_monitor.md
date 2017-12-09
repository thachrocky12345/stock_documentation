
Stock Monitor
======

`/monitor`

This is where all the stock and options that you are interested is saved

### Methods

Method | URL | Description
--- | --- | ---
**[GET](/documentation/endpoint/stock_monitor#get-all-of-your-stocks)** | `monitor` | GET ALL OF YOUR STOCKS
**[GET](/documentation/endpoint/stock_monitor#check-specific-stocks)** | `/monitor?symbol=CCC` | CHECK SPECIFIC STOCKS
**[GET](/documentation/endpoint/stock_monitor#check-by-monitor-id)** | `/monitor/<id>` | CHECK BY MONITOR ID
**[GET](/documentation/endpoint/stock_monitor#check-current-market-price-for-the-stock)** | `/monitor/<id>/current` | CHECK CURRENT MARKET PRICE FOR THE STOCK
**[PUT](/documentation/endpoint/stock_monitor#update-your-monitor-status)** | `monitor` | UPDATE YOUR MONITOR STATUS
**[POST](/documentation/endpoint/stock_monitor#insert-new-stock-to-monitor)** | `monitor` | INSERT NEW STOCK TO Monitor

### Object Attributes

Attribute | Type | Readonly | Nullable | Has Default
--- | --- | --- | --- | ---
`active` | boolean | &nbsp; | &nbsp; | &bullet;
`angle_down` | numeric | &nbsp; | &bullet; | &nbsp;
`angle_up` | numeric | &nbsp; | &bullet; | &nbsp;
`business_id` | integer | &nbsp; | &nbsp; | &bullet;
`change_percent` | numeric | &nbsp; | &bullet; | &nbsp;
`check_acquired` | boolean | &nbsp; | &nbsp; | &bullet;
`created` | timestamp | &nbsp; | &nbsp; | &bullet;
`email` | boolean | &nbsp; | &nbsp; | &bullet;
`id` | integer | &nbsp; | &nbsp; | &bullet;
`international` | boolean | &nbsp; | &nbsp; | &bullet;
`note` | text | &nbsp; | &bullet; | &nbsp;
`options` | None | &nbsp; | &bullet; | &nbsp;
`priority` | integer | &nbsp; | &nbsp; | &bullet;
`repeat_time` | integer | &nbsp; | &nbsp; | &bullet;
`stock_high` | numeric | &nbsp; | &bullet; | &nbsp;
`stock_low` | numeric | &nbsp; | &bullet; | &nbsp;
`symbol` | text | &nbsp; | &nbsp; | &nbsp;
`text_message` | boolean | &nbsp; | &nbsp; | &bullet;
`update_acquired` | boolean | &nbsp; | &nbsp; | &bullet;
`volume` | integer | &nbsp; | &bullet; | &nbsp;

GET ALL OF YOUR STOCKS
------
<code request-method="GET">**GET** monitor</code>

Get all stock

### Example
```http
GET http://localhost:6789/monitor
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
Date: Sat, 09 Dec 2017 15:55:59 GMT
Expires: 0
Server: TwistedWeb/17.1.0
Transfer-Encoding: chunked
Vary: Origin

[
    {
        "active": true, 
        "angle_down": -3.0, 
        "angle_up": 3.0, 
        "business_id": 5, 
        "change_percent": 5.0, 
        "check_acquired": false, 
        "created": "2017-12-09T14:41:29.284172", 
        "email": true, 
        "id": 34, 
        "international": true, 
        "note": "Updated check percent change, stock high, stock_low, angle steep, active or not", 
        "options": [], 
        "priority": 1, 
        "repeat_time": 600, 
        "stock_high": 16000.0, 
        "stock_low": 10000.0, 
        "symbol": "BTCUSD=X", 
        "text_message": false, 
        "update_acquired": false, 
        "volume": null
    }, 
    {
        "active": true, 
        "angle_down": -5.0, 
        "angle_up": 5.0, 
        "business_id": 5, 
        "change_percent": 1.0, 
        "check_acquired": false, 
        "created": "2017-12-09T14:41:29.488953", 
        "email": true, 
        "id": 35, 
        "international": false, 
        "note": "test", 
        "options": [
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
        ], 
        "priority": 1, 
        "repeat_time": 60, 
        "stock_high": 84.0, 
        "stock_low": 70.0, 
        "symbol": "MSFT", 
        "text_message": false, 
        "update_acquired": false, 
        "volume": 5000000
    }
]
```


CHECK SPECIFIC STOCKS
------
<code request-method="GET">**GET** /monitor?symbol=CCC</code>

Get the right symbol

### Example
```http
GET http://localhost:6789/monitor?symbol=CCC
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
Date: Sat, 09 Dec 2017 15:56:00 GMT
Expires: 0
Server: TwistedWeb/17.1.0
Transfer-Encoding: chunked
Vary: Origin

[]
```


CHECK BY MONITOR ID
------
<code request-method="GET">**GET** /monitor/&lt;id&gt;</code>

Get the right id

### Example
```http
GET http://localhost:6789/monitor/34
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
Date: Sat, 09 Dec 2017 15:56:00 GMT
Expires: 0
Server: TwistedWeb/17.1.0
Transfer-Encoding: chunked
Vary: Origin

{
    "active": true, 
    "angle_down": -3.0, 
    "angle_up": 3.0, 
    "business_id": 5, 
    "change_percent": 5.0, 
    "check_acquired": false, 
    "created": "2017-12-09T14:41:29.284172", 
    "email": true, 
    "id": 34, 
    "international": true, 
    "note": "Updated check percent change, stock high, stock_low, angle steep, active or not", 
    "options": [], 
    "priority": 1, 
    "repeat_time": 600, 
    "stock_high": 16000.0, 
    "stock_low": 10000.0, 
    "symbol": "BTCUSD=X", 
    "text_message": false, 
    "update_acquired": false, 
    "volume": null
}
```


CHECK CURRENT MARKET PRICE FOR THE STOCK
------
<code request-method="GET">**GET** /monitor/&lt;id&gt;/current</code>

Get stock current

### Example
```http
GET http://localhost:6789/monitor/34/current
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
Date: Sat, 09 Dec 2017 15:56:00 GMT
Expires: 0
Server: TwistedWeb/17.1.0
Transfer-Encoding: chunked
Vary: Origin

{
    "algorithm": null, 
    "ask": 0.0, 
    "askSize": 0, 
    "averageDailyVolume10Day": 0, 
    "averageDailyVolume3Month": 0, 
    "bid": 0.0, 
    "bidSize": 0, 
    "bookValue": null, 
    "circulatingSupply": null, 
    "coinImageUrl": null, 
    "currency": "USD", 
    "dividendDate": null, 
    "earningsTimestamp": null, 
    "earningsTimestampEnd": null, 
    "earningsTimestampStart": null, 
    "epsForward": null, 
    "epsTrailingTwelveMonths": null, 
    "exchange": "CCY", 
    "exchangeDataDelayedBy": 0, 
    "exchangeTimezoneName": "Europe/London", 
    "exchangeTimezoneShortName": "GMT", 
    "fiftyDayAverage": 7601.0947, 
    "fiftyDayAverageChange": -6.7559995e-05, 
    "fiftyDayAverageChangePercent": -8.888192e-09, 
    "fiftyTwoWeekHigh": 19230.77, 
    "fiftyTwoWeekHighChange": -0.0012643699, 
    "fiftyTwoWeekHighChangePercent": -6.574724e-08, 
    "fiftyTwoWeekLow": 752.8023, 
    "fiftyTwoWeekLowChange": 1.2e-05, 
    "fiftyTwoWeekLowChangePercent": 1.594044e-08, 
    "financialCurrency": null, 
    "forwardPE": null, 
    "fromCurrency": null, 
    "fullExchangeName": "CCY", 
    "gmtOffSetMilliseconds": 0, 
    "language": "en-US", 
    "lastMarket": null, 
    "longName": null, 
    "market": "ccy_market", 
    "marketCap": null, 
    "marketState": "CLOSED", 
    "maxSupply": null, 
    "messageBoardId": "finmb_BTC_X", 
    "postMarketChange": null, 
    "postMarketChangePercent": null, 
    "postMarketPrice": null, 
    "postMarketTime": null, 
    "priceHint": 6, 
    "priceToBook": null, 
    "quoteSourceName": null, 
    "quoteType": "CURRENCY", 
    "regularMarketChange": -504.03223, 
    "regularMarketChangePercent": -3.1250033, 
    "regularMarketDayHigh": 16129.032, 
    "regularMarketDayLow": 15151.515, 
    "regularMarketOpen": 16129.032, 
    "regularMarketPreviousClose": 16129.032, 
    "regularMarketPrice": 15625.0, 
    "regularMarketTime": 1512834948, 
    "regularMarketVolume": 0, 
    "sharesOutstanding": null, 
    "shortName": "BTC/USD", 
    "sourceInterval": 15, 
    "startDate": null, 
    "symbol": "BTCUSD=X", 
    "tradeable": false, 
    "trailingAnnualDividendRate": null, 
    "trailingAnnualDividendYield": null, 
    "trailingPE": null, 
    "trailingThreeMonthNavReturns": null, 
    "trailingThreeMonthReturns": null, 
    "twoHundredDayAverage": 3699.7178, 
    "twoHundredDayAverageChange": -0.00020629089, 
    "twoHundredDayAverageChangePercent": -5.5758548e-08, 
    "volume24Hr": null, 
    "volumeAllCurrencies": null, 
    "ytdReturn": null
}
```


UPDATE YOUR MONITOR STATUS
------
<code request-method="PUT">**PUT** monitor</code>

This Indicators are very important for reporting, monitor id must be included

### Example
```http
PUT http://localhost:6789/monitor
Authorization: Basic YW5kcmVpOmFuZHJlaTEyMzQ1IQ==
Content-Length: 303
Content-Type: application/json
Host: localhost:6789
Origin: http://localhost:6789

{
    "active": true, 
    "angle_down": -3, 
    "angle_up": 3, 
    "change_percent": 5.0, 
    "email": true, 
    "id": 34, 
    "note": "Updated check percent change, stock high, stock_low, angle steep, active or not", 
    "stock_high": 16000, 
    "stock_low": 10000, 
    "text_message": false
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
Date: Sat, 09 Dec 2017 15:56:00 GMT
Expires: 0
Server: TwistedWeb/17.1.0
Transfer-Encoding: chunked
Vary: Origin

{
    "active": true, 
    "angle_down": -3.0, 
    "angle_up": 3.0, 
    "business_id": 5, 
    "change_percent": 5.0, 
    "check_acquired": false, 
    "created": "2017-12-09T14:41:29.284172", 
    "email": true, 
    "id": 34, 
    "international": true, 
    "note": "Updated check percent change, stock high, stock_low, angle steep, active or not", 
    "options": [], 
    "priority": 1, 
    "repeat_time": 600, 
    "stock_high": 16000.0, 
    "stock_low": 10000.0, 
    "symbol": "BTCUSD=X", 
    "text_message": false, 
    "update_acquired": false, 
    "volume": null
}
```


INSERT NEW STOCK TO Monitor
------
<code request-method="POST">**POST** monitor</code>

You can insert new stock or COIN to monitor

### Example
```http
POST http://localhost:6789/monitor
Authorization: Basic YW5kcmVpOmFuZHJlaTEyMzQ1IQ==
Content-Length: 276
Content-Type: application/json
Host: localhost:6789
Origin: http://localhost:6789

{
    "angle_down": -3, 
    "angle_up": 3, 
    "change_percent": 3, 
    "email": true, 
    "international": false, 
    "note": "Checking target price", 
    "stock_high": 21, 
    "stock_low": 19, 
    "symbol": "CCC", 
    "text_message": false, 
    "volume": 1000000
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
Date: Sat, 09 Dec 2017 15:56:00 GMT
Expires: 0
Server: TwistedWeb/17.1.0
Transfer-Encoding: chunked
Vary: Origin

{
    "active": true, 
    "angle_down": -3.0, 
    "angle_up": 3.0, 
    "business_id": 5, 
    "change_percent": 3.0, 
    "check_acquired": false, 
    "created": "2017-12-09T15:56:01.085658", 
    "email": true, 
    "id": 37, 
    "international": false, 
    "note": "Checking target price", 
    "options": [], 
    "priority": 10, 
    "repeat_time": 60, 
    "stock_high": 21.0, 
    "stock_low": 19.0, 
    "symbol": "CCC", 
    "text_message": false, 
    "update_acquired": false, 
    "volume": 1000000
}
```

