
Show current positions
======

`/positions`

This endpoint is use to get live positions support trading

### Methods

Method | URL | Description
--- | --- | ---
**[GET](/documentation/endpoint/positions#get-current-position)** | `/positions` | GET current position
**[GET](/documentation/endpoint/positions#get-specific-position)** | `/positions/<id>` | GET specific position
**[GET](/documentation/endpoint/positions#get-current-orders)** | `/etrade/order` | GET current orders

### Object Attributes

Attribute | Type | Readonly | Nullable | Has Default
--- | --- | --- | --- | ---
`alert` | None | &nbsp; | &bullet; | &nbsp;
`auto_trade` | None | &nbsp; | &bullet; | &nbsp;
`bought_price` | None | &nbsp; | &bullet; | &nbsp;
`call_put` | None | &nbsp; | &bullet; | &nbsp;
`completed` | timestamp | &nbsp; | &bullet; | &nbsp;
`cost_basic` | None | &nbsp; | &bullet; | &nbsp;
`created` | timestamp | &nbsp; | &nbsp; | &bullet;
`current_price` | None | &nbsp; | &bullet; | &nbsp;
`daily_angles` | None | &nbsp; | &bullet; | &nbsp;
`description` | None | &nbsp; | &bullet; | &nbsp;
`exp_day` | None | &nbsp; | &bullet; | &nbsp;
`exp_month` | None | &nbsp; | &bullet; | &nbsp;
`exp_year` | None | &nbsp; | &bullet; | &nbsp;
`id` | integer | &bullet; | &nbsp; | &bullet;
`last_updated` | timestamp | &nbsp; | &bullet; | &nbsp;
`long_or_short` | None | &nbsp; | &bullet; | &nbsp;
`market_value` | None | &nbsp; | &bullet; | &nbsp;
`predict` | None | &nbsp; | &bullet; | &nbsp;
`profit` | None | &nbsp; | &bullet; | &nbsp;
`qty` | None | &nbsp; | &bullet; | &nbsp;
`strike_price` | None | &nbsp; | &bullet; | &nbsp;
`symbol` | text | &nbsp; | &nbsp; | &nbsp;
`type_code` | None | &nbsp; | &bullet; | &nbsp;

GET current position
------
<code request-method="GET">**GET** /positions</code>

GET current positions

### Example
```http
GET http://localhost:6789/positions
Authorization: Basic dGhhY2hidWk6NG44OW8zajgyNA==
Host: localhost:6789
Origin: http://localhost:6789
```

```http
HTTP/1.1 200 Ok
Access-Control-Allow-Credentials: true
Access-Control-Allow-Headers: Suppress-WWW-Authenticate, Content-Type, Authorization, Vary
Access-Control-Allow-Methods: GET, PUT, POST, DELETE, HEAD, OPTIONS
Access-Control-Allow-Origin: *
Access-Control-Max-Age: 3600
Cache-Control: no-store, must-revalidate
Content-Type: application/json
Date: Mon, 23 Apr 2018 22:01:41 GMT
Expires: 0
Server: TwistedWeb/16.6.0
Transfer-Encoding: chunked
Vary: Origin

[
    {
        "alert": false, 
        "auto_trade": false, 
        "bought_price": 126.45599999999999, 
        "call_put": "CALL", 
        "completed": null, 
        "cost_basic": 632.28, 
        "created": "2018-04-23T15:33:28.261780-04:00", 
        "current_price": 1.08, 
        "description": "ROKU Apr 27 '18 $32 Call", 
        "exp_day": 27, 
        "exp_month": 4, 
        "exp_year": 2018, 
        "id": 1, 
        "last_updated": "2018-04-23T16:11:30.053537-04:00", 
        "long_or_short": "LONG", 
        "market_value": 537.5, 
        "predict": {
            "action": "Hold", 
            "angle": 18.034455555733125, 
            "current_price": 32.27, 
            "days_angle": {
                "momentum_angle_14days": -0.13714677673131134, 
                "momentum_angle_30days": 4.3170570840267555, 
                "momentum_angle_7days": -7.436395281644331
            }, 
            "predict_price": 32.46305205480894, 
            "score": 0.0
        }, 
        "profit": -94.77999999999997, 
        "qty": 5, 
        "strike_price": 32.0, 
        "symbol": "ROKU", 
        "type_code": "OPTN"
    }, 
    {
        "alert": false, 
        "auto_trade": false, 
        "bought_price": 97.4572972972973, 
        "call_put": "CALL", 
        "completed": null, 
        "cost_basic": 3605.92, 
        "created": "2018-04-23T15:33:28.423534-04:00", 
        "current_price": 0.18, 
        "description": "WMT Apr 27 '18 $88 Call", 
        "exp_day": 27, 
        "exp_month": 4, 
        "exp_year": 2018, 
        "id": 2, 
        "last_updated": "2018-04-23T16:11:30.093682-04:00", 
        "long_or_short": "LONG", 
        "market_value": 666.0, 
        "predict": {
            "action": "Buy", 
            "angle": -3.5838860119196574, 
            "current_price": 86.14, 
            "days_angle": {
                "momentum_angle_14days": 1.9644469628720453, 
                "momentum_angle_30days": -0.5495807410324248, 
                "momentum_angle_7days": -0.35862498456514086
            }, 
            "predict_price": 86.0027576223365, 
            "score": 6.734938400546371
        }, 
        "profit": -2939.92, 
        "qty": 37, 
        "strike_price": 88.0, 
        "symbol": "WMT", 
        "type_code": "OPTN"
    }
]
```


GET specific position
------
<code request-method="GET">**GET** /positions/&lt;id&gt;</code>

GET specific positions

### Example
```http
GET http://localhost:6789/positions/2
Authorization: Basic dGhhY2hidWk6NG44OW8zajgyNA==
Content-Type: application/json
Host: localhost:6789
Origin: http://localhost:6789
```

```http
HTTP/1.1 200 Ok
Access-Control-Allow-Credentials: true
Access-Control-Allow-Headers: Suppress-WWW-Authenticate, Content-Type, Authorization, Vary
Access-Control-Allow-Methods: GET, PUT, POST, DELETE, HEAD, OPTIONS
Access-Control-Allow-Origin: *
Access-Control-Max-Age: 3600
Cache-Control: no-store, must-revalidate
Content-Type: application/json
Date: Mon, 23 Apr 2018 22:01:41 GMT
Expires: 0
Server: TwistedWeb/16.6.0
Transfer-Encoding: chunked
Vary: Origin

{
    "alert": false, 
    "auto_trade": false, 
    "bought_price": 97.4572972972973, 
    "call_put": "CALL", 
    "completed": null, 
    "cost_basic": 3605.92, 
    "created": "2018-04-23T15:33:28.423534-04:00", 
    "current_price": 0.18, 
    "daily_angles": {
        "fourteen_days": {
            "mean_square_error": 0.4148302282332971, 
            "predict_price": 87.63295857988146, 
            "predict_time": "2018-04-27", 
            "variance_score": 0.25403389567865353
        }, 
        "seven_days": {
            "mean_square_error": 0.4361469298245456, 
            "predict_price": 86.84947368421047, 
            "predict_time": "2018-04-25", 
            "variance_score": 0.012121238085821662
        }, 
        "thirty_days": {
            "mean_square_error": 0.8177771230993379, 
            "predict_price": 86.5128427074169, 
            "predict_time": "2018-05-03", 
            "variance_score": 0.013231739896001347
        }
    }, 
    "description": "WMT Apr 27 '18 $88 Call", 
    "exp_day": 27, 
    "exp_month": 4, 
    "exp_year": 2018, 
    "id": 2, 
    "last_updated": "2018-04-23T16:11:30.093682-04:00", 
    "long_or_short": "LONG", 
    "market_value": 666.0, 
    "predict": {
        "action": "Buy", 
        "angle": -3.5838860119196574, 
        "current_price": 86.14, 
        "days_angle": {
            "momentum_angle_14days": 1.9644469628720453, 
            "momentum_angle_30days": -0.5495807410324248, 
            "momentum_angle_7days": -0.35862498456514086
        }, 
        "predict_price": 86.0027576223365, 
        "score": 6.734938400546371
    }, 
    "profit": -2939.92, 
    "qty": 37, 
    "strike_price": 88.0, 
    "symbol": "WMT", 
    "type_code": "OPTN"
}
```


GET current orders
------
<code request-method="GET">**GET** /etrade/order</code>

GET  current placing orders

### Example
```http
GET http://localhost:6789/etrade/order
Authorization: Basic dGhhY2hidWk6NG44OW8zajgyNA==
Content-Type: application/json
Host: localhost:6789
Origin: http://localhost:6789
```

```http
HTTP/1.1 200 Ok
Access-Control-Allow-Credentials: true
Access-Control-Allow-Headers: Suppress-WWW-Authenticate, Content-Type, Authorization, Vary
Access-Control-Allow-Methods: GET, PUT, POST, DELETE, HEAD, OPTIONS
Access-Control-Allow-Origin: *
Access-Control-Max-Age: 3600
Cache-Control: no-store, must-revalidate
Content-Type: application/json
Date: Mon, 23 Apr 2018 22:01:43 GMT
Expires: 0
Server: TwistedWeb/16.6.0
Transfer-Encoding: chunked
Vary: Origin

[
    {
        "allOrNone": false, 
        "legDetails": {
            "estimatedCommission": 5.85, 
            "estimatedFees": 0, 
            "executedPrice": 0.68, 
            "filledQuantity": 2, 
            "legNumber": 1, 
            "orderAction": "SELL_CLOSE", 
            "orderedQuantity": 2, 
            "symbolDescription": "TSLA APR 310 Call", 
            "symbolInfo": {
                "callPut": "CALL", 
                "expDay": 27, 
                "expMonth": 4, 
                "expYear": 2018, 
                "strikePrice": 310, 
                "symbol": "TSLA"
            }
        }, 
        "limitPrice": 0, 
        "orderExecutedTime": 1524505563905, 
        "orderId": 1460, 
        "orderPlacedTime": 1524505563290, 
        "orderStatus": "EXECUTED", 
        "orderTerm": "GOOD_FOR_DAY", 
        "orderType": "OPTN", 
        "orderValue": 118.112577, 
        "priceType": "MARKET", 
        "replacesOrderId": 1457, 
        "stopPrice": 0
    }, 
    {
        "allOrNone": false, 
        "legDetails": {
            "estimatedCommission": 6.75, 
            "estimatedFees": 0, 
            "executedPrice": 0.48, 
            "filledQuantity": 4, 
            "legNumber": 1, 
            "orderAction": "SELL_CLOSE", 
            "orderedQuantity": 4, 
            "symbolDescription": "NVDA APR 237.5 Call", 
            "symbolInfo": {
                "callPut": "CALL", 
                "expDay": 27, 
                "expMonth": 4, 
                "expYear": 2018, 
                "strikePrice": "237.50", 
                "symbol": "NVDA"
            }
        }, 
        "limitPrice": 0, 
        "orderExecutedTime": 1524505544928, 
        "orderId": 1459, 
        "orderPlacedTime": 1524505543229, 
        "orderStatus": "EXECUTED", 
        "orderTerm": "GOOD_FOR_DAY", 
        "orderType": "OPTN", 
        "orderValue": 181.175177, 
        "priceType": "MARKET", 
        "replacesOrderId": 1455, 
        "stopPrice": 0
    }, 
    {
        "allOrNone": false, 
        "legDetails": {
            "estimatedCommission": 21.6, 
            "estimatedFees": 0, 
            "executedPrice": 0, 
            "filledQuantity": 0, 
            "legNumber": 1, 
            "orderAction": "SELL_CLOSE", 
            "orderedQuantity": 37, 
            "symbolDescription": "WMT APR 88 Call", 
            "symbolInfo": {
                "callPut": "CALL", 
                "expDay": 27, 
                "expMonth": 4, 
                "expYear": 2018, 
                "strikePrice": 88, 
                "symbol": "WMT"
            }
        }, 
        "limitPrice": 1.5, 
        "orderExecutedTime": null, 
        "orderId": 1458, 
        "orderPlacedTime": 1524491596312, 
        "orderStatus": "OPEN", 
        "orderTerm": "GOOD_UNTIL_CANCEL", 
        "orderType": "OPTN", 
        "orderValue": 5527.708077, 
        "priceType": "LIMIT", 
        "replacesOrderId": null, 
        "stopPrice": 0
    }, 
    {
        "allOrNone": false, 
        "legDetails": {
            "estimatedCommission": 7.2, 
            "estimatedFees": 0, 
            "executedPrice": 0, 
            "filledQuantity": 0, 
            "legNumber": 1, 
            "orderAction": "SELL_CLOSE", 
            "orderedQuantity": 5, 
            "symbolDescription": "ROKU APR 32 Call", 
            "symbolInfo": {
                "callPut": "CALL", 
                "expDay": 27, 
                "expMonth": 4, 
                "expYear": 2018, 
                "strikePrice": 32, 
                "symbol": "ROKU"
            }
        }, 
        "limitPrice": 5, 
        "orderExecutedTime": null, 
        "orderId": 1456, 
        "orderPlacedTime": 1524491535502, 
        "orderStatus": "OPEN", 
        "orderTerm": "GOOD_UNTIL_CANCEL", 
        "orderType": "OPTN", 
        "orderValue": 2492.706477, 
        "priceType": "LIMIT", 
        "replacesOrderId": null, 
        "stopPrice": 0
    }, 
    {
        "allOrNone": false, 
        "legDetails": {
            "estimatedCommission": 5.4, 
            "estimatedFees": 0, 
            "executedPrice": 0.29, 
            "filledQuantity": 1, 
            "legNumber": 1, 
            "orderAction": "BUY_OPEN", 
            "orderedQuantity": 1, 
            "symbolDescription": "WMT APR 88 Call", 
            "symbolInfo": {
                "callPut": "CALL", 
                "expDay": 27, 
                "expMonth": 4, 
                "expYear": 2018, 
                "strikePrice": 88, 
                "symbol": "WMT"
            }
        }, 
        "limitPrice": 0, 
        "orderExecutedTime": 1524491292605, 
        "orderId": 1454, 
        "orderPlacedTime": 1524491291832, 
        "orderStatus": "EXECUTED", 
        "orderTerm": "GOOD_FOR_DAY", 
        "orderType": "OPTN", 
        "orderValue": 34.4167, 
        "priceType": "MARKET", 
        "replacesOrderId": null, 
        "stopPrice": 0
    }
]
```

