
Predict with history and details
======

`/predict`

This is where your prediction with score and history of date and detail so that you can check graph on daily-predict

### Methods

Method | URL | Description
--- | --- | ---
**[GET](/documentation/endpoint/predict#get-stock-predict)** | `/predict?symbol=ABC` | GET STOCK PREDICT
**[GET](/documentation/endpoint/predict#get-predict-trend-on-stock-movement)** | `/predict/trend?symbol=TSLA` | GET PREDICT TREND ON STOCK MOVEMENT
**[POST](/documentation/endpoint/predict#get-prediction-trend-for-a-certain-momentums-data)** | `/predict/data?symbol=CHTR` | GET PREDICTION TREND FOR A CERTAIN MOMENTUMS DATA
**[POST](/documentation/endpoint/predict#get-historical-data-for-a-certain-momentums-data)** | `/predict/history?symbol=CHTR` | GET HISTORICAL DATA FOR A CERTAIN MOMENTUMS DATA

### Object Attributes

Attribute | Type | Readonly | Nullable | Has Default
--- | --- | --- | --- | ---
`angle` | None | &nbsp; | &bullet; | &nbsp;
`current_price` | None | &nbsp; | &bullet; | &nbsp;
`current_time` | None | &nbsp; | &bullet; | &nbsp;
`data` | None | &nbsp; | &bullet; | &nbsp;
`history` | None | &nbsp; | &bullet; | &nbsp;
`predict` | None | &nbsp; | &bullet; | &nbsp;
`predict_price` | None | &nbsp; | &bullet; | &nbsp;
`predict_time` | None | &nbsp; | &bullet; | &nbsp;
`symbol` | None | &nbsp; | &bullet; | &nbsp;

GET STOCK PREDICT
------
<code request-method="GET">**GET** /predict?symbol=ABC</code>

Get full predict details

### Example
```http
GET http://localhost:6789/predict?symbol=AAPL
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
Date: Sun, 25 Feb 2018 16:25:46 GMT
Expires: 0
Server: TwistedWeb/16.6.0
Transfer-Encoding: chunked
Vary: Origin

{
    "angle": null, 
    "current_price": 175.51999999999998, 
    "current_time": "2018-02-25T06:25:46.576367-05:00", 
    "data": {
        "momentum_angle_14days": 12.053115603876263, 
        "momentum_angle_30days": 5.761908533752696, 
        "momentum_angle_7days": 1.9752461554804916
    }, 
    "history": [
        {
            "average_volume_7days_mils": 95.73, 
            "close": 1.964286, 
            "date": "2004-04-02", 
            "open": 1.982143, 
            "perc_pred_change": 3.14, 
            "today_high_prev_low_perc": 4.72, 
            "today_low_prev_high_perc": -0.14, 
            "volume_change_to_prev_mils": -10.96, 
            "volume_mils": 68.0, 
            "volume_to_14days": -27.73, 
            "volume_to_30days": -27.73, 
            "volume_to_7days": -27.73
        }, 
        {
            "average_volume_7days_mils": 83.49, 
            "close": 1.987857, 
            "date": "2004-04-06", 
            "open": 1.979286, 
            "perc_pred_change": -0.47, 
            "today_high_prev_low_perc": 2.56, 
            "today_low_prev_high_perc": -3.39, 
            "volume_change_to_prev_mils": -31.92, 
            "volume_mils": 64.0, 
            "volume_to_14days": -19.49, 
            "volume_to_30days": -19.49, 
            "volume_to_7days": -19.49
        }
    ], 
    "predict": {
        "data": {
            "momentum_angle_14days": 12.053115603876263, 
            "momentum_angle_30days": 5.761908533752696, 
            "momentum_angle_7days": 1.9752461554804916
        }, 
        "estimate_change": 0.6584153851601638, 
        "pred": "Buy", 
        "score": 22.552478386395094
    }, 
    "predict_price": null, 
    "predict_time": null, 
    "symbol": "AAPL"
}
```


GET PREDICT TREND ON STOCK MOVEMENT
------
<code request-method="GET">**GET** /predict/trend?symbol=TSLA</code>

This is all the possibility when stock is moving up and down

### Example
```http
GET http://localhost:6789/predict/trend?symbol=TSLA
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
Date: Sun, 25 Feb 2018 16:25:47 GMT
Expires: 0
Server: TwistedWeb/16.6.0
Transfer-Encoding: chunked
Vary: Origin

{
    "going_down": [
        {
            "data": {
                "momentum_angle_14days": 14.988258820689657, 
                "momentum_angle_30days": -3.799502184137873, 
                "momentum_angle_7days": 5.122457576122762
            }, 
            "history": [], 
            "pred": "Buy", 
            "score": 42.593116082368155
        }, 
        {
            "data": {
                "momentum_angle_14days": 14.988258820689657, 
                "momentum_angle_30days": -3.799502184137873, 
                "momentum_angle_7days": 5.122457576122762
            }, 
            "history": [], 
            "pred": "Sell", 
            "score": 34.866810364456285
        }, 
        {
            "data": {
                "momentum_angle_14days": 14.388258820689657, 
                "momentum_angle_30days": -4.199502184137873, 
                "momentum_angle_7days": 3.1224575761227618
            }, 
            "history": [], 
            "pred": "Sell", 
            "score": 13.54879748610632
        }, 
        {
            "data": {
                "momentum_angle_14days": 14.328258820689657, 
                "momentum_angle_30days": -4.239502184137873, 
                "momentum_angle_7days": 2.9224575761227616
            }, 
            "history": [], 
            "pred": "Buy", 
            "score": 34.57147177615574
        }
    ], 
    "going_up": [
        {
            "data": {
                "momentum_angle_14days": 14.988258820689657, 
                "momentum_angle_30days": -3.799502184137873, 
                "momentum_angle_7days": 5.122457576122762
            }, 
            "history": [], 
            "pred": "Buy", 
            "score": 42.593116082368155
        }, 
        {
            "data": {
                "momentum_angle_14days": 14.988258820689657, 
                "momentum_angle_30days": -3.799502184137873, 
                "momentum_angle_7days": 5.122457576122762
            }, 
            "history": [], 
            "pred": "Sell", 
            "score": 34.866810364456285
        }
    ]
}
```


GET PREDICTION TREND FOR A CERTAIN MOMENTUMS DATA
------
<code request-method="POST">**POST** /predict/data?symbol=CHTR</code>

You can insert new stock or COIN to monitor

### Example
```http
POST http://localhost:6789/predict/data?symbol=CHTR
Authorization: Basic a2Vubnk6a2VubnkxMjM0NSE=
Content-Length: 150
Content-Type: application/json
Host: localhost:6789
Origin: http://localhost:6789

{
    "momentum_angle_14days": 1.9580327667688986, 
    "momentum_angle_30days": 16.684173735002826, 
    "momentum_angle_7days": 0.2657172788284544
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
Date: Sun, 25 Feb 2018 16:25:48 GMT
Expires: 0
Server: TwistedWeb/16.6.0
Transfer-Encoding: chunked
Vary: Origin

{
    "going_down": [
        {
            "data": {
                "momentum_angle_14days": 1.9580327667688986, 
                "momentum_angle_30days": 16.684173735002826, 
                "momentum_angle_7days": 0.2657172788284544
            }, 
            "history": [
                {
                    "average_volume_7days_mils": 0.28, 
                    "close": 69.940278, 
                    "date": "2012-03-01", 
                    "open": 69.520017, 
                    "perc_pred_change": -1.08, 
                    "today_high_prev_low_perc": 0.56, 
                    "today_low_prev_high_perc": -0.87, 
                    "volume_change_to_prev_mils": -0.11, 
                    "volume_mils": 0.0, 
                    "volume_to_14days": -0.28, 
                    "volume_to_30days": -0.28, 
                    "volume_to_7days": -0.28
                }, 
                {
                    "average_volume_7days_mils": 0.31, 
                    "close": 80.491041, 
                    "date": "2012-07-12", 
                    "open": 78.334438, 
                    "perc_pred_change": 0.13, 
                    "today_high_prev_low_perc": 1.78, 
                    "today_low_prev_high_perc": -1.07, 
                    "volume_change_to_prev_mils": 0.06, 
                    "volume_mils": 0.0, 
                    "volume_to_14days": -0.31, 
                    "volume_to_30days": -0.31, 
                    "volume_to_7days": -0.31
                }, 
                {
                    "average_volume_7days_mils": 0.29, 
                    "close": 80.590576, 
                    "date": "2012-07-13", 
                    "open": 80.404777, 
                    "perc_pred_change": -0.47, 
                    "today_high_prev_low_perc": 2.81, 
                    "today_low_prev_high_perc": -0.11, 
                    "volume_change_to_prev_mils": -0.21, 
                    "volume_mils": 0.0, 
                    "volume_to_14days": -0.29, 
                    "volume_to_30days": -0.29, 
                    "volume_to_7days": -0.29
                }
            ], 
            "pred": "Sell", 
            "score": 0.7146185948614461
        }, 
        {
            "data": {
                "momentum_angle_14days": 1.3580327667688985, 
                "momentum_angle_30days": 16.284173735002827, 
                "momentum_angle_7days": -1.7342827211715455
            }, 
            "history": [
                {
                    "average_volume_7days_mils": 0.27, 
                    "close": 69.188232, 
                    "date": "2012-03-02", 
                    "open": 68.911744, 
                    "perc_pred_change": -0.34, 
                    "today_high_prev_low_perc": -0.48, 
                    "today_low_prev_high_perc": -1.49, 
                    "volume_change_to_prev_mils": -0.04, 
                    "volume_mils": 0.0, 
                    "volume_to_14days": -0.27, 
                    "volume_to_30days": -0.27, 
                    "volume_to_7days": -0.27
                }, 
                {
                    "average_volume_7days_mils": 1.61, 
                    "close": 397.05, 
                    "date": "2017-08-22", 
                    "open": 395.0, 
                    "perc_pred_change": -1.7, 
                    "today_high_prev_low_perc": 1.44, 
                    "today_low_prev_high_perc": -0.37, 
                    "volume_change_to_prev_mils": 0.03, 
                    "volume_mils": 0.0, 
                    "volume_to_14days": -1.61, 
                    "volume_to_30days": -1.61, 
                    "volume_to_7days": -1.61
                }
            ], 
            "pred": "Sell", 
            "score": 0.6726830826474114
        }, 
        {
            "data": {
                "momentum_angle_14days": 0.9380327667688986, 
                "momentum_angle_30days": 16.004173735002826, 
                "momentum_angle_7days": -3.134282721171546
            }, 
            "history": [], 
            "pred": "Buy", 
            "score": 15.609209331009561
        }, 
        {
            "data": {
                "momentum_angle_14days": 0.8780327667688987, 
                "momentum_angle_30days": 15.964173735002825, 
                "momentum_angle_7days": -3.3342827211715456
            }, 
            "history": [], 
            "pred": "Sell", 
            "score": 12.641799146534552
        }, 
        {
            "data": {
                "momentum_angle_14days": -0.2619672332311016, 
                "momentum_angle_30days": 15.204173735002826, 
                "momentum_angle_7days": -7.134282721171546
            }, 
            "history": [], 
            "pred": "Sell", 
            "score": 1.6214066880108993
        }
    ], 
    "going_up": [
        {
            "data": {
                "momentum_angle_14days": 1.9580327667688986, 
                "momentum_angle_30days": 16.684173735002826, 
                "momentum_angle_7days": 0.2657172788284544
            }, 
            "history": [
                {
                    "average_volume_7days_mils": 0.28, 
                    "close": 69.940278, 
                    "date": "2012-03-01", 
                    "open": 69.520017, 
                    "perc_pred_change": -1.08, 
                    "today_high_prev_low_perc": 0.56, 
                    "today_low_prev_high_perc": -0.87, 
                    "volume_change_to_prev_mils": -0.11, 
                    "volume_mils": 0.0, 
                    "volume_to_14days": -0.28, 
                    "volume_to_30days": -0.28, 
                    "volume_to_7days": -0.28
                }, 
                {
                    "average_volume_7days_mils": 0.31, 
                    "close": 80.491041, 
                    "date": "2012-07-12", 
                    "open": 78.334438, 
                    "perc_pred_change": 0.13, 
                    "today_high_prev_low_perc": 1.78, 
                    "today_low_prev_high_perc": -1.07, 
                    "volume_change_to_prev_mils": 0.06, 
                    "volume_mils": 0.0, 
                    "volume_to_14days": -0.31, 
                    "volume_to_30days": -0.31, 
                    "volume_to_7days": -0.31
                }, 
                {
                    "average_volume_7days_mils": 0.29, 
                    "close": 80.590576, 
                    "date": "2012-07-13", 
                    "open": 80.404777, 
                    "perc_pred_change": -0.47, 
                    "today_high_prev_low_perc": 2.81, 
                    "today_low_prev_high_perc": -0.11, 
                    "volume_change_to_prev_mils": -0.21, 
                    "volume_mils": 0.0, 
                    "volume_to_14days": -0.29, 
                    "volume_to_30days": -0.29, 
                    "volume_to_7days": -0.29
                }
            ], 
            "pred": "Sell", 
            "score": 0.7146185948614461
        }, 
        {
            "data": {
                "momentum_angle_14days": 1.9580327667688986, 
                "momentum_angle_30days": 16.684173735002826, 
                "momentum_angle_7days": 0.2657172788284544
            }, 
            "history": [
                {
                    "average_volume_7days_mils": 0.28, 
                    "close": 69.940278, 
                    "date": "2012-03-01", 
                    "open": 69.520017, 
                    "perc_pred_change": -1.08, 
                    "today_high_prev_low_perc": 0.56, 
                    "today_low_prev_high_perc": -0.87, 
                    "volume_change_to_prev_mils": -0.11, 
                    "volume_mils": 0.0, 
                    "volume_to_14days": -0.28, 
                    "volume_to_30days": -0.28, 
                    "volume_to_7days": -0.28
                }, 
                {
                    "average_volume_7days_mils": 0.31, 
                    "close": 80.491041, 
                    "date": "2012-07-12", 
                    "open": 78.334438, 
                    "perc_pred_change": 0.13, 
                    "today_high_prev_low_perc": 1.78, 
                    "today_low_prev_high_perc": -1.07, 
                    "volume_change_to_prev_mils": 0.06, 
                    "volume_mils": 0.0, 
                    "volume_to_14days": -0.31, 
                    "volume_to_30days": -0.31, 
                    "volume_to_7days": -0.31
                }, 
                {
                    "average_volume_7days_mils": 0.29, 
                    "close": 80.590576, 
                    "date": "2012-07-13", 
                    "open": 80.404777, 
                    "perc_pred_change": -0.47, 
                    "today_high_prev_low_perc": 2.81, 
                    "today_low_prev_high_perc": -0.11, 
                    "volume_change_to_prev_mils": -0.21, 
                    "volume_mils": 0.0, 
                    "volume_to_14days": -0.29, 
                    "volume_to_30days": -0.29, 
                    "volume_to_7days": -0.29
                }
            ], 
            "pred": "Hold", 
            "score": 0.15368879266042362
        }, 
        {
            "data": {
                "momentum_angle_14days": 2.978032766768899, 
                "momentum_angle_30days": 17.364173735002826, 
                "momentum_angle_7days": 3.665717278828455
            }, 
            "history": [], 
            "pred": "Sell", 
            "score": 1.377032539859815
        }
    ]
}
```


GET HISTORICAL DATA FOR A CERTAIN MOMENTUMS DATA
------
<code request-method="POST">**POST** /predict/history?symbol=CHTR</code>

You can insert new stock or COIN to monitor

### Example
```http
POST http://localhost:6789/predict/history?symbol=CHTR
Authorization: Basic a2Vubnk6a2VubnkxMjM0NSE=
Content-Length: 150
Content-Type: application/json
Host: localhost:6789
Origin: http://localhost:6789

{
    "momentum_angle_14days": 1.9580327667688986, 
    "momentum_angle_30days": 16.684173735002826, 
    "momentum_angle_7days": 0.2657172788284544
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
Date: Sun, 25 Feb 2018 16:25:49 GMT
Expires: 0
Server: TwistedWeb/16.6.0
Transfer-Encoding: chunked
Vary: Origin

[
    {
        "average_volume_7days_mils": 0.28, 
        "close": 69.940278, 
        "date": "2012-03-01", 
        "open": 69.520017, 
        "perc_pred_change": -1.08, 
        "today_high_prev_low_perc": 0.56, 
        "today_low_prev_high_perc": -0.87, 
        "volume_change_to_prev_mils": -0.11, 
        "volume_mils": 0.0, 
        "volume_to_14days": -0.28, 
        "volume_to_30days": -0.28, 
        "volume_to_7days": -0.28
    }, 
    {
        "average_volume_7days_mils": 0.31, 
        "close": 80.491041, 
        "date": "2012-07-12", 
        "open": 78.334438, 
        "perc_pred_change": 0.13, 
        "today_high_prev_low_perc": 1.78, 
        "today_low_prev_high_perc": -1.07, 
        "volume_change_to_prev_mils": 0.06, 
        "volume_mils": 0.0, 
        "volume_to_14days": -0.31, 
        "volume_to_30days": -0.31, 
        "volume_to_7days": -0.31
    }, 
    {
        "average_volume_7days_mils": 0.29, 
        "close": 80.590576, 
        "date": "2012-07-13", 
        "open": 80.404777, 
        "perc_pred_change": -0.47, 
        "today_high_prev_low_perc": 2.81, 
        "today_low_prev_high_perc": -0.11, 
        "volume_change_to_prev_mils": -0.21, 
        "volume_mils": 0.0, 
        "volume_to_14days": -0.29, 
        "volume_to_30days": -0.29, 
        "volume_to_7days": -0.29
    }
]
```

