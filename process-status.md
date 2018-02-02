
Auto trade process status
======

`/process-status`

When you doing the auto trade, it shows the status on the trading

### Methods

Method | URL | Description
--- | --- | ---
**[GET](/documentation/endpoint/process-status#get-process-status)** | `/process-status` | GET Process Status

### Object Attributes

Attribute | Type | Readonly | Nullable | Has Default
--- | --- | --- | --- | ---
`business_id` | integer | &nbsp; | &nbsp; | &nbsp;
`completed` | boolean | &nbsp; | &bullet; | &bullet;
`created` | timestamp | &nbsp; | &nbsp; | &bullet;
`host` | text | &nbsp; | &nbsp; | &nbsp;
`id` | integer | &nbsp; | &nbsp; | &bullet;
`only_consider` | text | &nbsp; | &bullet; | &nbsp;
`pid` | integer | &nbsp; | &nbsp; | &nbsp;
`status_running` | text | &nbsp; | &bullet; | &nbsp;
`symbol` | text | &nbsp; | &nbsp; | &nbsp;
`updated` | timestamp | &nbsp; | &nbsp; | &bullet;

GET Process Status
------
<code request-method="GET">**GET** /process-status</code>

Get full predict details

### Example
```http
GET http://localhost:6789/process-status
Authorization: Basic dGhhY2hidWk6NG44OW8zajgyNA==
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
Date: Fri, 02 Feb 2018 14:13:57 GMT
Expires: 0
Server: TwistedWeb/16.6.0
Transfer-Encoding: chunked
Vary: Origin

[
    {
        "business_id": 1, 
        "completed": false, 
        "created": "2018-02-02T08:31:58.712523-05:00", 
        "host": "ubu-ny3-8g-ipython", 
        "id": 110, 
        "only_consider": null, 
        "pid": 18803, 
        "status_running": "started", 
        "symbol": "CC", 
        "updated": "2018-02-02T08:31:58.712523-05:00"
    }, 
    {
        "business_id": 1, 
        "completed": false, 
        "created": "2018-02-02T08:31:58.812981-05:00", 
        "host": "ubu-ny3-8g-ipython", 
        "id": 111, 
        "only_consider": null, 
        "pid": 18822, 
        "status_running": "started", 
        "symbol": "M", 
        "updated": "2018-02-02T08:31:58.812981-05:00"
    }, 
    {
        "business_id": 1, 
        "completed": false, 
        "created": "2018-02-02T08:31:58.936046-05:00", 
        "host": "ubu-ny3-8g-ipython", 
        "id": 112, 
        "only_consider": null, 
        "pid": 18799, 
        "status_running": "started", 
        "symbol": "C", 
        "updated": "2018-02-02T08:31:58.936046-05:00"
    }, 
    {
        "business_id": 1, 
        "completed": false, 
        "created": "2018-02-02T08:31:58.936046-05:00", 
        "host": "ubu-ny3-8g-ipython", 
        "id": 115, 
        "only_consider": null, 
        "pid": 18836, 
        "status_running": "started", 
        "symbol": "GOOG", 
        "updated": "2018-02-02T08:31:58.936046-05:00"
    }, 
    {
        "business_id": 1, 
        "completed": false, 
        "created": "2018-02-02T08:31:58.936046-05:00", 
        "host": "ubu-ny3-8g-ipython", 
        "id": 113, 
        "only_consider": null, 
        "pid": 18838, 
        "status_running": "started", 
        "symbol": "KODK", 
        "updated": "2018-02-02T08:31:58.936046-05:00"
    }, 
    {
        "business_id": 1, 
        "completed": false, 
        "created": "2018-02-02T08:31:58.936046-05:00", 
        "host": "ubu-ny3-8g-ipython", 
        "id": 114, 
        "only_consider": null, 
        "pid": 18840, 
        "status_running": "started", 
        "symbol": "SKX", 
        "updated": "2018-02-02T08:31:58.936046-05:00"
    }, 
    {
        "business_id": 1, 
        "completed": false, 
        "created": "2018-02-02T08:31:59.074444-05:00", 
        "host": "ubu-ny3-8g-ipython", 
        "id": 118, 
        "only_consider": null, 
        "pid": 18844, 
        "status_running": "started", 
        "symbol": "AMD", 
        "updated": "2018-02-02T08:31:59.074444-05:00"
    }, 
    {
        "business_id": 1, 
        "completed": false, 
        "created": "2018-02-02T08:31:59.074444-05:00", 
        "host": "ubu-ny3-8g-ipython", 
        "id": 116, 
        "only_consider": null, 
        "pid": 18847, 
        "status_running": "Market Closed", 
        "symbol": "BAC", 
        "updated": "2018-02-02T08:32:00.318256-05:00"
    }, 
    {
        "business_id": 1, 
        "completed": false, 
        "created": "2018-02-02T08:31:59.074444-05:00", 
        "host": "ubu-ny3-8g-ipython", 
        "id": 117, 
        "only_consider": null, 
        "pid": 18846, 
        "status_running": "started", 
        "symbol": "GOOS", 
        "updated": "2018-02-02T08:31:59.074444-05:00"
    }, 
    {
        "business_id": 1, 
        "completed": false, 
        "created": "2018-02-02T08:31:59.209673-05:00", 
        "host": "ubu-ny3-8g-ipython", 
        "id": 121, 
        "only_consider": null, 
        "pid": 18809, 
        "status_running": "started", 
        "symbol": "AAPL", 
        "updated": "2018-02-02T08:31:59.209673-05:00"
    }, 
    {
        "business_id": 1, 
        "completed": false, 
        "created": "2018-02-02T08:31:59.209673-05:00", 
        "host": "ubu-ny3-8g-ipython", 
        "id": 123, 
        "only_consider": null, 
        "pid": 18824, 
        "status_running": "started", 
        "symbol": "AMZN", 
        "updated": "2018-02-02T08:31:59.209673-05:00"
    }, 
    {
        "business_id": 1, 
        "completed": false, 
        "created": "2018-02-02T08:31:59.209673-05:00", 
        "host": "ubu-ny3-8g-ipython", 
        "id": 129, 
        "only_consider": null, 
        "pid": 18807, 
        "status_running": "started", 
        "symbol": "BABA", 
        "updated": "2018-02-02T08:31:59.209673-05:00"
    }, 
    {
        "business_id": 1, 
        "completed": false, 
        "created": "2018-02-02T08:31:59.209673-05:00", 
        "host": "ubu-ny3-8g-ipython", 
        "id": 126, 
        "only_consider": null, 
        "pid": 18813, 
        "status_running": "started", 
        "symbol": "BIDU", 
        "updated": "2018-02-02T08:31:59.209673-05:00"
    }, 
    {
        "business_id": 1, 
        "completed": false, 
        "created": "2018-02-02T08:31:59.209673-05:00", 
        "host": "ubu-ny3-8g-ipython", 
        "id": 124, 
        "only_consider": null, 
        "pid": 18833, 
        "status_running": "started", 
        "symbol": "CHTR", 
        "updated": "2018-02-02T08:31:59.209673-05:00"
    }, 
    {
        "business_id": 1, 
        "completed": false, 
        "created": "2018-02-02T08:31:59.209673-05:00", 
        "host": "ubu-ny3-8g-ipython", 
        "id": 122, 
        "only_consider": null, 
        "pid": 18810, 
        "status_running": "started", 
        "symbol": "GE", 
        "updated": "2018-02-02T08:31:59.209673-05:00"
    }, 
    {
        "business_id": 1, 
        "completed": false, 
        "created": "2018-02-02T08:31:59.209673-05:00", 
        "host": "ubu-ny3-8g-ipython", 
        "id": 119, 
        "only_consider": null, 
        "pid": 18837, 
        "status_running": "started", 
        "symbol": "HVBTF", 
        "updated": "2018-02-02T08:31:59.209673-05:00"
    }, 
    {
        "business_id": 1, 
        "completed": false, 
        "created": "2018-02-02T08:31:59.209673-05:00", 
        "host": "ubu-ny3-8g-ipython", 
        "id": 125, 
        "only_consider": null, 
        "pid": 18832, 
        "status_running": "started", 
        "symbol": "NVDA", 
        "updated": "2018-02-02T08:31:59.209673-05:00"
    }, 
    {
        "business_id": 1, 
        "completed": false, 
        "created": "2018-02-02T08:31:59.209673-05:00", 
        "host": "ubu-ny3-8g-ipython", 
        "id": 130, 
        "only_consider": null, 
        "pid": 18843, 
        "status_running": "started", 
        "symbol": "TEUM", 
        "updated": "2018-02-02T08:31:59.209673-05:00"
    }, 
    {
        "business_id": 1, 
        "completed": false, 
        "created": "2018-02-02T08:31:59.209673-05:00", 
        "host": "ubu-ny3-8g-ipython", 
        "id": 128, 
        "only_consider": null, 
        "pid": 18839, 
        "status_running": "started", 
        "symbol": "TRIP", 
        "updated": "2018-02-02T08:31:59.209673-05:00"
    }, 
    {
        "business_id": 1, 
        "completed": false, 
        "created": "2018-02-02T08:31:59.209673-05:00", 
        "host": "ubu-ny3-8g-ipython", 
        "id": 127, 
        "only_consider": null, 
        "pid": 18820, 
        "status_running": "started", 
        "symbol": "TSLA", 
        "updated": "2018-02-02T08:31:59.209673-05:00"
    }, 
    {
        "business_id": 1, 
        "completed": false, 
        "created": "2018-02-02T08:31:59.332499-05:00", 
        "host": "ubu-ny3-8g-ipython", 
        "id": 135, 
        "only_consider": null, 
        "pid": 18835, 
        "status_running": "started", 
        "symbol": "BIIB", 
        "updated": "2018-02-02T08:31:59.332499-05:00"
    }, 
    {
        "business_id": 1, 
        "completed": false, 
        "created": "2018-02-02T08:31:59.332499-05:00", 
        "host": "ubu-ny3-8g-ipython", 
        "id": 134, 
        "only_consider": null, 
        "pid": 18842, 
        "status_running": "started", 
        "symbol": "GRPN", 
        "updated": "2018-02-02T08:31:59.332499-05:00"
    }, 
    {
        "business_id": 1, 
        "completed": false, 
        "created": "2018-02-02T08:31:59.332499-05:00", 
        "host": "ubu-ny3-8g-ipython", 
        "id": 137, 
        "only_consider": null, 
        "pid": 18868, 
        "status_running": "started", 
        "symbol": "MIHI", 
        "updated": "2018-02-02T08:31:59.332499-05:00"
    }, 
    {
        "business_id": 1, 
        "completed": false, 
        "created": "2018-02-02T08:31:59.332499-05:00", 
        "host": "ubu-ny3-8g-ipython", 
        "id": 136, 
        "only_consider": null, 
        "pid": 18849, 
        "status_running": "started", 
        "symbol": "NETE", 
        "updated": "2018-02-02T08:31:59.332499-05:00"
    }, 
    {
        "business_id": 1, 
        "completed": false, 
        "created": "2018-02-02T08:31:59.332499-05:00", 
        "host": "ubu-ny3-8g-ipython", 
        "id": 133, 
        "only_consider": null, 
        "pid": 18848, 
        "status_running": "started", 
        "symbol": "ORLY", 
        "updated": "2018-02-02T08:31:59.332499-05:00"
    }, 
    {
        "business_id": 1, 
        "completed": false, 
        "created": "2018-02-02T08:31:59.332499-05:00", 
        "host": "ubu-ny3-8g-ipython", 
        "id": 131, 
        "only_consider": null, 
        "pid": 18815, 
        "status_running": "started", 
        "symbol": "PCLN", 
        "updated": "2018-02-02T08:31:59.332499-05:00"
    }, 
    {
        "business_id": 1, 
        "completed": false, 
        "created": "2018-02-02T08:31:59.332499-05:00", 
        "host": "ubu-ny3-8g-ipython", 
        "id": 132, 
        "only_consider": null, 
        "pid": 18850, 
        "status_running": "started", 
        "symbol": "TWTR", 
        "updated": "2018-02-02T08:31:59.332499-05:00"
    }
]
```

