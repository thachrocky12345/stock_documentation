
Live real-time data
======

`/live-data`

provide real-time data with ask and bid price

### Methods

Method | URL | Description
--- | --- | ---
**[GET](/documentation/endpoint/live-data#get-live-data)** | `/live-data?symbol=e6_f` | GET live-data

### Object Attributes

Attribute | Type | Readonly | Nullable | Has Default
--- | --- | --- | --- | ---
`bar_ask` | numeric | &nbsp; | &bullet; | &nbsp;
`bar_bid` | numeric | &nbsp; | &bullet; | &nbsp;
`bar_close` | numeric | &nbsp; | &bullet; | &nbsp;
`bar_high` | numeric | &nbsp; | &bullet; | &nbsp;
`bar_low` | numeric | &nbsp; | &bullet; | &nbsp;
`bar_open` | numeric | &nbsp; | &bullet; | &nbsp;
`bar_vol` | integer | &nbsp; | &bullet; | &nbsp;
`cum_vol` | integer | &nbsp; | &bullet; | &nbsp;
`dtm` | timestamp | &nbsp; | &nbsp; | &nbsp;
`symbol` | text | &nbsp; | &nbsp; | &nbsp;

GET live-data
------
<code request-method="GET">**GET** /live-data?symbol=e6_f</code>

Get current live data

### Example
```http
GET http://localhost:6789/live-data?symbol=aapl
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
    "bar_ask": 175.57, 
    "bar_bid": 175.47, 
    "bar_close": 172.85, 
    "bar_high": 172.87, 
    "bar_low": 172.83, 
    "bar_open": 172.866, 
    "bar_vol": 22014, 
    "cum_vol": 1435350940, 
    "dtm": "2018-02-23T19:57:43-05:00", 
    "symbol": "AAPL"
}
```

