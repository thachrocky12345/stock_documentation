
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
Date: Tue, 16 Jan 2018 12:33:42 GMT
Expires: 0
Server: TwistedWeb/16.6.0
Transfer-Encoding: chunked
Vary: Origin

{
    "angle": null, 
    "current_time": "2018-01-16T07:33:42.420844", 
    "data": {
        "momentum_angle_14days": 3.841889577600042, 
        "momentum_angle_30days": 2.413074876202193, 
        "momentum_angle_7days": 2.7198907961297034
    }, 
    "history": [
        {
            "average_volume_7days_mils": 161.0979, 
            "close": 6.094285, 
            "date": "2005-04-12", 
            "high_low": 3.012471169686985, 
            "low_high": -5.271828665568369, 
            "open": 6.07, 
            "perc_pred_change": 0.77665568369028, 
            "volume": 245265300, 
            "volume_to_14days": 83.90209999999999, 
            "volume_to_30days": 83.90209999999999, 
            "volume_to_7days": 83.90209999999999, 
            "volume_to_prev": 245265094.5843
        }, 
        {
            "average_volume_7days_mils": 67.69583914285715, 
            "close": 61.472839, 
            "date": "2013-07-17", 
            "high_low": 1.4338430896115193, 
            "low_high": -0.46121190140292156, 
            "open": 61.174267, 
            "perc_pred_change": 0.3381438146206149, 
            "volume": 49737479, 
            "volume_to_14days": -18.695839142857153, 
            "volume_to_30days": -18.695839142857153, 
            "volume_to_7days": -18.695839142857153, 
            "volume_to_prev": 49737424.971401
        }, 
        {
            "average_volume_7days_mils": 70.03012614285714, 
            "close": 76.779977, 
            "date": "2014-03-27", 
            "high_low": -0.26162358942698494, 
            "low_high": -0.8708128092897722, 
            "open": 76.445706, 
            "perc_pred_change": -0.11212402172072294, 
            "volume": 55330425, 
            "volume_to_14days": -15.030126142857142, 
            "volume_to_30days": -15.030126142857142, 
            "volume_to_7days": -15.030126142857142, 
            "volume_to_prev": 55330350.605098
        }, 
        {
            "average_volume_7days_mils": 69.11947485714285, 
            "close": 76.694263, 
            "date": "2014-03-28", 
            "high_low": 0.32567141124208326, 
            "low_high": -0.6008419184520788, 
            "open": 76.321406, 
            "perc_pred_change": -0.022461588299356017, 
            "volume": 49703046, 
            "volume_to_14days": -20.119474857142848, 
            "volume_to_30days": -20.119474857142848, 
            "volume_to_7days": -20.119474857142848, 
            "volume_to_prev": 49702990.669575
        }, 
        {
            "average_volume_7days_mils": 27.468082857142857, 
            "close": 119.04, 
            "date": "2017-01-13", 
            "high_low": 0.6985943944112448, 
            "low_high": -0.3703391970372864, 
            "open": 118.81, 
            "perc_pred_change": 0.0, 
            "volume": 26083030, 
            "volume_to_14days": -1.468082857142857, 
            "volume_to_30days": -1.468082857142857, 
            "volume_to_7days": -1.468082857142857, 
            "volume_to_prev": 26083002.94245
        }, 
        {
            "average_volume_7days_mils": 21.611867142857143, 
            "close": 155.98, 
            "date": "2017-10-19", 
            "high_low": -2.3351825570894076, 
            "low_high": -3.057669978067346, 
            "open": 155.02, 
            "perc_pred_change": 0.1741710747000387, 
            "volume": 42357420, 
            "volume_to_14days": 20.388132857142857, 
            "volume_to_30days": 20.388132857142857, 
            "volume_to_7days": 20.388132857142857, 
            "volume_to_prev": 42357403.74715
        }
    ], 
    "predict": {
        "data": {
            "momentum_angle_14days": 3.841889577600042, 
            "momentum_angle_30days": 2.413074876202193, 
            "momentum_angle_7days": 2.7198907961297034
        }, 
        "estimate_change": 0.3016343595252741, 
        "pred": "Buy", 
        "score": 5.384763372475204
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
Date: Tue, 16 Jan 2018 12:33:43 GMT
Expires: 0
Server: TwistedWeb/16.6.0
Transfer-Encoding: chunked
Vary: Origin

{
    "going_down": [
        {
            "data": {
                "momentum_angle_14days": 11.297305218263364, 
                "momentum_angle_30days": 3.2920758614487875, 
                "momentum_angle_7days": 0.45883679075975936
            }, 
            "pred": "Buy", 
            "score": 14.194099572193888
        }, 
        {
            "data": {
                "momentum_angle_14days": 11.117305218263365, 
                "momentum_angle_30days": 3.1720758614487874, 
                "momentum_angle_7days": -0.14116320924024073
            }, 
            "pred": "Hold", 
            "score": 3.009707888535195
        }, 
        {
            "data": {
                "momentum_angle_14days": 10.817305218263364, 
                "momentum_angle_30days": 2.972075861448787, 
                "momentum_angle_7days": -1.1411632092402408
            }, 
            "pred": "Buy", 
            "score": 12.58997121890839
        }, 
        {
            "data": {
                "momentum_angle_14days": 10.637305218263364, 
                "momentum_angle_30days": 2.8520758614487876, 
                "momentum_angle_7days": -1.741163209240241
            }, 
            "pred": "Hold", 
            "score": 10.879209941577148
        }, 
        {
            "data": {
                "momentum_angle_14days": 10.517305218263365, 
                "momentum_angle_30days": 2.7720758614487875, 
                "momentum_angle_7days": -2.141163209240241
            }, 
            "pred": "Sell", 
            "score": 0.820483662044277
        }, 
        {
            "data": {
                "momentum_angle_14days": 10.217305218263364, 
                "momentum_angle_30days": 2.5720758614487873, 
                "momentum_angle_7days": -3.141163209240241
            }, 
            "pred": "Buy", 
            "score": 12.276814224193792
        }, 
        {
            "data": {
                "momentum_angle_14days": 9.977305218263364, 
                "momentum_angle_30days": 2.4120758614487876, 
                "momentum_angle_7days": -3.941163209240241
            }, 
            "pred": "Sell", 
            "score": 10.122922406657137
        }, 
        {
            "data": {
                "momentum_angle_14days": 9.917305218263365, 
                "momentum_angle_30days": 2.3720758614487876, 
                "momentum_angle_7days": -4.141163209240241
            }, 
            "pred": "Buy", 
            "score": 3.642360088550799
        }, 
        {
            "data": {
                "momentum_angle_14days": 9.497305218263364, 
                "momentum_angle_30days": 2.0920758614487873, 
                "momentum_angle_7days": -5.54116320924024
            }, 
            "pred": "Buy", 
            "score": 24.596106498509577
        }
    ], 
    "going_up": [
        {
            "data": {
                "momentum_angle_14days": 11.297305218263364, 
                "momentum_angle_30days": 3.2920758614487875, 
                "momentum_angle_7days": 0.45883679075975936
            }, 
            "pred": "Sell", 
            "score": 11.786052943323595
        }, 
        {
            "data": {
                "momentum_angle_14days": 11.357305218263365, 
                "momentum_angle_30days": 3.3320758614487875, 
                "momentum_angle_7days": 0.6588367907597594
            }, 
            "pred": "Buy", 
            "score": 14.194099572193888
        }, 
        {
            "data": {
                "momentum_angle_14days": 11.477305218263364, 
                "momentum_angle_30days": 3.4120758614487876, 
                "momentum_angle_7days": 1.0588367907597593
            }, 
            "pred": "Sell", 
            "score": 3.0150869407497654
        }, 
        {
            "data": {
                "momentum_angle_14days": 11.537305218263365, 
                "momentum_angle_30days": 3.4520758614487876, 
                "momentum_angle_7days": 1.2588367907597595
            }, 
            "pred": "Sell", 
            "score": 4.1458221929597014
        }, 
        {
            "data": {
                "momentum_angle_14days": 11.777305218263365, 
                "momentum_angle_30days": 3.612075861448788, 
                "momentum_angle_7days": 2.0588367907597593
            }, 
            "pred": "Sell", 
            "score": 13.702769988044981
        }, 
        {
            "data": {
                "momentum_angle_14days": 12.377305218263364, 
                "momentum_angle_30days": 4.012075861448787, 
                "momentum_angle_7days": 4.058836790759759
            }, 
            "pred": "Hold", 
            "score": 39.00889004749953
        }, 
        {
            "data": {
                "momentum_angle_14days": 12.677305218263363, 
                "momentum_angle_30days": 4.212075861448787, 
                "momentum_angle_7days": 5.05883679075976
            }, 
            "pred": "Buy", 
            "score": 11.825533235554934
        }, 
        {
            "data": {
                "momentum_angle_14days": 12.737305218263364, 
                "momentum_angle_30days": 4.2520758614487875, 
                "momentum_angle_7days": 5.25883679075976
            }, 
            "pred": "Hold", 
            "score": 12.993022537706695
        }, 
        {
            "data": {
                "momentum_angle_14days": 12.857305218263365, 
                "momentum_angle_30days": 4.3320758614487875, 
                "momentum_angle_7days": 5.65883679075976
            }, 
            "pred": "Sell", 
            "score": 12.703003576817112
        }, 
        {
            "data": {
                "momentum_angle_14days": 12.977305218263364, 
                "momentum_angle_30days": 4.412075861448788, 
                "momentum_angle_7days": 6.05883679075976
            }, 
            "pred": "Sell", 
            "score": 0.00819482143455294
        }, 
        {
            "data": {
                "momentum_angle_14days": 13.397305218263364, 
                "momentum_angle_30days": 4.692075861448788, 
                "momentum_angle_7days": 7.45883679075976
            }, 
            "pred": "Sell", 
            "score": 0.2517150649811978
        }, 
        {
            "data": {
                "momentum_angle_14days": 13.517305218263365, 
                "momentum_angle_30days": 4.772075861448788, 
                "momentum_angle_7days": 7.85883679075976
            }, 
            "pred": "Buy", 
            "score": 21.924912215125833
        }, 
        {
            "data": {
                "momentum_angle_14days": 13.577305218263366, 
                "momentum_angle_30days": 4.812075861448788, 
                "momentum_angle_7days": 8.05883679075976
            }, 
            "pred": "Sell", 
            "score": 0.07402581372632855
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
Authorization: Basic YW5kcmVpOmFuZHJlaTEyMzQ1IQ==
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
Date: Tue, 16 Jan 2018 12:33:43 GMT
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
            "pred": "Sell", 
            "score": 0.7146185948614461
        }, 
        {
            "data": {
                "momentum_angle_14days": 1.8380327667688987, 
                "momentum_angle_30days": 16.604173735002828, 
                "momentum_angle_7days": -0.1342827211715456
            }, 
            "pred": "Hold", 
            "score": 7.871201269377764
        }, 
        {
            "data": {
                "momentum_angle_14days": 1.5380327667688984, 
                "momentum_angle_30days": 16.404173735002825, 
                "momentum_angle_7days": -1.1342827211715458
            }, 
            "pred": "Sell", 
            "score": 7.365899456428286
        }, 
        {
            "data": {
                "momentum_angle_14days": 1.4780327667688986, 
                "momentum_angle_30days": 16.364173735002826, 
                "momentum_angle_7days": -1.3342827211715456
            }, 
            "pred": "Sell", 
            "score": 0.6726830826474114
        }, 
        {
            "data": {
                "momentum_angle_14days": 1.2380327667688986, 
                "momentum_angle_30days": 16.204173735002826, 
                "momentum_angle_7days": -2.134282721171546
            }, 
            "pred": "Buy", 
            "score": 11.168683103023493
        }, 
        {
            "data": {
                "momentum_angle_14days": 0.9980327667688986, 
                "momentum_angle_30days": 16.044173735002826, 
                "momentum_angle_7days": -2.9342827211715456
            }, 
            "pred": "Sell", 
            "score": 9.047763698068902
        }, 
        {
            "data": {
                "momentum_angle_14days": 0.9380327667688986, 
                "momentum_angle_30days": 16.004173735002826, 
                "momentum_angle_7days": -3.134282721171546
            }, 
            "pred": "Buy", 
            "score": 15.609209331009561
        }, 
        {
            "data": {
                "momentum_angle_14days": 0.6380327667688985, 
                "momentum_angle_30days": 15.804173735002825, 
                "momentum_angle_7days": -4.134282721171546
            }, 
            "pred": "Buy", 
            "score": 55.64460768587292
        }, 
        {
            "data": {
                "momentum_angle_14days": -0.2619672332311016, 
                "momentum_angle_30days": 15.204173735002826, 
                "momentum_angle_7days": -7.134282721171546
            }, 
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
            "pred": "Sell", 
            "score": 0.7146185948614461
        }, 
        {
            "data": {
                "momentum_angle_14days": 2.2580327667688986, 
                "momentum_angle_30days": 16.884173735002825, 
                "momentum_angle_7days": 1.2657172788284545
            }, 
            "pred": "Buy", 
            "score": 2.4753225397975807
        }, 
        {
            "data": {
                "momentum_angle_14days": 2.438032766768899, 
                "momentum_angle_30days": 17.004173735002826, 
                "momentum_angle_7days": 1.8657172788284546
            }, 
            "pred": "Buy", 
            "score": 13.850766534848827
        }, 
        {
            "data": {
                "momentum_angle_14days": 2.4980327667688984, 
                "momentum_angle_30days": 17.044173735002826, 
                "momentum_angle_7days": 2.0657172788284544
            }, 
            "pred": "Buy", 
            "score": 4.0688077698472345
        }, 
        {
            "data": {
                "momentum_angle_14days": 2.558032766768899, 
                "momentum_angle_30days": 17.084173735002825, 
                "momentum_angle_7days": 2.2657172788284545
            }, 
            "pred": "Sell", 
            "score": 4.684227299551269
        }, 
        {
            "data": {
                "momentum_angle_14days": 2.7980327667688987, 
                "momentum_angle_30days": 17.244173735002825, 
                "momentum_angle_7days": 3.065717278828455
            }, 
            "pred": "Sell", 
            "score": 1.377032539859815
        }, 
        {
            "data": {
                "momentum_angle_14days": 3.098032766768899, 
                "momentum_angle_30days": 17.444173735002828, 
                "momentum_angle_7days": 4.065717278828455
            }, 
            "pred": "Buy", 
            "score": 26.605715584610373
        }, 
        {
            "data": {
                "momentum_angle_14days": 3.2780327667688987, 
                "momentum_angle_30days": 17.564173735002825, 
                "momentum_angle_7days": 4.665717278828454
            }, 
            "pred": "Hold", 
            "score": 10.956556852172035
        }, 
        {
            "data": {
                "momentum_angle_14days": 3.3980327667688988, 
                "momentum_angle_30days": 17.644173735002827, 
                "momentum_angle_7days": 5.065717278828455
            }, 
            "pred": "Buy", 
            "score": 39.77645116107927
        }, 
        {
            "data": {
                "momentum_angle_14days": 3.518032766768899, 
                "momentum_angle_30days": 17.724173735002825, 
                "momentum_angle_7days": 5.465717278828454
            }, 
            "pred": "Sell", 
            "score": 0.8902454353109048
        }, 
        {
            "data": {
                "momentum_angle_14days": 3.6980327667688986, 
                "momentum_angle_30days": 17.844173735002826, 
                "momentum_angle_7days": 6.065717278828455
            }, 
            "pred": "Buy", 
            "score": 16.341216234187144
        }, 
        {
            "data": {
                "momentum_angle_14days": 4.058032766768899, 
                "momentum_angle_30days": 18.084173735002825, 
                "momentum_angle_7days": 7.265717278828454
            }, 
            "pred": "Sell", 
            "score": 0.04904578884840316
        }, 
        {
            "data": {
                "momentum_angle_14days": 4.298032766768898, 
                "momentum_angle_30days": 18.244173735002825, 
                "momentum_angle_7days": 8.065717278828455
            }, 
            "pred": "Sell", 
            "score": 0.3915632754342432
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
Authorization: Basic YW5kcmVpOmFuZHJlaTEyMzQ1IQ==
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
Date: Tue, 16 Jan 2018 12:33:44 GMT
Expires: 0
Server: TwistedWeb/16.6.0
Transfer-Encoding: chunked
Vary: Origin

[
    {
        "average_volume_7days_mils": 0.275497, 
        "close": 69.940278, 
        "date": "2012-03-01", 
        "high_low": 0.5567921538339095, 
        "low_high": -0.8749595098631808, 
        "open": 69.520017, 
        "perc_pred_change": -1.0817690104995228, 
        "volume": 213758, 
        "volume_to_14days": -0.275497, 
        "volume_to_30days": -0.275497, 
        "volume_to_7days": -0.275497, 
        "volume_to_prev": 213757.675328
    }, 
    {
        "average_volume_7days_mils": 0.306039, 
        "close": 80.491041, 
        "date": "2012-07-12", 
        "high_low": 1.7789072540483408, 
        "low_high": -1.072991677045031, 
        "open": 78.334438, 
        "perc_pred_change": 0.12706416557172467, 
        "volume": 427395, 
        "volume_to_14days": -0.306039, 
        "volume_to_30days": -0.306039, 
        "volume_to_7days": -0.306039, 
        "volume_to_prev": 427394.631584
    }, 
    {
        "average_volume_7days_mils": 0.29290328571428575, 
        "close": 80.590576, 
        "date": "2012-07-13", 
        "high_low": 2.8059750728492165, 
        "low_high": -0.10728715782645601, 
        "open": 80.404777, 
        "perc_pred_change": -0.4676625121415361, 
        "volume": 214089, 
        "volume_to_14days": -0.29290328571428575, 
        "volume_to_30days": -0.29290328571428575, 
        "volume_to_7days": -0.29290328571428575, 
        "volume_to_prev": 214088.572605
    }
]
```

