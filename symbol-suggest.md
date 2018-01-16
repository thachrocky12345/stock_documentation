
Get suggest symbol what exists in the system
======

`/symbol-suggest`

This symbol suggestion and auto fill data

### Methods

Method | URL | Description
--- | --- | ---
**[GET](/documentation/endpoint/symbol-suggest#this-symbol-suggestion)** | `/symbol-suggest?search=bitcoin` | This symbol suggestion
**[GET](/documentation/endpoint/symbol-suggest#note-and-stoch_high-stock-low-to-monitor,-even-so,-user-also-can-input-his-own-way)** | `/symbol-suggest/auto-fill?symbol=BTC-USD` | note and stoch_high stock low to monitor, even so, user also can input his own way

### Object Attributes

Attribute | Type | Readonly | Nullable | Has Default
--- | --- | --- | --- | ---
`name` | text | &nbsp; | &nbsp; | &nbsp;
`symbol` | text | &nbsp; | &nbsp; | &nbsp;

This symbol suggestion
------
<code request-method="GET">**GET** /symbol-suggest?search=bitcoin</code>

It will execute every single new char that type in to get suggest symbol what exists in the system

### Query Parameters

Parameter | Type | Description
--- | --- | ---
`search` | string | This can be symbol of name of the stock



### Example
```http
GET http://localhost:6789/symbol-suggest?search=bitcoin
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
Date: Sat, 16 Dec 2017 15:38:02 GMT
Expires: 0
Server: TwistedWeb/17.1.0
Transfer-Encoding: chunked
Vary: Origin

[
    {
        "name": "Bitcoin USD", 
        "symbol": "BTC-USD"
    }, 
    {
        "name": "Bitcoin Investment Trust", 
        "symbol": "GBTC"
    }
]
```


note and stoch_high stock low to monitor, even so, user also can input his own way
------
<code request-method="GET">**GET** /symbol-suggest/auto-fill?symbol=BTC-USD</code>

Get suggestion for stock low and high as current price

### Query Parameters

Parameter | Type | Description
--- | --- | ---
`symbol` | string | This symbol must he at right url format example BTCUSD=X is BTCUSD%3DX



### Example
```http
GET http://localhost:6789/symbol-suggest/auto-fill?symbol=BTCUSD%3DX
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
Date: Sat, 16 Dec 2017 15:38:02 GMT
Expires: 0
Server: TwistedWeb/17.1.0
Transfer-Encoding: chunked
Vary: Origin

{
    "note": "BTC/USD", 
    "stock_high": 18867.924, 
    "stock_low": 17857.143, 
    "symbol": "BTCUSD=X"
}
```

