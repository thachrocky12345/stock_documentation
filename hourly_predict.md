
Get hourly-predict data
======

`/hourly-predict`

This kind of intraday query, hour by hour, for all stocks

### Methods

Method | URL | Description
--- | --- | ---
**[GET](/documentation/endpoint/hourly_predict#get-hourly-predict-and-data-for-graph)** | `hourly-predict?symbol=CERN&today=2017-12-08&start=8-30&end=14-30` | Get Hourly Predict and data for graph
**[GET](/documentation/endpoint/hourly_predict#get-all-available-symbol)** | `/hourly-predict/available` | GET ALL AVAILABLE SYMBOL

### Object Attributes

Attribute | Type | Readonly | Nullable | Has Default
--- | --- | --- | --- | ---
`angle` | None | &nbsp; | &bullet; | &nbsp;
`coef` | None | &nbsp; | &bullet; | &nbsp;
`data` | None | &nbsp; | &bullet; | &nbsp;
`end` | None | &nbsp; | &bullet; | &nbsp;
`intercept` | None | &nbsp; | &bullet; | &nbsp;
`predict_price` | None | &nbsp; | &bullet; | &nbsp;
`predict_time` | None | &nbsp; | &bullet; | &nbsp;
`start` | None | &nbsp; | &bullet; | &nbsp;

Get Hourly Predict and data for graph
------
<code request-method="GET">**GET** hourly-predict?symbol=CERN&today=2017-12-08&start=8-30&end=14-30</code>

Get statistic report and data for date: 2017-12-08 from 8:30 to 14:30 NY's time

### Query Parameters

Parameter | Type | Description
--- | --- | ---
`end` | string | Time to end, example end=14-30, default: market closed 16:00
`start` | string | Time to start, example start=8-30, default: market open 9:30
`symbol` | string | This is must provide and accurately, you also can check /hourly-predict/available to get right symbol
`today` | string | This is the date you want to check, e.g:2017-12-08, default current date



### Example
```http
GET http://localhost:6789/hourly-predict?symbol=CERN&today=2017-12-08&start=8-30&end=14-30
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

{
    "angle": 8.868162224660056, 
    "coef": 2.0925467156435548e-05, 
    "data": [
        {
            "market_time": 1512747039, 
            "price": 69.88, 
            "volume": 144006
        }, 
        {
            "market_time": 1512747092, 
            "price": 69.86, 
            "volume": 145120
        }, 
        {
            "market_time": 1512747160, 
            "price": 69.91, 
            "volume": 146208
        }, 
        {
            "market_time": 1512747162, 
            "price": 69.91, 
            "volume": 147310
        }, 
        {
            "market_time": 1512747307, 
            "price": 69.9, 
            "volume": 153295
        }, 
        {
            "market_time": 1512747458, 
            "price": 69.91, 
            "volume": 155641
        }, 
        {
            "market_time": 1512747468, 
            "price": 69.91, 
            "volume": 157241
        }, 
        {
            "market_time": 1512747480, 
            "price": 69.93, 
            "volume": 157741
        }, 
        {
            "market_time": 1512747507, 
            "price": 69.98, 
            "volume": 158774
        }, 
        {
            "market_time": 1512757019, 
            "price": 70.33, 
            "volume": 374196
        }, 
        {
            "market_time": 1512757029, 
            "price": 70.33, 
            "volume": 374794
        }, 
        {
            "market_time": 1512757925, 
            "price": 70.27, 
            "volume": 393750
        }, 
        {
            "market_time": 1512758773, 
            "price": 70.2801, 
            "volume": 407290
        }, 
        {
            "market_time": 1512758860, 
            "price": 70.2687, 
            "volume": 408577
        }, 
        {
            "market_time": 1512758998, 
            "price": 70.265, 
            "volume": 409373
        }, 
        {
            "market_time": 1512759333, 
            "price": 70.32, 
            "volume": 415417
        }, 
        {
            "market_time": 1512759377, 
            "price": 70.33, 
            "volume": 416337
        }, 
        {
            "market_time": 1512759751, 
            "price": 70.28, 
            "volume": 423763
        }, 
        {
            "market_time": 1512759771, 
            "price": 70.3, 
            "volume": 424478
        }, 
        {
            "market_time": 1512759817, 
            "price": 70.2999, 
            "volume": 425670
        }, 
        {
            "market_time": 1512759839, 
            "price": 70.29, 
            "volume": 425891
        }, 
        {
            "market_time": 1512759844, 
            "price": 70.285, 
            "volume": 426491
        }, 
        {
            "market_time": 1512760022, 
            "price": 70.3299, 
            "volume": 428530
        }, 
        {
            "market_time": 1512760074, 
            "price": 70.32, 
            "volume": 430368
        }, 
        {
            "market_time": 1512760150, 
            "price": 70.33, 
            "volume": 431018
        }, 
        {
            "market_time": 1512760231, 
            "price": 70.31, 
            "volume": 431971
        }, 
        {
            "market_time": 1512760243, 
            "price": 70.31, 
            "volume": 432071
        }, 
        {
            "market_time": 1512760264, 
            "price": 70.31, 
            "volume": 432849
        }, 
        {
            "market_time": 1512760333, 
            "price": 70.315, 
            "volume": 433131
        }, 
        {
            "market_time": 1512760721, 
            "price": 70.31, 
            "volume": 444703
        }, 
        {
            "market_time": 1512760789, 
            "price": 70.32, 
            "volume": 445713
        }, 
        {
            "market_time": 1512760806, 
            "price": 70.33, 
            "volume": 446746
        }, 
        {
            "market_time": 1512760826, 
            "price": 70.3, 
            "volume": 447652
        }, 
        {
            "market_time": 1512760844, 
            "price": 70.28, 
            "volume": 448787
        }, 
        {
            "market_time": 1512760878, 
            "price": 70.25, 
            "volume": 450003
        }, 
        {
            "market_time": 1512760910, 
            "price": 70.2534, 
            "volume": 450440
        }, 
        {
            "market_time": 1512760916, 
            "price": 70.21, 
            "volume": 451394
        }, 
        {
            "market_time": 1512760930, 
            "price": 70.2, 
            "volume": 452060
        }, 
        {
            "market_time": 1512761275, 
            "price": 70.22, 
            "volume": 462582
        }, 
        {
            "market_time": 1512761335, 
            "price": 70.2, 
            "volume": 463207
        }, 
        {
            "market_time": 1512761358, 
            "price": 70.21, 
            "volume": 463841
        }, 
        {
            "market_time": 1512761389, 
            "price": 70.2, 
            "volume": 463941
        }, 
        {
            "market_time": 1512761435, 
            "price": 70.19, 
            "volume": 464255
        }, 
        {
            "market_time": 1512761539, 
            "price": 70.21, 
            "volume": 464979
        }, 
        {
            "market_time": 1512761563, 
            "price": 70.19, 
            "volume": 465627
        }, 
        {
            "market_time": 1512761577, 
            "price": 70.18, 
            "volume": 467554
        }, 
        {
            "market_time": 1512761642, 
            "price": 70.17, 
            "volume": 467716
        }, 
        {
            "market_time": 1512761677, 
            "price": 70.2, 
            "volume": 469122
        }, 
        {
            "market_time": 1512761696, 
            "price": 70.2, 
            "volume": 469416
        }, 
        {
            "market_time": 1512761705, 
            "price": 70.2, 
            "volume": 470016
        }, 
        {
            "market_time": 1512761725, 
            "price": 70.19, 
            "volume": 471020
        }, 
        {
            "market_time": 1512761768, 
            "price": 70.2, 
            "volume": 471972
        }, 
        {
            "market_time": 1512761838, 
            "price": 70.2, 
            "volume": 473235
        }, 
        {
            "market_time": 1512761856, 
            "price": 70.19, 
            "volume": 473885
        }, 
        {
            "market_time": 1512761879, 
            "price": 70.18, 
            "volume": 474443
        }, 
        {
            "market_time": 1512761887, 
            "price": 70.2001, 
            "volume": 474958
        }, 
        {
            "market_time": 1512761937, 
            "price": 70.2, 
            "volume": 475064
        }, 
        {
            "market_time": 1512761965, 
            "price": 70.21, 
            "volume": 476450
        }, 
        {
            "market_time": 1512761978, 
            "price": 70.21, 
            "volume": 476750
        }, 
        {
            "market_time": 1512762007, 
            "price": 70.23, 
            "volume": 478341
        }, 
        {
            "market_time": 1512762080, 
            "price": 70.27, 
            "volume": 480179
        }, 
        {
            "market_time": 1512762184, 
            "price": 70.29, 
            "volume": 480542
        }, 
        {
            "market_time": 1512762225, 
            "price": 70.27, 
            "volume": 480776
        }, 
        {
            "market_time": 1512762227, 
            "price": 70.29, 
            "volume": 482247
        }, 
        {
            "market_time": 1512762244, 
            "price": 70.265, 
            "volume": 482393
        }, 
        {
            "market_time": 1512762285, 
            "price": 70.25, 
            "volume": 482559
        }, 
        {
            "market_time": 1512762339, 
            "price": 70.2635, 
            "volume": 484359
        }, 
        {
            "market_time": 1512762424, 
            "price": 70.28, 
            "volume": 484725
        }, 
        {
            "market_time": 1512762430, 
            "price": 70.29, 
            "volume": 487964
        }, 
        {
            "market_time": 1512762449, 
            "price": 70.3, 
            "volume": 489054
        }, 
        {
            "market_time": 1512762483, 
            "price": 70.3, 
            "volume": 489182
        }, 
        {
            "market_time": 1512762522, 
            "price": 70.2902, 
            "volume": 489570
        }, 
        {
            "market_time": 1512762945, 
            "price": 70.28, 
            "volume": 496118
        }, 
        {
            "market_time": 1512763174, 
            "price": 70.27, 
            "volume": 500562
        }, 
        {
            "market_time": 1512763247, 
            "price": 70.28, 
            "volume": 500796
        }, 
        {
            "market_time": 1512763286, 
            "price": 70.29, 
            "volume": 500896
        }, 
        {
            "market_time": 1512763313, 
            "price": 70.29, 
            "volume": 501196
        }, 
        {
            "market_time": 1512763368, 
            "price": 70.29, 
            "volume": 501815
        }, 
        {
            "market_time": 1512763395, 
            "price": 70.28, 
            "volume": 502055
        }, 
        {
            "market_time": 1512763436, 
            "price": 70.28, 
            "volume": 503614
        }, 
        {
            "market_time": 1512763445, 
            "price": 70.27, 
            "volume": 503838
        }, 
        {
            "market_time": 1512763574, 
            "price": 70.28, 
            "volume": 506750
        }, 
        {
            "market_time": 1512763608, 
            "price": 70.28, 
            "volume": 510847
        }, 
        {
            "market_time": 1512763620, 
            "price": 70.28, 
            "volume": 511752
        }, 
        {
            "market_time": 1512763750, 
            "price": 70.29, 
            "volume": 514131
        }, 
        {
            "market_time": 1512763782, 
            "price": 70.29, 
            "volume": 515336
        }, 
        {
            "market_time": 1512763814, 
            "price": 70.29, 
            "volume": 516622
        }, 
        {
            "market_time": 1512763881, 
            "price": 70.28, 
            "volume": 518407
        }, 
        {
            "market_time": 1512763893, 
            "price": 70.29, 
            "volume": 518722
        }, 
        {
            "market_time": 1512763977, 
            "price": 70.28, 
            "volume": 522938
        }, 
        {
            "market_time": 1512763990, 
            "price": 70.29, 
            "volume": 526910
        }, 
        {
            "market_time": 1512764051, 
            "price": 70.31, 
            "volume": 529370
        }, 
        {
            "market_time": 1512764071, 
            "price": 70.3, 
            "volume": 529919
        }, 
        {
            "market_time": 1512764087, 
            "price": 70.3, 
            "volume": 530725
        }, 
        {
            "market_time": 1512764157, 
            "price": 70.3, 
            "volume": 531134
        }, 
        {
            "market_time": 1512764165, 
            "price": 70.3, 
            "volume": 533015
        }, 
        {
            "market_time": 1512764183, 
            "price": 70.3, 
            "volume": 533822
        }, 
        {
            "market_time": 1512764227, 
            "price": 70.29, 
            "volume": 534426
        }, 
        {
            "market_time": 1512764230, 
            "price": 70.28, 
            "volume": 534826
        }, 
        {
            "market_time": 1512764249, 
            "price": 70.29, 
            "volume": 534943
        }, 
        {
            "market_time": 1512764255, 
            "price": 70.28, 
            "volume": 535481
        }, 
        {
            "market_time": 1512764292, 
            "price": 70.3, 
            "volume": 535712
        }, 
        {
            "market_time": 1512764323, 
            "price": 70.2985, 
            "volume": 536232
        }, 
        {
            "market_time": 1512764343, 
            "price": 70.29, 
            "volume": 537076
        }, 
        {
            "market_time": 1512764369, 
            "price": 70.3, 
            "volume": 538828
        }, 
        {
            "market_time": 1512764371, 
            "price": 70.3, 
            "volume": 539428
        }, 
        {
            "market_time": 1512764390, 
            "price": 70.3, 
            "volume": 539728
        }, 
        {
            "market_time": 1512764393, 
            "price": 70.3, 
            "volume": 539928
        }, 
        {
            "market_time": 1512764410, 
            "price": 70.31, 
            "volume": 540228
        }, 
        {
            "market_time": 1512764428, 
            "price": 70.31, 
            "volume": 540328
        }, 
        {
            "market_time": 1512764459, 
            "price": 70.3, 
            "volume": 540833
        }, 
        {
            "market_time": 1512764466, 
            "price": 70.3013, 
            "volume": 542559
        }, 
        {
            "market_time": 1512764501, 
            "price": 70.33, 
            "volume": 544359
        }, 
        {
            "market_time": 1512764503, 
            "price": 70.32, 
            "volume": 544555
        }, 
        {
            "market_time": 1512764515, 
            "price": 70.32, 
            "volume": 544704
        }, 
        {
            "market_time": 1512764530, 
            "price": 70.32, 
            "volume": 545780
        }, 
        {
            "market_time": 1512764545, 
            "price": 70.32, 
            "volume": 546071
        }, 
        {
            "market_time": 1512764569, 
            "price": 70.32, 
            "volume": 546975
        }, 
        {
            "market_time": 1512764594, 
            "price": 70.32, 
            "volume": 547162
        }, 
        {
            "market_time": 1512764622, 
            "price": 70.33, 
            "volume": 547262
        }, 
        {
            "market_time": 1512764641, 
            "price": 70.33, 
            "volume": 549167
        }, 
        {
            "market_time": 1512764674, 
            "price": 70.3301, 
            "volume": 549277
        }, 
        {
            "market_time": 1512764687, 
            "price": 70.35, 
            "volume": 550002
        }, 
        {
            "market_time": 1512764695, 
            "price": 70.3445, 
            "volume": 550560
        }, 
        {
            "market_time": 1512764739, 
            "price": 70.33, 
            "volume": 552075
        }, 
        {
            "market_time": 1512764742, 
            "price": 70.33, 
            "volume": 552175
        }, 
        {
            "market_time": 1512764784, 
            "price": 70.32, 
            "volume": 552725
        }, 
        {
            "market_time": 1512764812, 
            "price": 70.34, 
            "volume": 552970
        }, 
        {
            "market_time": 1512764861, 
            "price": 70.33, 
            "volume": 554108
        }, 
        {
            "market_time": 1512764865, 
            "price": 70.32, 
            "volume": 555060
        }, 
        {
            "market_time": 1512764918, 
            "price": 70.33, 
            "volume": 556161
        }, 
        {
            "market_time": 1512764926, 
            "price": 70.34, 
            "volume": 556262
        }, 
        {
            "market_time": 1512764940, 
            "price": 70.34, 
            "volume": 556928
        }, 
        {
            "market_time": 1512764943, 
            "price": 70.33, 
            "volume": 557128
        }, 
        {
            "market_time": 1512764966, 
            "price": 70.325, 
            "volume": 558328
        }, 
        {
            "market_time": 1512764994, 
            "price": 70.32, 
            "volume": 559174
        }, 
        {
            "market_time": 1512765016, 
            "price": 70.33, 
            "volume": 559328
        }, 
        {
            "market_time": 1512765079, 
            "price": 70.34, 
            "volume": 560625
        }, 
        {
            "market_time": 1512765092, 
            "price": 70.33, 
            "volume": 562204
        }, 
        {
            "market_time": 1512765151, 
            "price": 70.31, 
            "volume": 564010
        }, 
        {
            "market_time": 1512765163, 
            "price": 70.31, 
            "volume": 566346
        }, 
        {
            "market_time": 1512765180, 
            "price": 70.31, 
            "volume": 566651
        }, 
        {
            "market_time": 1512765187, 
            "price": 70.31, 
            "volume": 566959
        }, 
        {
            "market_time": 1512765207, 
            "price": 70.32, 
            "volume": 569679
        }, 
        {
            "market_time": 1512765230, 
            "price": 70.31, 
            "volume": 570403
        }, 
        {
            "market_time": 1512765234, 
            "price": 70.31, 
            "volume": 570503
        }, 
        {
            "market_time": 1512765256, 
            "price": 70.31, 
            "volume": 571561
        }, 
        {
            "market_time": 1512765279, 
            "price": 70.28, 
            "volume": 573481
        }, 
        {
            "market_time": 1512765302, 
            "price": 70.28, 
            "volume": 574957
        }, 
        {
            "market_time": 1512765320, 
            "price": 70.27, 
            "volume": 575363
        }, 
        {
            "market_time": 1512765333, 
            "price": 70.28, 
            "volume": 575470
        }, 
        {
            "market_time": 1512765349, 
            "price": 70.28, 
            "volume": 576032
        }, 
        {
            "market_time": 1512765393, 
            "price": 70.285, 
            "volume": 576690
        }, 
        {
            "market_time": 1512765408, 
            "price": 70.28, 
            "volume": 579935
        }, 
        {
            "market_time": 1512765416, 
            "price": 70.29, 
            "volume": 580911
        }, 
        {
            "market_time": 1512765424, 
            "price": 70.29, 
            "volume": 581379
        }, 
        {
            "market_time": 1512765445, 
            "price": 70.29, 
            "volume": 581854
        }, 
        {
            "market_time": 1512765477, 
            "price": 70.29, 
            "volume": 582445
        }, 
        {
            "market_time": 1512765483, 
            "price": 70.2964, 
            "volume": 583239
        }, 
        {
            "market_time": 1512765506, 
            "price": 70.3, 
            "volume": 583798
        }, 
        {
            "market_time": 1512765514, 
            "price": 70.3, 
            "volume": 584606
        }, 
        {
            "market_time": 1512765530, 
            "price": 70.32, 
            "volume": 586581
        }, 
        {
            "market_time": 1512765572, 
            "price": 70.34, 
            "volume": 586683
        }, 
        {
            "market_time": 1512765603, 
            "price": 70.335, 
            "volume": 587649
        }, 
        {
            "market_time": 1512765610, 
            "price": 70.33, 
            "volume": 588781
        }, 
        {
            "market_time": 1512765638, 
            "price": 70.33, 
            "volume": 589818
        }, 
        {
            "market_time": 1512765651, 
            "price": 70.3342, 
            "volume": 590838
        }, 
        {
            "market_time": 1512765690, 
            "price": 70.33, 
            "volume": 591354
        }, 
        {
            "market_time": 1512765721, 
            "price": 70.33, 
            "volume": 591623
        }, 
        {
            "market_time": 1512765738, 
            "price": 70.32, 
            "volume": 592656
        }, 
        {
            "market_time": 1512765748, 
            "price": 70.315, 
            "volume": 595700
        }, 
        {
            "market_time": 1512765772, 
            "price": 70.31, 
            "volume": 595811
        }, 
        {
            "market_time": 1512765798, 
            "price": 70.29, 
            "volume": 597534
        }, 
        {
            "market_time": 1512765808, 
            "price": 70.3, 
            "volume": 597759
        }, 
        {
            "market_time": 1512765820, 
            "price": 70.29, 
            "volume": 598097
        }, 
        {
            "market_time": 1512765839, 
            "price": 70.29, 
            "volume": 602749
        }, 
        {
            "market_time": 1512765843, 
            "price": 70.3, 
            "volume": 604110
        }, 
        {
            "market_time": 1512765875, 
            "price": 70.3, 
            "volume": 605465
        }, 
        {
            "market_time": 1512765916, 
            "price": 70.29, 
            "volume": 609205
        }, 
        {
            "market_time": 1512765935, 
            "price": 70.29, 
            "volume": 609309
        }, 
        {
            "market_time": 1512765950, 
            "price": 70.3, 
            "volume": 609545
        }, 
        {
            "market_time": 1512765952, 
            "price": 70.3001, 
            "volume": 611082
        }, 
        {
            "market_time": 1512765964, 
            "price": 70.32, 
            "volume": 613605
        }, 
        {
            "market_time": 1512766000, 
            "price": 70.31, 
            "volume": 615274
        }, 
        {
            "market_time": 1512766003, 
            "price": 70.31, 
            "volume": 615503
        }, 
        {
            "market_time": 1512766020, 
            "price": 70.3, 
            "volume": 616683
        }, 
        {
            "market_time": 1512766030, 
            "price": 70.315, 
            "volume": 617412
        }, 
        {
            "market_time": 1512766045, 
            "price": 70.32, 
            "volume": 618731
        }, 
        {
            "market_time": 1512766058, 
            "price": 70.32, 
            "volume": 620266
        }, 
        {
            "market_time": 1512766081, 
            "price": 70.32, 
            "volume": 621023
        }, 
        {
            "market_time": 1512766097, 
            "price": 70.32, 
            "volume": 626661
        }, 
        {
            "market_time": 1512766106, 
            "price": 70.32, 
            "volume": 627069
        }, 
        {
            "market_time": 1512766113, 
            "price": 70.29, 
            "volume": 628520
        }, 
        {
            "market_time": 1512766128, 
            "price": 70.29, 
            "volume": 628922
        }, 
        {
            "market_time": 1512766140, 
            "price": 70.29, 
            "volume": 630956
        }, 
        {
            "market_time": 1512766149, 
            "price": 70.3, 
            "volume": 631056
        }, 
        {
            "market_time": 1512766160, 
            "price": 70.31, 
            "volume": 631466
        }, 
        {
            "market_time": 1512766173, 
            "price": 70.315, 
            "volume": 632071
        }, 
        {
            "market_time": 1512766190, 
            "price": 70.3, 
            "volume": 633713
        }, 
        {
            "market_time": 1512766200, 
            "price": 70.3, 
            "volume": 634848
        }, 
        {
            "market_time": 1512766205, 
            "price": 70.37, 
            "volume": 649553
        }, 
        {
            "market_time": 1512766228, 
            "price": 70.38, 
            "volume": 650573
        }, 
        {
            "market_time": 1512766235, 
            "price": 70.39, 
            "volume": 651581
        }, 
        {
            "market_time": 1512766244, 
            "price": 70.4, 
            "volume": 653259
        }, 
        {
            "market_time": 1512766273, 
            "price": 70.4, 
            "volume": 654158
        }, 
        {
            "market_time": 1512766276, 
            "price": 70.41, 
            "volume": 656893
        }, 
        {
            "market_time": 1512766299, 
            "price": 70.42, 
            "volume": 660450
        }, 
        {
            "market_time": 1512766328, 
            "price": 70.415, 
            "volume": 661592
        }, 
        {
            "market_time": 1512766340, 
            "price": 70.42, 
            "volume": 662047
        }, 
        {
            "market_time": 1512766352, 
            "price": 70.42, 
            "volume": 662318
        }, 
        {
            "market_time": 1512766379, 
            "price": 70.42, 
            "volume": 667792
        }, 
        {
            "market_time": 1512766387, 
            "price": 70.425, 
            "volume": 668392
        }, 
        {
            "market_time": 1512766399, 
            "price": 70.42, 
            "volume": 668674
        }, 
        {
            "market_time": 1512766410, 
            "price": 70.43, 
            "volume": 669748
        }, 
        {
            "market_time": 1512766417, 
            "price": 70.42, 
            "volume": 670125
        }, 
        {
            "market_time": 1512766449, 
            "price": 70.4101, 
            "volume": 675719
        }, 
        {
            "market_time": 1512766477, 
            "price": 70.4, 
            "volume": 685696
        }, 
        {
            "market_time": 1512766499, 
            "price": 70.39, 
            "volume": 687496
        }, 
        {
            "market_time": 1512766519, 
            "price": 70.395, 
            "volume": 692643
        }, 
        {
            "market_time": 1512766540, 
            "price": 70.4, 
            "volume": 694808
        }, 
        {
            "market_time": 1512766547, 
            "price": 70.4, 
            "volume": 696289
        }, 
        {
            "market_time": 1512766572, 
            "price": 70.395, 
            "volume": 697892
        }, 
        {
            "market_time": 1512766590, 
            "price": 70.39, 
            "volume": 699013
        }, 
        {
            "market_time": 1512766600, 
            "price": 70.4, 
            "volume": 700409
        }, 
        {
            "market_time": 1512766610, 
            "price": 70.395, 
            "volume": 701009
        }, 
        {
            "market_time": 1512766615, 
            "price": 70.4, 
            "volume": 702710
        }, 
        {
            "market_time": 1512766633, 
            "price": 70.39, 
            "volume": 704165
        }, 
        {
            "market_time": 1512766650, 
            "price": 70.38, 
            "volume": 713863
        }, 
        {
            "market_time": 1512766658, 
            "price": 70.38, 
            "volume": 714202
        }, 
        {
            "market_time": 1512766670, 
            "price": 70.39, 
            "volume": 716116
        }, 
        {
            "market_time": 1512766682, 
            "price": 70.38, 
            "volume": 717059
        }, 
        {
            "market_time": 1512766700, 
            "price": 70.38, 
            "volume": 720148
        }, 
        {
            "market_time": 1512766706, 
            "price": 70.38, 
            "volume": 721537
        }, 
        {
            "market_time": 1512766721, 
            "price": 70.38, 
            "volume": 729417
        }, 
        {
            "market_time": 1512766730, 
            "price": 70.37, 
            "volume": 732926
        }, 
        {
            "market_time": 1512766739, 
            "price": 70.37, 
            "volume": 736228
        }, 
        {
            "market_time": 1512766751, 
            "price": 70.39, 
            "volume": 742849
        }, 
        {
            "market_time": 1512766769, 
            "price": 70.4, 
            "volume": 756601
        }, 
        {
            "market_time": 1512766778, 
            "price": 70.395, 
            "volume": 758580
        }, 
        {
            "market_time": 1512766786, 
            "price": 70.42, 
            "volume": 763064
        }, 
        {
            "market_time": 1512766796, 
            "price": 70.41, 
            "volume": 769612
        }, 
        {
            "market_time": 1512766802, 
            "price": 70.42, 
            "volume": 774703
        }
    ], 
    "end": "2017-12-08 14:30:00", 
    "intercept": -31584.988811717696, 
    "predict_price": 70.50106888181472, 
    "predict_time": "2017-12-08 22:49:49", 
    "start": "2017-12-08 08:30:00"
}
```


GET ALL AVAILABLE SYMBOL
------
<code request-method="GET">**GET** /hourly-predict/available</code>

Get all current available hourly data on the database

### Example
```http
GET http://localhost:6789/hourly-predict/available
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
        "symbol": "ETHUSD=X"
    }, 
    {
        "symbol": "SHW"
    }, 
    {
        "symbol": "C"
    }, 
    {
        "symbol": "XRP-USD"
    }, 
    {
        "symbol": "JPM"
    }, 
    {
        "symbol": "LTC-USD"
    }, 
    {
        "symbol": "DASH-USD"
    }, 
    {
        "symbol": "GBTC"
    }, 
    {
        "symbol": "RACE"
    }, 
    {
        "symbol": "BLL"
    }, 
    {
        "symbol": "FB"
    }, 
    {
        "symbol": "CCC"
    }, 
    {
        "symbol": "BTC-USD"
    }, 
    {
        "symbol": "DWDP"
    }, 
    {
        "symbol": "AMZN"
    }, 
    {
        "symbol": "XLB"
    }, 
    {
        "symbol": "M"
    }, 
    {
        "symbol": "BTCUSD=X"
    }, 
    {
        "symbol": "CC"
    }, 
    {
        "symbol": "MAID-USD"
    }, 
    {
        "symbol": "XMR-USD"
    }, 
    {
        "symbol": "CERN"
    }, 
    {
        "symbol": "WMT"
    }, 
    {
        "symbol": "MSFT"
    }
]
```

