
Auto trade execute status
======

`/execute-status`

When you doing the auto trade, this show the status on your transactions where they are completed or not

### Methods

Method | URL | Description
--- | --- | ---
**[GET](/documentation/endpoint/execute-status#get-execute-status)** | `/execute-status` | GET Execute Status
**[GET](/documentation/endpoint/execute-status#get-execute-status-what-is-completed)** | `/execute-status?completed=True` | GET Execute Status what is completed
**[GET](/documentation/endpoint/execute-status#get-csv-profit-details)** | `/execute-status/profit/details.csv` | GET CSV profit details

### Object Attributes

Attribute | Type | Readonly | Nullable | Has Default
--- | --- | --- | --- | ---
`bought` | numeric | &nbsp; | &nbsp; | &nbsp;
`bought_more` | integer | &nbsp; | &nbsp; | &bullet;
`business_id` | integer | &nbsp; | &nbsp; | &nbsp;
`completed` | timestamp | &nbsp; | &bullet; | &nbsp;
`created` | timestamp | &nbsp; | &nbsp; | &bullet;
`id` | integer | &nbsp; | &nbsp; | &bullet;
`profit` | integer | &nbsp; | &bullet; | &nbsp;
`sold` | numeric | &nbsp; | &bullet; | &nbsp;
`symbol` | text | &nbsp; | &nbsp; | &nbsp;
`total_shares` | integer | &nbsp; | &bullet; | &nbsp;
`type` | text | &nbsp; | &nbsp; | &bullet;

GET Execute Status
------
<code request-method="GET">**GET** /execute-status</code>

Get current executing symbol

### Example
```http
GET http://localhost:6789/execute-status
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
Date: Fri, 02 Feb 2018 14:13:56 GMT
Expires: 0
Server: TwistedWeb/16.6.0
Transfer-Encoding: chunked
Vary: Origin

[
    {
        "bought": 73.91, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": null, 
        "created": "2018-02-01T11:56:02.679575-05:00", 
        "id": 205, 
        "profit": null, 
        "sold": null, 
        "symbol": "CL", 
        "total_shares": 67, 
        "type": "UP"
    }, 
    {
        "bought": 246.59, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": null, 
        "created": "2018-02-01T11:10:58.491032-05:00", 
        "id": 204, 
        "profit": null, 
        "sold": null, 
        "symbol": "BIDU", 
        "total_shares": 20, 
        "type": "DOWN"
    }, 
    {
        "bought": 6.86, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": null, 
        "created": "2018-02-01T11:10:58.471607-05:00", 
        "id": 203, 
        "profit": null, 
        "sold": null, 
        "symbol": "NETE", 
        "total_shares": 728, 
        "type": "UP"
    }, 
    {
        "bought": 7.6001, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": null, 
        "created": "2018-02-01T11:10:58.469001-05:00", 
        "id": 202, 
        "profit": null, 
        "sold": null, 
        "symbol": "KODK", 
        "total_shares": 657, 
        "type": "UP"
    }, 
    {
        "bought": 1.8871, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": null, 
        "created": "2018-02-01T11:10:58.462466-05:00", 
        "id": 201, 
        "profit": null, 
        "sold": null, 
        "symbol": "HVBTF", 
        "total_shares": 2649, 
        "type": "UP"
    }, 
    {
        "bought": 169.19, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": null, 
        "created": "2018-02-01T11:06:48.976934-05:00", 
        "id": 200, 
        "profit": null, 
        "sold": null, 
        "symbol": "WYNN", 
        "total_shares": 29, 
        "type": "UP"
    }, 
    {
        "bought": 34.81, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": null, 
        "created": "2018-02-01T11:03:48.025503-05:00", 
        "id": 199, 
        "profit": null, 
        "sold": null, 
        "symbol": "TRIP", 
        "total_shares": 143, 
        "type": "UP"
    }, 
    {
        "bought": 25.71, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": null, 
        "created": "2018-02-01T11:03:02.005353-05:00", 
        "id": 198, 
        "profit": null, 
        "sold": null, 
        "symbol": "M", 
        "total_shares": 194, 
        "type": "UP"
    }, 
    {
        "bought": 2.2193, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": null, 
        "created": "2018-02-01T11:02:07.618308-05:00", 
        "id": 197, 
        "profit": null, 
        "sold": null, 
        "symbol": "TEUM", 
        "total_shares": 2252, 
        "type": "UP"
    }, 
    {
        "bought": 1171.64, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": null, 
        "created": "2018-02-01T11:02:07.488412-05:00", 
        "id": 196, 
        "profit": null, 
        "sold": null, 
        "symbol": "GOOG", 
        "total_shares": 4, 
        "type": "UP"
    }, 
    {
        "bought": 377.59, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": null, 
        "created": "2018-02-01T11:02:07.435409-05:00", 
        "id": 195, 
        "profit": null, 
        "sold": null, 
        "symbol": "CHTR", 
        "total_shares": 13, 
        "type": "UP"
    }, 
    {
        "bought": 0.32, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": null, 
        "created": "2018-02-01T11:02:07.363835-05:00", 
        "id": 194, 
        "profit": null, 
        "sold": null, 
        "symbol": "MIHI", 
        "total_shares": 15624, 
        "type": "UP"
    }, 
    {
        "bought": 245.9799, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": null, 
        "created": "2018-02-01T11:01:59.215727-05:00", 
        "id": 193, 
        "profit": null, 
        "sold": null, 
        "symbol": "NVDA", 
        "total_shares": 20, 
        "type": "UP"
    }, 
    {
        "bought": 26.11, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": null, 
        "created": "2018-02-01T11:01:59.178059-05:00", 
        "id": 192, 
        "profit": null, 
        "sold": null, 
        "symbol": "TWTR", 
        "total_shares": 191, 
        "type": "UP"
    }, 
    {
        "bought": 32.09, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": null, 
        "created": "2018-02-01T11:01:59.162209-05:00", 
        "id": 191, 
        "profit": null, 
        "sold": null, 
        "symbol": "BAC", 
        "total_shares": 155, 
        "type": "DOWN"
    }, 
    {
        "bought": 263.35, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": null, 
        "created": "2018-02-01T11:01:58.198703-05:00", 
        "id": 190, 
        "profit": null, 
        "sold": null, 
        "symbol": "ORLY", 
        "total_shares": 18, 
        "type": "UP"
    }, 
    {
        "bought": 5.345, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": null, 
        "created": "2018-02-01T11:01:57.874675-05:00", 
        "id": 189, 
        "profit": null, 
        "sold": null, 
        "symbol": "GRPN", 
        "total_shares": 935, 
        "type": "UP"
    }, 
    {
        "bought": 51.605, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": null, 
        "created": "2018-02-01T10:58:51.594385-05:00", 
        "id": 187, 
        "profit": null, 
        "sold": null, 
        "symbol": "CC", 
        "total_shares": 96, 
        "type": "UP"
    }, 
    {
        "bought": 78.29, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": null, 
        "created": "2018-02-01T10:58:51.356264-05:00", 
        "id": 186, 
        "profit": null, 
        "sold": null, 
        "symbol": "C", 
        "total_shares": 63, 
        "type": "UP"
    }, 
    {
        "bought": 50.49, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": null, 
        "created": "2018-01-30T13:56:47.427248-05:00", 
        "id": 146, 
        "profit": null, 
        "sold": null, 
        "symbol": "HOG", 
        "total_shares": 99, 
        "type": "DOWN"
    }, 
    {
        "bought": 34.66, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": null, 
        "created": "2018-01-30T13:45:46.960438-05:00", 
        "id": 121, 
        "profit": null, 
        "sold": null, 
        "symbol": "GOOS", 
        "total_shares": 144, 
        "type": "UP"
    }, 
    {
        "bought": 1430.12, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": null, 
        "created": "2018-01-30T12:27:11.813218-05:00", 
        "id": 113, 
        "profit": null, 
        "sold": null, 
        "symbol": "AMZN", 
        "total_shares": 3, 
        "type": "UP"
    }, 
    {
        "bought": 357.2484, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": null, 
        "created": "2018-01-30T11:28:56.291892-05:00", 
        "id": 112, 
        "profit": null, 
        "sold": null, 
        "symbol": "BIIB", 
        "total_shares": 13, 
        "type": "UP"
    }, 
    {
        "bought": 13.09, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": null, 
        "created": "2018-01-30T10:57:46.956333-05:00", 
        "id": 142, 
        "profit": null, 
        "sold": null, 
        "symbol": "AMD", 
        "total_shares": 381, 
        "type": "UP"
    }, 
    {
        "bought": 67.76, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": null, 
        "created": "2018-01-30T10:43:46.859806-05:00", 
        "id": 180, 
        "profit": null, 
        "sold": null, 
        "symbol": "FSLR", 
        "total_shares": 73, 
        "type": "UP"
    }, 
    {
        "bought": 197.76, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": null, 
        "created": "2018-01-30T10:01:04.085696-05:00", 
        "id": 107, 
        "profit": null, 
        "sold": null, 
        "symbol": "BABA", 
        "total_shares": 25, 
        "type": "DOWN"
    }, 
    {
        "bought": 167.96, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": null, 
        "created": "2018-01-29T16:29:56.520754-05:00", 
        "id": 138, 
        "profit": null, 
        "sold": null, 
        "symbol": "AAPL", 
        "total_shares": 29, 
        "type": "UP"
    }, 
    {
        "bought": 1932.72, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": null, 
        "created": "2018-01-29T14:25:57.096585-05:00", 
        "id": 134, 
        "profit": null, 
        "sold": null, 
        "symbol": "PCLN", 
        "total_shares": 2, 
        "type": "UP"
    }, 
    {
        "bought": 348.01, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": null, 
        "created": "2018-01-29T14:22:46.672963-05:00", 
        "id": 99, 
        "profit": null, 
        "sold": null, 
        "symbol": "TSLA", 
        "total_shares": 14, 
        "type": "UP"
    }, 
    {
        "bought": 50.38, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T13:56:45.642860-05:00", 
        "created": "2018-01-30T13:46:47.895277-05:00", 
        "id": 122, 
        "profit": 10, 
        "sold": 50.49, 
        "symbol": "HOG", 
        "total_shares": 99, 
        "type": "UP"
    }, 
    {
        "bought": 52.61, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T13:45:46.042627-05:00", 
        "created": "2018-01-30T13:40:11.359448-05:00", 
        "id": 120, 
        "profit": 5, 
        "sold": 52.67, 
        "symbol": "CC", 
        "total_shares": 95, 
        "type": "UP"
    }, 
    {
        "bought": 52.535, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T13:36:00.363034-05:00", 
        "created": "2018-01-30T13:30:56.650186-05:00", 
        "id": 183, 
        "profit": 4, 
        "sold": 52.58, 
        "symbol": "CC", 
        "total_shares": 95, 
        "type": "UP"
    }, 
    {
        "bought": 52.6, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T13:26:45.664899-05:00", 
        "created": "2018-01-30T13:21:11.661048-05:00", 
        "id": 176, 
        "profit": -6, 
        "sold": 52.53, 
        "symbol": "CC", 
        "total_shares": 95, 
        "type": "UP"
    }, 
    {
        "bought": 52.57, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T13:17:00.511654-05:00", 
        "created": "2018-01-30T13:11:56.728431-05:00", 
        "id": 166, 
        "profit": 0, 
        "sold": 52.58, 
        "symbol": "CC", 
        "total_shares": 95, 
        "type": "UP"
    }, 
    {
        "bought": 52.6, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T13:07:45.483446-05:00", 
        "created": "2018-01-30T13:02:11.902645-05:00", 
        "id": 158, 
        "profit": -13, 
        "sold": 52.46, 
        "symbol": "CC", 
        "total_shares": 95, 
        "type": "UP"
    }, 
    {
        "bought": 52.5852, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T12:58:00.673974-05:00", 
        "created": "2018-01-30T12:52:56.336367-05:00", 
        "id": 145, 
        "profit": 0, 
        "sold": 52.59, 
        "symbol": "CC", 
        "total_shares": 95, 
        "type": "UP"
    }, 
    {
        "bought": 52.565, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T12:48:45.433713-05:00", 
        "created": "2018-01-30T12:43:11.814062-05:00", 
        "id": 118, 
        "profit": -1, 
        "sold": 52.55, 
        "symbol": "CC", 
        "total_shares": 95, 
        "type": "UP"
    }, 
    {
        "bought": 52.545, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T12:39:00.744353-05:00", 
        "created": "2018-01-30T12:33:56.741891-05:00", 
        "id": 115, 
        "profit": 2, 
        "sold": 52.57, 
        "symbol": "CC", 
        "total_shares": 95, 
        "type": "UP"
    }, 
    {
        "bought": 52.58, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T12:29:45.655935-05:00", 
        "created": "2018-01-30T12:24:11.330661-05:00", 
        "id": 182, 
        "profit": -3, 
        "sold": 52.54, 
        "symbol": "CC", 
        "total_shares": 95, 
        "type": "UP"
    }, 
    {
        "bought": 1428.8308, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T12:23:00.441460-05:00", 
        "created": "2018-01-30T11:58:12.040941-05:00", 
        "id": 165, 
        "profit": 9, 
        "sold": 1431.8835, 
        "symbol": "AMZN", 
        "total_shares": 3, 
        "type": "UP"
    }, 
    {
        "bought": 52.58, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T12:20:00.347894-05:00", 
        "created": "2018-01-30T12:14:56.446953-05:00", 
        "id": 175, 
        "profit": 2, 
        "sold": 52.605, 
        "symbol": "CC", 
        "total_shares": 95, 
        "type": "UP"
    }, 
    {
        "bought": 52.64, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T12:10:45.431096-05:00", 
        "created": "2018-01-30T12:05:11.325441-05:00", 
        "id": 174, 
        "profit": -2, 
        "sold": 52.615, 
        "symbol": "CC", 
        "total_shares": 94, 
        "type": "UP"
    }, 
    {
        "bought": 52.65, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T12:00:46.195411-05:00", 
        "created": "2018-01-30T11:55:11.677582-05:00", 
        "id": 164, 
        "profit": 0, 
        "sold": 52.66, 
        "symbol": "CC", 
        "total_shares": 94, 
        "type": "UP"
    }, 
    {
        "bought": 1427.705, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T11:53:46.148407-05:00", 
        "created": "2018-01-30T11:14:12.323876-05:00", 
        "id": 173, 
        "profit": 9, 
        "sold": 1430.9985, 
        "symbol": "AMZN", 
        "total_shares": 3, 
        "type": "UP"
    }, 
    {
        "bought": 52.745, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T11:51:00.375304-05:00", 
        "created": "2018-01-30T11:45:57.102664-05:00", 
        "id": 157, 
        "profit": -8, 
        "sold": 52.65, 
        "symbol": "CC", 
        "total_shares": 94, 
        "type": "UP"
    }, 
    {
        "bought": 52.63, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T11:41:45.388103-05:00", 
        "created": "2018-01-30T11:36:11.627437-05:00", 
        "id": 144, 
        "profit": 3, 
        "sold": 52.67, 
        "symbol": "CC", 
        "total_shares": 95, 
        "type": "UP"
    }, 
    {
        "bought": 52.62, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T11:32:00.344311-05:00", 
        "created": "2018-01-30T11:26:56.791366-05:00", 
        "id": 181, 
        "profit": -2, 
        "sold": 52.59, 
        "symbol": "CC", 
        "total_shares": 95, 
        "type": "UP"
    }, 
    {
        "bought": 356.85, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T11:24:00.945376-05:00", 
        "created": "2018-01-30T10:48:12.206966-05:00", 
        "id": 111, 
        "profit": 11, 
        "sold": 357.6899, 
        "symbol": "BIIB", 
        "total_shares": 14, 
        "type": "UP"
    }, 
    {
        "bought": 52.59, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T11:22:45.630022-05:00", 
        "created": "2018-01-30T11:17:11.171979-05:00", 
        "id": 172, 
        "profit": -1, 
        "sold": 52.57, 
        "symbol": "CC", 
        "total_shares": 95, 
        "type": "UP"
    }, 
    {
        "bought": 52.61, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T11:12:45.723178-05:00", 
        "created": "2018-01-30T11:07:11.266902-05:00", 
        "id": 163, 
        "profit": -4, 
        "sold": 52.56, 
        "symbol": "CC", 
        "total_shares": 95, 
        "type": "UP"
    }, 
    {
        "bought": 1421.555, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T11:09:46.140003-05:00", 
        "created": "2018-01-30T11:01:11.784045-05:00", 
        "id": 156, 
        "profit": 13, 
        "sold": 1426.165, 
        "symbol": "AMZN", 
        "total_shares": 3, 
        "type": "UP"
    }, 
    {
        "bought": 52.58, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T11:02:45.930930-05:00", 
        "created": "2018-01-30T10:57:11.681582-05:00", 
        "id": 143, 
        "profit": 6, 
        "sold": 52.65, 
        "symbol": "CC", 
        "total_shares": 95, 
        "type": "UP"
    }, 
    {
        "bought": 1413.882, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T10:56:45.731635-05:00", 
        "created": "2018-01-30T10:47:57.247726-05:00", 
        "id": 110, 
        "profit": 13, 
        "sold": 1418.23, 
        "symbol": "AMZN", 
        "total_shares": 3, 
        "type": "UP"
    }, 
    {
        "bought": 52.37, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T10:53:00.449527-05:00", 
        "created": "2018-01-30T10:47:57.060431-05:00", 
        "id": 109, 
        "profit": 4, 
        "sold": 52.42, 
        "symbol": "CC", 
        "total_shares": 95, 
        "type": "UP"
    }, 
    {
        "bought": 1412.04, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T10:43:00.505442-05:00", 
        "created": "2018-01-30T10:16:13.411477-05:00", 
        "id": 155, 
        "profit": 10, 
        "sold": 1415.67, 
        "symbol": "AMZN", 
        "total_shares": 3, 
        "type": "UP"
    }, 
    {
        "bought": 356.21, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T10:42:45.724105-05:00", 
        "created": "2018-01-30T10:35:56.021571-05:00", 
        "id": 171, 
        "profit": 11, 
        "sold": 357.05, 
        "symbol": "BIIB", 
        "total_shares": 14, 
        "type": "UP"
    }, 
    {
        "bought": 52.52, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T10:39:45.588457-05:00", 
        "created": "2018-01-30T10:34:11.448930-05:00", 
        "id": 170, 
        "profit": 0, 
        "sold": 52.52, 
        "symbol": "CC", 
        "total_shares": 95, 
        "type": "UP"
    }, 
    {
        "bought": 355.62, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T10:31:00.857597-05:00", 
        "created": "2018-01-30T10:25:56.582663-05:00", 
        "id": 162, 
        "profit": 16, 
        "sold": 356.8, 
        "symbol": "BIIB", 
        "total_shares": 14, 
        "type": "UP"
    }, 
    {
        "bought": 52.2005, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T10:30:00.405292-05:00", 
        "created": "2018-01-30T10:24:55.871793-05:00", 
        "id": 154, 
        "profit": 12, 
        "sold": 52.33, 
        "symbol": "CC", 
        "total_shares": 95, 
        "type": "UP"
    }, 
    {
        "bought": 354.0, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T10:21:45.615626-05:00", 
        "created": "2018-01-30T10:15:57.325112-05:00", 
        "id": 153, 
        "profit": 10, 
        "sold": 354.73, 
        "symbol": "BIIB", 
        "total_shares": 14, 
        "type": "UP"
    }, 
    {
        "bought": 52.31, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T10:20:00.885616-05:00", 
        "created": "2018-01-30T10:14:56.639658-05:00", 
        "id": 152, 
        "profit": 1, 
        "sold": 52.33, 
        "symbol": "CC", 
        "total_shares": 95, 
        "type": "UP"
    }, 
    {
        "bought": 1406.8489, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T10:11:46.388014-05:00", 
        "created": "2018-01-30T10:04:58.784661-05:00", 
        "id": 141, 
        "profit": 9, 
        "sold": 1409.9705, 
        "symbol": "AMZN", 
        "total_shares": 3, 
        "type": "UP"
    }, 
    {
        "bought": 352.39, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T10:11:00.903426-05:00", 
        "created": "2018-01-30T10:05:58.968399-05:00", 
        "id": 140, 
        "profit": 17, 
        "sold": 353.63, 
        "symbol": "BIIB", 
        "total_shares": 14, 
        "type": "UP"
    }, 
    {
        "bought": 52.3, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T10:10:02.752313-05:00", 
        "created": "2018-01-30T10:04:58.615894-05:00", 
        "id": 139, 
        "profit": -2, 
        "sold": 52.2711, 
        "symbol": "CC", 
        "total_shares": 95, 
        "type": "UP"
    }, 
    {
        "bought": 352.2199, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T10:01:00.504263-05:00", 
        "created": "2018-01-30T09:50:57.003302-05:00", 
        "id": 179, 
        "profit": 10, 
        "sold": 352.975, 
        "symbol": "BIIB", 
        "total_shares": 14, 
        "type": "UP"
    }, 
    {
        "bought": 198.9, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T10:00:48.108927-05:00", 
        "created": "2018-01-30T09:30:06.601707-05:00", 
        "id": 151, 
        "profit": -25, 
        "sold": 197.9, 
        "symbol": "BABA", 
        "total_shares": 25, 
        "type": "UP"
    }, 
    {
        "bought": 1402.75, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T10:00:01.853561-05:00", 
        "created": "2018-01-30T09:35:57.356648-05:00", 
        "id": 169, 
        "profit": 15, 
        "sold": 1408.0, 
        "symbol": "AMZN", 
        "total_shares": 3, 
        "type": "UP"
    }, 
    {
        "bought": 52.75, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T10:00:01.762175-05:00", 
        "created": "2018-01-30T09:30:46.914093-05:00", 
        "id": 161, 
        "profit": -35, 
        "sold": 52.37, 
        "symbol": "CC", 
        "total_shares": 94, 
        "type": "UP"
    }, 
    {
        "bought": 358.48, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T09:46:06.307693-05:00", 
        "created": "2018-01-30T09:30:04.793414-05:00", 
        "id": 150, 
        "profit": 76, 
        "sold": 352.5719, 
        "symbol": "BIIB", 
        "total_shares": 13, 
        "type": "DOWN"
    }, 
    {
        "bought": 1417.68, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T09:30:47.162525-05:00", 
        "created": "2018-01-30T09:30:06.271396-05:00", 
        "id": 149, 
        "profit": 71, 
        "sold": 1394.0001, 
        "symbol": "AMZN", 
        "total_shares": 3, 
        "type": "DOWN"
    }, 
    {
        "bought": 168.96, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-29T16:25:45.582757-05:00", 
        "created": "2018-01-29T16:20:11.478952-05:00", 
        "id": 137, 
        "profit": -29, 
        "sold": 167.96, 
        "symbol": "AAPL", 
        "total_shares": 29, 
        "type": "UP"
    }, 
    {
        "bought": 167.96, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-29T16:16:00.444527-05:00", 
        "created": "2018-01-29T16:10:56.192653-05:00", 
        "id": 106, 
        "profit": 58, 
        "sold": 169.96, 
        "symbol": "AAPL", 
        "total_shares": 29, 
        "type": "UP"
    }, 
    {
        "bought": 167.96, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-29T16:06:45.323305-05:00", 
        "created": "2018-01-29T16:01:11.531854-05:00", 
        "id": 178, 
        "profit": 0, 
        "sold": 167.96, 
        "symbol": "AAPL", 
        "total_shares": 29, 
        "type": "UP"
    }, 
    {
        "bought": 167.96, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-29T16:06:45.323305-05:00", 
        "created": "2018-01-29T16:01:11.531854-05:00", 
        "id": 63, 
        "profit": 0, 
        "sold": 167.96, 
        "symbol": "AAPL", 
        "total_shares": 29, 
        "type": "UP"
    }, 
    {
        "bought": 168.14, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-29T15:57:00.495427-05:00", 
        "created": "2018-01-29T15:51:56.308682-05:00", 
        "id": 168, 
        "profit": 3, 
        "sold": 168.27, 
        "symbol": "AAPL", 
        "total_shares": 29, 
        "type": "UP"
    }, 
    {
        "bought": 168.15, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-29T15:47:45.577596-05:00", 
        "created": "2018-01-29T15:42:11.429427-05:00", 
        "id": 160, 
        "profit": -4, 
        "sold": 168.01, 
        "symbol": "AAPL", 
        "total_shares": 29, 
        "type": "UP"
    }, 
    {
        "bought": 168.16, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-29T15:38:00.494667-05:00", 
        "created": "2018-01-29T15:32:56.562495-05:00", 
        "id": 148, 
        "profit": -5, 
        "sold": 167.9801, 
        "symbol": "AAPL", 
        "total_shares": 29, 
        "type": "UP"
    }, 
    {
        "bought": 168.4, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-29T15:28:45.577458-05:00", 
        "created": "2018-01-29T15:23:11.231230-05:00", 
        "id": 136, 
        "profit": -7, 
        "sold": 168.14, 
        "symbol": "AAPL", 
        "total_shares": 29, 
        "type": "UP"
    }, 
    {
        "bought": 168.3, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-29T15:19:00.470518-05:00", 
        "created": "2018-01-29T15:13:56.468639-05:00", 
        "id": 105, 
        "profit": 6, 
        "sold": 168.519, 
        "symbol": "AAPL", 
        "total_shares": 29, 
        "type": "UP"
    }, 
    {
        "bought": 168.21, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-29T15:09:45.498895-05:00", 
        "created": "2018-01-29T15:04:11.636150-05:00", 
        "id": 177, 
        "profit": 5, 
        "sold": 168.405, 
        "symbol": "AAPL", 
        "total_shares": 29, 
        "type": "UP"
    }, 
    {
        "bought": 168.0, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-29T15:00:00.578571-05:00", 
        "created": "2018-01-29T14:54:56.419456-05:00", 
        "id": 167, 
        "profit": 6, 
        "sold": 168.21, 
        "symbol": "AAPL", 
        "total_shares": 29, 
        "type": "UP"
    }, 
    {
        "bought": 167.97, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-29T14:50:45.551180-05:00", 
        "created": "2018-01-29T14:45:11.468890-05:00", 
        "id": 159, 
        "profit": 4, 
        "sold": 168.11, 
        "symbol": "AAPL", 
        "total_shares": 29, 
        "type": "UP"
    }, 
    {
        "bought": 167.95, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-29T14:41:00.615265-05:00", 
        "created": "2018-01-29T14:35:56.154369-05:00", 
        "id": 147, 
        "profit": -4, 
        "sold": 167.79, 
        "symbol": "AAPL", 
        "total_shares": 29, 
        "type": "UP"
    }, 
    {
        "bought": 168.17, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-29T14:31:01.098335-05:00", 
        "created": "2018-01-29T14:25:56.313848-05:00", 
        "id": 135, 
        "profit": -2, 
        "sold": 168.0852, 
        "symbol": "AAPL", 
        "total_shares": 29, 
        "type": "UP"
    }, 
    {
        "bought": 1397.71, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-29T14:03:46.376476-05:00", 
        "created": "2018-01-26T14:34:56.731418-05:00", 
        "id": 125, 
        "profit": -78, 
        "sold": 1423.7656, 
        "symbol": "AMZN", 
        "total_shares": 3, 
        "type": "DOWN"
    }, 
    {
        "bought": 40.73, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-29T14:03:46.316085-05:00", 
        "created": "2018-01-26T14:30:46.942666-05:00", 
        "id": 133, 
        "profit": -17, 
        "sold": 40.87, 
        "symbol": "SKX", 
        "total_shares": 122, 
        "type": "DOWN"
    }, 
    {
        "bought": 242.13, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-29T14:03:46.165153-05:00", 
        "created": "2018-01-26T14:34:57.062868-05:00", 
        "id": 127, 
        "profit": -103, 
        "sold": 247.32, 
        "symbol": "NVDA", 
        "total_shares": 20, 
        "type": "DOWN"
    }, 
    {
        "bought": 254.90480810286832, 
        "bought_more": 30, 
        "business_id": 1, 
        "completed": "2018-01-29T14:03:46.163043-05:00", 
        "created": "2018-01-26T14:30:46.327345-05:00", 
        "id": 184, 
        "profit": -73, 
        "sold": 255.03, 
        "symbol": "BIDU", 
        "total_shares": 589, 
        "type": "DOWN"
    }, 
    {
        "bought": 32.08, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-29T11:25:02.704483-05:00", 
        "created": "2018-01-26T14:30:46.164594-05:00", 
        "id": 132, 
        "profit": 35, 
        "sold": 32.31, 
        "symbol": "BAC", 
        "total_shares": 155, 
        "type": "UP"
    }, 
    {
        "bought": 275.03, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-29T11:25:02.637985-05:00", 
        "created": "2018-01-26T14:30:46.299519-05:00", 
        "id": 131, 
        "profit": -30, 
        "sold": 273.32, 
        "symbol": "ORLY", 
        "total_shares": 18, 
        "type": "UP"
    }, 
    {
        "bought": 366.44841890193675, 
        "bought_more": 30, 
        "business_id": 1, 
        "completed": "2018-01-29T10:59:48.920356-05:00", 
        "created": "2018-01-26T16:31:56.962123-05:00", 
        "id": 130, 
        "profit": 1503, 
        "sold": 362.7175, 
        "symbol": "BIIB", 
        "total_shares": 403, 
        "type": "DOWN"
    }, 
    {
        "bought": 170.87, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-29T10:32:49.397762-05:00", 
        "created": "2018-01-26T14:30:46.324520-05:00", 
        "id": 129, 
        "profit": -91, 
        "sold": 167.725, 
        "symbol": "AAPL", 
        "total_shares": 29, 
        "type": "UP"
    }, 
    {
        "bought": 203.381, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-29T10:30:01.966158-05:00", 
        "created": "2018-01-26T14:30:46.844361-05:00", 
        "id": 128, 
        "profit": 52, 
        "sold": 205.5765, 
        "symbol": "BABA", 
        "total_shares": 24, 
        "type": "UP"
    }, 
    {
        "bought": 16.035, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-29T10:27:46.242215-05:00", 
        "created": "2018-01-26T14:29:01.479545-05:00", 
        "id": 123, 
        "profit": 51, 
        "sold": 16.2, 
        "symbol": "GE", 
        "total_shares": 311, 
        "type": "UP"
    }, 
    {
        "bought": 53.28159879215937, 
        "bought_more": 30, 
        "business_id": 1, 
        "completed": "2018-01-29T10:17:02.384475-05:00", 
        "created": "2018-01-26T14:29:01.451444-05:00", 
        "id": 114, 
        "profit": 1583, 
        "sold": 53.83, 
        "symbol": "CC", 
        "total_shares": 2887, 
        "type": "UP"
    }, 
    {
        "bought": 7.78, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-29T10:00:03.148653-05:00", 
        "created": "2018-01-26T16:29:45.852041-05:00", 
        "id": 126, 
        "profit": -83, 
        "sold": 7.65, 
        "symbol": "NETE", 
        "total_shares": 642, 
        "type": "UP"
    }, 
    {
        "bought": 2.29, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-29T09:48:48.132516-05:00", 
        "created": "2018-01-26T14:30:45.981656-05:00", 
        "id": 108, 
        "profit": 109, 
        "sold": 2.34, 
        "symbol": "HVBTF", 
        "total_shares": 2183, 
        "type": "UP"
    }, 
    {
        "bought": 79.68, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-29T09:44:48.898852-05:00", 
        "created": "2018-01-26T14:29:01.571905-05:00", 
        "id": 116, 
        "profit": 50, 
        "sold": 80.49, 
        "symbol": "C", 
        "total_shares": 62, 
        "type": "UP"
    }, 
    {
        "bought": 9.475, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-29T09:39:48.783933-05:00", 
        "created": "2018-01-26T14:30:46.728562-05:00", 
        "id": 124, 
        "profit": 164, 
        "sold": 9.788, 
        "symbol": "KODK", 
        "total_shares": 527, 
        "type": "UP"
    }, 
    {
        "bought": 27.15, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-29T09:37:48.916807-05:00", 
        "created": "2018-01-26T14:29:01.570944-05:00", 
        "id": 119, 
        "profit": 31, 
        "sold": 27.32, 
        "symbol": "M", 
        "total_shares": 184, 
        "type": "UP"
    }, 
    {
        "bought": 1169.9175, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-29T09:37:03.570617-05:00", 
        "created": "2018-01-26T14:30:46.599259-05:00", 
        "id": 117, 
        "profit": 20, 
        "sold": 1175.0, 
        "symbol": "GOOG", 
        "total_shares": 4, 
        "type": "UP"
    }, 
    {
        "bought": 367.91, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-26T16:27:45.668015-05:00", 
        "created": "2018-01-26T16:12:11.618914-05:00", 
        "id": 104, 
        "profit": 0, 
        "sold": 367.91, 
        "symbol": "BIIB", 
        "total_shares": 13, 
        "type": "DOWN"
    }, 
    {
        "bought": 367.8, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-26T16:08:00.449147-05:00", 
        "created": "2018-01-26T15:52:56.877384-05:00", 
        "id": 103, 
        "profit": -1, 
        "sold": 367.91, 
        "symbol": "BIIB", 
        "total_shares": 13, 
        "type": "DOWN"
    }, 
    {
        "bought": 368.36, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-26T15:48:45.538403-05:00", 
        "created": "2018-01-26T15:33:11.925442-05:00", 
        "id": 102, 
        "profit": 7, 
        "sold": 367.75, 
        "symbol": "BIIB", 
        "total_shares": 13, 
        "type": "DOWN"
    }, 
    {
        "bought": 369.4712, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-26T15:29:00.612242-05:00", 
        "created": "2018-01-26T15:13:56.473984-05:00", 
        "id": 101, 
        "profit": 23, 
        "sold": 367.7, 
        "symbol": "BIIB", 
        "total_shares": 13, 
        "type": "DOWN"
    }, 
    {
        "bought": 368.74, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-26T15:09:45.576066-05:00", 
        "created": "2018-01-26T14:54:11.869738-05:00", 
        "id": 100, 
        "profit": -11, 
        "sold": 369.62, 
        "symbol": "BIIB", 
        "total_shares": 13, 
        "type": "DOWN"
    }, 
    {
        "bought": 368.13, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-26T14:50:00.560133-05:00", 
        "created": "2018-01-26T14:34:56.228089-05:00", 
        "id": 77, 
        "profit": -11, 
        "sold": 369.03, 
        "symbol": "BIIB", 
        "total_shares": 13, 
        "type": "DOWN"
    }, 
    {
        "bought": 368.09, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-26T14:27:00.386514-05:00", 
        "created": "2018-01-26T14:26:56.859543-05:00", 
        "id": 98, 
        "profit": 0, 
        "sold": 368.09, 
        "symbol": "BIIB", 
        "total_shares": 13, 
        "type": "DOWN"
    }, 
    {
        "bought": 12.875, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-26T14:22:46.964043-05:00", 
        "created": "2018-01-26T12:22:46.426109-05:00", 
        "id": 97, 
        "profit": 5, 
        "sold": 12.86, 
        "symbol": "AMD", 
        "total_shares": 388, 
        "type": "DOWN"
    }, 
    {
        "bought": 274.08, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-26T14:22:46.823018-05:00", 
        "created": "2018-01-26T12:20:01.826055-05:00", 
        "id": 96, 
        "profit": 24, 
        "sold": 275.46, 
        "symbol": "ORLY", 
        "total_shares": 18, 
        "type": "UP"
    }, 
    {
        "bought": 32.08, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-26T14:22:46.710314-05:00", 
        "created": "2018-01-26T12:20:02.501869-05:00", 
        "id": 94, 
        "profit": 7, 
        "sold": 32.13, 
        "symbol": "BAC", 
        "total_shares": 155, 
        "type": "UP"
    }, 
    {
        "bought": 1166.87, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-26T14:22:46.708669-05:00", 
        "created": "2018-01-26T12:20:03.611707-05:00", 
        "id": 95, 
        "profit": 20, 
        "sold": 1171.88, 
        "symbol": "GOOG", 
        "total_shares": 4, 
        "type": "UP"
    }, 
    {
        "bought": 53.18516336760372, 
        "bought_more": 30, 
        "business_id": 1, 
        "completed": "2018-01-26T14:22:46.623093-05:00", 
        "created": "2018-01-26T12:20:02.200852-05:00", 
        "id": 93, 
        "profit": 450, 
        "sold": 53.34, 
        "symbol": "CC", 
        "total_shares": 2912, 
        "type": "UP"
    }, 
    {
        "bought": 79.68, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-26T14:22:46.621134-05:00", 
        "created": "2018-01-26T12:20:03.231753-05:00", 
        "id": 90, 
        "profit": 11, 
        "sold": 79.865, 
        "symbol": "C", 
        "total_shares": 62, 
        "type": "UP"
    }, 
    {
        "bought": 170.77, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-26T14:22:46.620946-05:00", 
        "created": "2018-01-26T12:24:47.066662-05:00", 
        "id": 92, 
        "profit": -13, 
        "sold": 171.2488, 
        "symbol": "AAPL", 
        "total_shares": 29, 
        "type": "DOWN"
    }, 
    {
        "bought": 259.5, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-26T14:22:46.562686-05:00", 
        "created": "2018-01-26T14:10:47.265013-05:00", 
        "id": 89, 
        "profit": -11, 
        "sold": 260.1, 
        "symbol": "BIDU", 
        "total_shares": 19, 
        "type": "DOWN"
    }, 
    {
        "bought": 203.65154809265363, 
        "bought_more": 30, 
        "business_id": 1, 
        "completed": "2018-01-26T14:22:46.556665-05:00", 
        "created": "2018-01-26T12:20:01.999917-05:00", 
        "id": 88, 
        "profit": 207, 
        "sold": 203.93, 
        "symbol": "BABA", 
        "total_shares": 744, 
        "type": "UP"
    }, 
    {
        "bought": 9.655, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-26T14:22:46.547289-05:00", 
        "created": "2018-01-26T12:20:02.100812-05:00", 
        "id": 87, 
        "profit": -43, 
        "sold": 9.5716, 
        "symbol": "KODK", 
        "total_shares": 517, 
        "type": "UP"
    }, 
    {
        "bought": 26.955, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-26T14:22:46.545716-05:00", 
        "created": "2018-01-26T12:20:02.305611-05:00", 
        "id": 86, 
        "profit": 33, 
        "sold": 27.135, 
        "symbol": "M", 
        "total_shares": 185, 
        "type": "UP"
    }, 
    {
        "bought": 40.74, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-26T14:22:46.360839-05:00", 
        "created": "2018-01-26T12:20:01.964961-05:00", 
        "id": 85, 
        "profit": -1, 
        "sold": 40.75, 
        "symbol": "SKX", 
        "total_shares": 122, 
        "type": "DOWN"
    }, 
    {
        "bought": 241.216, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-26T14:22:46.358979-05:00", 
        "created": "2018-01-26T12:27:56.795992-05:00", 
        "id": 84, 
        "profit": -21, 
        "sold": 242.29, 
        "symbol": "NVDA", 
        "total_shares": 20, 
        "type": "DOWN"
    }, 
    {
        "bought": 2.31, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-26T14:22:45.567188-05:00", 
        "created": "2018-01-26T12:20:00.589245-05:00", 
        "id": 83, 
        "profit": -55, 
        "sold": 2.2844, 
        "symbol": "HVBTF", 
        "total_shares": 2164, 
        "type": "UP"
    }, 
    {
        "bought": 368.65, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-26T14:18:01.453259-05:00", 
        "created": "2018-01-26T14:02:56.575330-05:00", 
        "id": 82, 
        "profit": 7, 
        "sold": 368.05, 
        "symbol": "BIIB", 
        "total_shares": 13, 
        "type": "DOWN"
    }, 
    {
        "bought": 368.89, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-26T13:58:45.337950-05:00", 
        "created": "2018-01-26T13:43:11.362424-05:00", 
        "id": 81, 
        "profit": 6, 
        "sold": 368.425, 
        "symbol": "BIIB", 
        "total_shares": 13, 
        "type": "DOWN"
    }, 
    {
        "bought": 369.87, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-26T13:38:45.811051-05:00", 
        "created": "2018-01-26T13:23:11.762170-05:00", 
        "id": 80, 
        "profit": 6, 
        "sold": 369.38, 
        "symbol": "BIIB", 
        "total_shares": 13, 
        "type": "DOWN"
    }, 
    {
        "bought": 369.15, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-26T13:19:00.468934-05:00", 
        "created": "2018-01-26T13:03:56.897093-05:00", 
        "id": 79, 
        "profit": -9, 
        "sold": 369.87, 
        "symbol": "BIIB", 
        "total_shares": 13, 
        "type": "DOWN"
    }, 
    {
        "bought": 368.9, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-26T12:59:45.663992-05:00", 
        "created": "2018-01-26T12:44:11.880302-05:00", 
        "id": 78, 
        "profit": -14, 
        "sold": 370.04, 
        "symbol": "BIIB", 
        "total_shares": 13, 
        "type": "DOWN"
    }, 
    {
        "bought": 369.25, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-26T12:39:45.963507-05:00", 
        "created": "2018-01-26T12:24:12.018528-05:00", 
        "id": 91, 
        "profit": 4, 
        "sold": 368.93, 
        "symbol": "BIIB", 
        "total_shares": 13, 
        "type": "DOWN"
    }, 
    {
        "bought": 12.865, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-26T12:21:46.869848-05:00", 
        "created": "2018-01-26T12:20:02.113178-05:00", 
        "id": 76, 
        "profit": 5, 
        "sold": 12.88, 
        "symbol": "AMD", 
        "total_shares": 388, 
        "type": "UP"
    }, 
    {
        "bought": 170.75, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-26T12:20:46.816094-05:00", 
        "created": "2018-01-26T12:20:02.383154-05:00", 
        "id": 75, 
        "profit": 0, 
        "sold": 170.775, 
        "symbol": "AAPL", 
        "total_shares": 29, 
        "type": "DOWN"
    }
]
```


GET Execute Status what is completed
------
<code request-method="GET">**GET** /execute-status?completed=True</code>

Get all executed transactions symbol

### Example
```http
GET http://localhost:6789/execute-status?completed=True
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
Date: Fri, 02 Feb 2018 14:13:56 GMT
Expires: 0
Server: TwistedWeb/16.6.0
Transfer-Encoding: chunked
Vary: Origin

[
    {
        "bought": 168.96, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-29T16:25:45.582757-05:00", 
        "created": "2018-01-29T16:20:11.478952-05:00", 
        "id": 137, 
        "profit": -29, 
        "sold": 167.96, 
        "symbol": "AAPL", 
        "total_shares": 29, 
        "type": "UP"
    }, 
    {
        "bought": 168.96, 
        "bought_more": 0, 
        "business_id": 7, 
        "completed": "2018-01-29T16:25:45.582757-05:00", 
        "created": "2018-01-29T16:20:11.478952-05:00", 
        "id": 52, 
        "profit": -29, 
        "sold": 167.96, 
        "symbol": "AAPL", 
        "total_shares": 29, 
        "type": "UP"
    }, 
    {
        "bought": 167.96, 
        "bought_more": 0, 
        "business_id": 7, 
        "completed": "2018-01-29T16:16:00.444527-05:00", 
        "created": "2018-01-29T16:10:56.192653-05:00", 
        "id": 32, 
        "profit": 0, 
        "sold": 167.96, 
        "symbol": "AAPL", 
        "total_shares": 29, 
        "type": "UP"
    }, 
    {
        "bought": 167.96, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-29T16:16:00.444527-05:00", 
        "created": "2018-01-29T16:10:56.192653-05:00", 
        "id": 106, 
        "profit": 58, 
        "sold": 169.96, 
        "symbol": "AAPL", 
        "total_shares": 29, 
        "type": "UP"
    }, 
    {
        "bought": 167.96, 
        "bought_more": 0, 
        "business_id": 7, 
        "completed": "2018-01-29T16:06:45.323305-05:00", 
        "created": "2018-01-29T16:01:11.531854-05:00", 
        "id": 61, 
        "profit": 0, 
        "sold": 167.96, 
        "symbol": "AAPL", 
        "total_shares": 29, 
        "type": "UP"
    }, 
    {
        "bought": 167.96, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-29T16:06:45.323305-05:00", 
        "created": "2018-01-29T16:01:11.531854-05:00", 
        "id": 178, 
        "profit": 0, 
        "sold": 167.96, 
        "symbol": "AAPL", 
        "total_shares": 29, 
        "type": "UP"
    }, 
    {
        "bought": 167.96, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-29T16:06:45.323305-05:00", 
        "created": "2018-01-29T16:01:11.531854-05:00", 
        "id": 63, 
        "profit": 0, 
        "sold": 167.96, 
        "symbol": "AAPL", 
        "total_shares": 29, 
        "type": "UP"
    }, 
    {
        "bought": 168.14, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-29T15:57:00.495427-05:00", 
        "created": "2018-01-29T15:51:56.308682-05:00", 
        "id": 168, 
        "profit": 3, 
        "sold": 168.27, 
        "symbol": "AAPL", 
        "total_shares": 29, 
        "type": "UP"
    }, 
    {
        "bought": 168.14, 
        "bought_more": 0, 
        "business_id": 7, 
        "completed": "2018-01-29T15:57:00.495427-05:00", 
        "created": "2018-01-29T15:51:56.308682-05:00", 
        "id": 59, 
        "profit": 3, 
        "sold": 168.27, 
        "symbol": "AAPL", 
        "total_shares": 29, 
        "type": "UP"
    }, 
    {
        "bought": 168.15, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-29T15:47:45.577596-05:00", 
        "created": "2018-01-29T15:42:11.429427-05:00", 
        "id": 160, 
        "profit": -4, 
        "sold": 168.01, 
        "symbol": "AAPL", 
        "total_shares": 29, 
        "type": "UP"
    }, 
    {
        "bought": 168.15, 
        "bought_more": 0, 
        "business_id": 7, 
        "completed": "2018-01-29T15:47:45.577596-05:00", 
        "created": "2018-01-29T15:42:11.429427-05:00", 
        "id": 57, 
        "profit": -4, 
        "sold": 168.01, 
        "symbol": "AAPL", 
        "total_shares": 29, 
        "type": "UP"
    }, 
    {
        "bought": 168.16, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-29T15:38:00.494667-05:00", 
        "created": "2018-01-29T15:32:56.562495-05:00", 
        "id": 148, 
        "profit": -5, 
        "sold": 167.9801, 
        "symbol": "AAPL", 
        "total_shares": 29, 
        "type": "UP"
    }, 
    {
        "bought": 168.16, 
        "bought_more": 0, 
        "business_id": 7, 
        "completed": "2018-01-29T15:38:00.494667-05:00", 
        "created": "2018-01-29T15:32:56.562495-05:00", 
        "id": 55, 
        "profit": -5, 
        "sold": 167.9801, 
        "symbol": "AAPL", 
        "total_shares": 29, 
        "type": "UP"
    }, 
    {
        "bought": 168.4, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-29T15:28:45.577458-05:00", 
        "created": "2018-01-29T15:23:11.231230-05:00", 
        "id": 136, 
        "profit": -7, 
        "sold": 168.14, 
        "symbol": "AAPL", 
        "total_shares": 29, 
        "type": "UP"
    }, 
    {
        "bought": 168.4, 
        "bought_more": 0, 
        "business_id": 7, 
        "completed": "2018-01-29T15:28:45.577458-05:00", 
        "created": "2018-01-29T15:23:11.231230-05:00", 
        "id": 51, 
        "profit": -7, 
        "sold": 168.14, 
        "symbol": "AAPL", 
        "total_shares": 29, 
        "type": "UP"
    }, 
    {
        "bought": 168.3, 
        "bought_more": 0, 
        "business_id": 7, 
        "completed": "2018-01-29T15:19:00.470518-05:00", 
        "created": "2018-01-29T15:13:56.468639-05:00", 
        "id": 31, 
        "profit": 6, 
        "sold": 168.519, 
        "symbol": "AAPL", 
        "total_shares": 29, 
        "type": "UP"
    }, 
    {
        "bought": 168.3, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-29T15:19:00.470518-05:00", 
        "created": "2018-01-29T15:13:56.468639-05:00", 
        "id": 105, 
        "profit": 6, 
        "sold": 168.519, 
        "symbol": "AAPL", 
        "total_shares": 29, 
        "type": "UP"
    }, 
    {
        "bought": 168.21, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-29T15:09:45.498895-05:00", 
        "created": "2018-01-29T15:04:11.636150-05:00", 
        "id": 177, 
        "profit": 5, 
        "sold": 168.405, 
        "symbol": "AAPL", 
        "total_shares": 29, 
        "type": "UP"
    }, 
    {
        "bought": 168.21, 
        "bought_more": 0, 
        "business_id": 7, 
        "completed": "2018-01-29T15:09:45.498895-05:00", 
        "created": "2018-01-29T15:04:11.636150-05:00", 
        "id": 60, 
        "profit": 5, 
        "sold": 168.405, 
        "symbol": "AAPL", 
        "total_shares": 29, 
        "type": "UP"
    }, 
    {
        "bought": 168.0, 
        "bought_more": 0, 
        "business_id": 7, 
        "completed": "2018-01-29T15:00:00.578571-05:00", 
        "created": "2018-01-29T14:54:56.419456-05:00", 
        "id": 58, 
        "profit": 6, 
        "sold": 168.21, 
        "symbol": "AAPL", 
        "total_shares": 29, 
        "type": "UP"
    }, 
    {
        "bought": 168.0, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-29T15:00:00.578571-05:00", 
        "created": "2018-01-29T14:54:56.419456-05:00", 
        "id": 167, 
        "profit": 6, 
        "sold": 168.21, 
        "symbol": "AAPL", 
        "total_shares": 29, 
        "type": "UP"
    }, 
    {
        "bought": 167.97, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-29T14:50:45.551180-05:00", 
        "created": "2018-01-29T14:45:11.468890-05:00", 
        "id": 159, 
        "profit": 4, 
        "sold": 168.11, 
        "symbol": "AAPL", 
        "total_shares": 29, 
        "type": "UP"
    }, 
    {
        "bought": 167.97, 
        "bought_more": 0, 
        "business_id": 7, 
        "completed": "2018-01-29T14:50:45.551180-05:00", 
        "created": "2018-01-29T14:45:11.468890-05:00", 
        "id": 56, 
        "profit": 4, 
        "sold": 168.11, 
        "symbol": "AAPL", 
        "total_shares": 29, 
        "type": "UP"
    }, 
    {
        "bought": 167.95, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-29T14:41:00.615265-05:00", 
        "created": "2018-01-29T14:35:56.154369-05:00", 
        "id": 147, 
        "profit": -4, 
        "sold": 167.79, 
        "symbol": "AAPL", 
        "total_shares": 29, 
        "type": "UP"
    }, 
    {
        "bought": 167.95, 
        "bought_more": 0, 
        "business_id": 7, 
        "completed": "2018-01-29T14:41:00.615265-05:00", 
        "created": "2018-01-29T14:35:56.154369-05:00", 
        "id": 54, 
        "profit": -4, 
        "sold": 167.79, 
        "symbol": "AAPL", 
        "total_shares": 29, 
        "type": "UP"
    }, 
    {
        "bought": 168.17, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-29T14:31:01.098335-05:00", 
        "created": "2018-01-29T14:25:56.313848-05:00", 
        "id": 135, 
        "profit": -2, 
        "sold": 168.0852, 
        "symbol": "AAPL", 
        "total_shares": 29, 
        "type": "UP"
    }, 
    {
        "bought": 168.17, 
        "bought_more": 0, 
        "business_id": 7, 
        "completed": "2018-01-29T14:31:01.098335-05:00", 
        "created": "2018-01-29T14:25:56.313848-05:00", 
        "id": 50, 
        "profit": -2, 
        "sold": 168.0852, 
        "symbol": "AAPL", 
        "total_shares": 29, 
        "type": "UP"
    }, 
    {
        "bought": 170.87, 
        "bought_more": 0, 
        "business_id": 7, 
        "completed": "2018-01-29T10:32:49.397762-05:00", 
        "created": "2018-01-26T14:30:46.324520-05:00", 
        "id": 44, 
        "profit": -91, 
        "sold": 167.725, 
        "symbol": "AAPL", 
        "total_shares": 29, 
        "type": "UP"
    }, 
    {
        "bought": 170.87, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-29T10:32:49.397762-05:00", 
        "created": "2018-01-26T14:30:46.324520-05:00", 
        "id": 129, 
        "profit": -91, 
        "sold": 167.725, 
        "symbol": "AAPL", 
        "total_shares": 29, 
        "type": "UP"
    }, 
    {
        "bought": 170.77, 
        "bought_more": 0, 
        "business_id": 7, 
        "completed": "2018-01-26T14:22:46.620946-05:00", 
        "created": "2018-01-26T12:24:47.066662-05:00", 
        "id": 18, 
        "profit": -13, 
        "sold": 171.2488, 
        "symbol": "AAPL", 
        "total_shares": 29, 
        "type": "DOWN"
    }, 
    {
        "bought": 170.77, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-26T14:22:46.620946-05:00", 
        "created": "2018-01-26T12:24:47.066662-05:00", 
        "id": 92, 
        "profit": -13, 
        "sold": 171.2488, 
        "symbol": "AAPL", 
        "total_shares": 29, 
        "type": "DOWN"
    }, 
    {
        "bought": 170.75, 
        "bought_more": 0, 
        "business_id": 7, 
        "completed": "2018-01-26T12:20:46.816094-05:00", 
        "created": "2018-01-26T12:20:02.383154-05:00", 
        "id": 1, 
        "profit": 0, 
        "sold": 170.775, 
        "symbol": "AAPL", 
        "total_shares": 29, 
        "type": "DOWN"
    }, 
    {
        "bought": 170.75, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-26T12:20:46.816094-05:00", 
        "created": "2018-01-26T12:20:02.383154-05:00", 
        "id": 75, 
        "profit": 0, 
        "sold": 170.775, 
        "symbol": "AAPL", 
        "total_shares": 29, 
        "type": "DOWN"
    }, 
    {
        "bought": 12.875, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-26T14:22:46.964043-05:00", 
        "created": "2018-01-26T12:22:46.426109-05:00", 
        "id": 97, 
        "profit": 5, 
        "sold": 12.86, 
        "symbol": "AMD", 
        "total_shares": 388, 
        "type": "DOWN"
    }, 
    {
        "bought": 12.875, 
        "bought_more": 0, 
        "business_id": 7, 
        "completed": "2018-01-26T14:22:46.964043-05:00", 
        "created": "2018-01-26T12:22:46.426109-05:00", 
        "id": 23, 
        "profit": 5, 
        "sold": 12.86, 
        "symbol": "AMD", 
        "total_shares": 388, 
        "type": "DOWN"
    }, 
    {
        "bought": 12.865, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-26T12:21:46.869848-05:00", 
        "created": "2018-01-26T12:20:02.113178-05:00", 
        "id": 76, 
        "profit": 5, 
        "sold": 12.88, 
        "symbol": "AMD", 
        "total_shares": 388, 
        "type": "UP"
    }, 
    {
        "bought": 12.865, 
        "bought_more": 0, 
        "business_id": 7, 
        "completed": "2018-01-26T12:21:46.869848-05:00", 
        "created": "2018-01-26T12:20:02.113178-05:00", 
        "id": 2, 
        "profit": 5, 
        "sold": 12.88, 
        "symbol": "AMD", 
        "total_shares": 388, 
        "type": "UP"
    }, 
    {
        "bought": 1428.8308, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T12:23:00.441460-05:00", 
        "created": "2018-01-30T11:58:12.040941-05:00", 
        "id": 165, 
        "profit": 9, 
        "sold": 1431.8835, 
        "symbol": "AMZN", 
        "total_shares": 3, 
        "type": "UP"
    }, 
    {
        "bought": 1427.705, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T11:53:46.148407-05:00", 
        "created": "2018-01-30T11:14:12.323876-05:00", 
        "id": 173, 
        "profit": 9, 
        "sold": 1430.9985, 
        "symbol": "AMZN", 
        "total_shares": 3, 
        "type": "UP"
    }, 
    {
        "bought": 1421.555, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T11:09:46.140003-05:00", 
        "created": "2018-01-30T11:01:11.784045-05:00", 
        "id": 156, 
        "profit": 13, 
        "sold": 1426.165, 
        "symbol": "AMZN", 
        "total_shares": 3, 
        "type": "UP"
    }, 
    {
        "bought": 1413.882, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T10:56:45.731635-05:00", 
        "created": "2018-01-30T10:47:57.247726-05:00", 
        "id": 110, 
        "profit": 13, 
        "sold": 1418.23, 
        "symbol": "AMZN", 
        "total_shares": 3, 
        "type": "UP"
    }, 
    {
        "bought": 1412.04, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T10:43:00.505442-05:00", 
        "created": "2018-01-30T10:16:13.411477-05:00", 
        "id": 155, 
        "profit": 10, 
        "sold": 1415.67, 
        "symbol": "AMZN", 
        "total_shares": 3, 
        "type": "UP"
    }, 
    {
        "bought": 1406.8489, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T10:11:46.388014-05:00", 
        "created": "2018-01-30T10:04:58.784661-05:00", 
        "id": 141, 
        "profit": 9, 
        "sold": 1409.9705, 
        "symbol": "AMZN", 
        "total_shares": 3, 
        "type": "UP"
    }, 
    {
        "bought": 1402.75, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T10:00:01.853561-05:00", 
        "created": "2018-01-30T09:35:57.356648-05:00", 
        "id": 169, 
        "profit": 15, 
        "sold": 1408.0, 
        "symbol": "AMZN", 
        "total_shares": 3, 
        "type": "UP"
    }, 
    {
        "bought": 1417.68, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T09:30:47.162525-05:00", 
        "created": "2018-01-30T09:30:06.271396-05:00", 
        "id": 149, 
        "profit": 71, 
        "sold": 1394.0001, 
        "symbol": "AMZN", 
        "total_shares": 3, 
        "type": "DOWN"
    }, 
    {
        "bought": 1397.71, 
        "bought_more": 0, 
        "business_id": 7, 
        "completed": "2018-01-29T14:03:46.376476-05:00", 
        "created": "2018-01-26T14:34:56.731418-05:00", 
        "id": 40, 
        "profit": -78, 
        "sold": 1423.7656, 
        "symbol": "AMZN", 
        "total_shares": 3, 
        "type": "DOWN"
    }, 
    {
        "bought": 1397.71, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-29T14:03:46.376476-05:00", 
        "created": "2018-01-26T14:34:56.731418-05:00", 
        "id": 125, 
        "profit": -78, 
        "sold": 1423.7656, 
        "symbol": "AMZN", 
        "total_shares": 3, 
        "type": "DOWN"
    }, 
    {
        "bought": 198.9, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T10:00:48.108927-05:00", 
        "created": "2018-01-30T09:30:06.601707-05:00", 
        "id": 151, 
        "profit": -25, 
        "sold": 197.9, 
        "symbol": "BABA", 
        "total_shares": 25, 
        "type": "UP"
    }, 
    {
        "bought": 203.381, 
        "bought_more": 0, 
        "business_id": 7, 
        "completed": "2018-01-29T10:30:01.966158-05:00", 
        "created": "2018-01-26T14:30:46.844361-05:00", 
        "id": 43, 
        "profit": 52, 
        "sold": 205.5765, 
        "symbol": "BABA", 
        "total_shares": 24, 
        "type": "UP"
    }, 
    {
        "bought": 203.381, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-29T10:30:01.966158-05:00", 
        "created": "2018-01-26T14:30:46.844361-05:00", 
        "id": 128, 
        "profit": 52, 
        "sold": 205.5765, 
        "symbol": "BABA", 
        "total_shares": 24, 
        "type": "UP"
    }, 
    {
        "bought": 203.65154809265363, 
        "bought_more": 30, 
        "business_id": 1, 
        "completed": "2018-01-26T14:22:46.556665-05:00", 
        "created": "2018-01-26T12:20:01.999917-05:00", 
        "id": 88, 
        "profit": 207, 
        "sold": 203.93, 
        "symbol": "BABA", 
        "total_shares": 744, 
        "type": "UP"
    }, 
    {
        "bought": 203.65154809265363, 
        "bought_more": 30, 
        "business_id": 7, 
        "completed": "2018-01-26T14:22:46.556665-05:00", 
        "created": "2018-01-26T12:20:01.999917-05:00", 
        "id": 14, 
        "profit": 207, 
        "sold": 203.93, 
        "symbol": "BABA", 
        "total_shares": 744, 
        "type": "UP"
    }, 
    {
        "bought": 32.08, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-29T11:25:02.704483-05:00", 
        "created": "2018-01-26T14:30:46.164594-05:00", 
        "id": 132, 
        "profit": 35, 
        "sold": 32.31, 
        "symbol": "BAC", 
        "total_shares": 155, 
        "type": "UP"
    }, 
    {
        "bought": 32.08, 
        "bought_more": 0, 
        "business_id": 7, 
        "completed": "2018-01-29T11:25:02.704483-05:00", 
        "created": "2018-01-26T14:30:46.164594-05:00", 
        "id": 47, 
        "profit": 35, 
        "sold": 32.31, 
        "symbol": "BAC", 
        "total_shares": 155, 
        "type": "UP"
    }, 
    {
        "bought": 32.08, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-26T14:22:46.710314-05:00", 
        "created": "2018-01-26T12:20:02.501869-05:00", 
        "id": 94, 
        "profit": 7, 
        "sold": 32.13, 
        "symbol": "BAC", 
        "total_shares": 155, 
        "type": "UP"
    }, 
    {
        "bought": 32.08, 
        "bought_more": 0, 
        "business_id": 7, 
        "completed": "2018-01-26T14:22:46.710314-05:00", 
        "created": "2018-01-26T12:20:02.501869-05:00", 
        "id": 20, 
        "profit": 7, 
        "sold": 32.13, 
        "symbol": "BAC", 
        "total_shares": 155, 
        "type": "UP"
    }, 
    {
        "bought": 254.90480810286832, 
        "bought_more": 30, 
        "business_id": 1, 
        "completed": "2018-01-29T14:03:46.163043-05:00", 
        "created": "2018-01-26T14:30:46.327345-05:00", 
        "id": 184, 
        "profit": -73, 
        "sold": 255.03, 
        "symbol": "BIDU", 
        "total_shares": 589, 
        "type": "DOWN"
    }, 
    {
        "bought": 254.90480810286832, 
        "bought_more": 30, 
        "business_id": 7, 
        "completed": "2018-01-29T14:03:46.163043-05:00", 
        "created": "2018-01-26T14:30:46.327345-05:00", 
        "id": 62, 
        "profit": -73, 
        "sold": 255.03, 
        "symbol": "BIDU", 
        "total_shares": 589, 
        "type": "DOWN"
    }, 
    {
        "bought": 259.5, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-26T14:22:46.562686-05:00", 
        "created": "2018-01-26T14:10:47.265013-05:00", 
        "id": 89, 
        "profit": -11, 
        "sold": 260.1, 
        "symbol": "BIDU", 
        "total_shares": 19, 
        "type": "DOWN"
    }, 
    {
        "bought": 356.85, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T11:24:00.945376-05:00", 
        "created": "2018-01-30T10:48:12.206966-05:00", 
        "id": 111, 
        "profit": 11, 
        "sold": 357.6899, 
        "symbol": "BIIB", 
        "total_shares": 14, 
        "type": "UP"
    }, 
    {
        "bought": 356.21, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T10:42:45.724105-05:00", 
        "created": "2018-01-30T10:35:56.021571-05:00", 
        "id": 171, 
        "profit": 11, 
        "sold": 357.05, 
        "symbol": "BIIB", 
        "total_shares": 14, 
        "type": "UP"
    }, 
    {
        "bought": 355.62, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T10:31:00.857597-05:00", 
        "created": "2018-01-30T10:25:56.582663-05:00", 
        "id": 162, 
        "profit": 16, 
        "sold": 356.8, 
        "symbol": "BIIB", 
        "total_shares": 14, 
        "type": "UP"
    }, 
    {
        "bought": 354.0, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T10:21:45.615626-05:00", 
        "created": "2018-01-30T10:15:57.325112-05:00", 
        "id": 153, 
        "profit": 10, 
        "sold": 354.73, 
        "symbol": "BIIB", 
        "total_shares": 14, 
        "type": "UP"
    }, 
    {
        "bought": 352.39, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T10:11:00.903426-05:00", 
        "created": "2018-01-30T10:05:58.968399-05:00", 
        "id": 140, 
        "profit": 17, 
        "sold": 353.63, 
        "symbol": "BIIB", 
        "total_shares": 14, 
        "type": "UP"
    }, 
    {
        "bought": 352.2199, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T10:01:00.504263-05:00", 
        "created": "2018-01-30T09:50:57.003302-05:00", 
        "id": 179, 
        "profit": 10, 
        "sold": 352.975, 
        "symbol": "BIIB", 
        "total_shares": 14, 
        "type": "UP"
    }, 
    {
        "bought": 358.48, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T09:46:06.307693-05:00", 
        "created": "2018-01-30T09:30:04.793414-05:00", 
        "id": 150, 
        "profit": 76, 
        "sold": 352.5719, 
        "symbol": "BIIB", 
        "total_shares": 13, 
        "type": "DOWN"
    }, 
    {
        "bought": 366.44841890193675, 
        "bought_more": 30, 
        "business_id": 7, 
        "completed": "2018-01-29T10:59:48.920356-05:00", 
        "created": "2018-01-26T16:31:56.962123-05:00", 
        "id": 45, 
        "profit": 1503, 
        "sold": 362.7175, 
        "symbol": "BIIB", 
        "total_shares": 403, 
        "type": "DOWN"
    }, 
    {
        "bought": 366.44841890193675, 
        "bought_more": 30, 
        "business_id": 1, 
        "completed": "2018-01-29T10:59:48.920356-05:00", 
        "created": "2018-01-26T16:31:56.962123-05:00", 
        "id": 130, 
        "profit": 1503, 
        "sold": 362.7175, 
        "symbol": "BIIB", 
        "total_shares": 403, 
        "type": "DOWN"
    }, 
    {
        "bought": 367.91, 
        "bought_more": 0, 
        "business_id": 7, 
        "completed": "2018-01-26T16:27:45.668015-05:00", 
        "created": "2018-01-26T16:12:11.618914-05:00", 
        "id": 30, 
        "profit": 0, 
        "sold": 367.91, 
        "symbol": "BIIB", 
        "total_shares": 13, 
        "type": "DOWN"
    }, 
    {
        "bought": 367.91, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-26T16:27:45.668015-05:00", 
        "created": "2018-01-26T16:12:11.618914-05:00", 
        "id": 104, 
        "profit": 0, 
        "sold": 367.91, 
        "symbol": "BIIB", 
        "total_shares": 13, 
        "type": "DOWN"
    }, 
    {
        "bought": 367.8, 
        "bought_more": 0, 
        "business_id": 7, 
        "completed": "2018-01-26T16:08:00.449147-05:00", 
        "created": "2018-01-26T15:52:56.877384-05:00", 
        "id": 29, 
        "profit": -1, 
        "sold": 367.91, 
        "symbol": "BIIB", 
        "total_shares": 13, 
        "type": "DOWN"
    }, 
    {
        "bought": 367.8, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-26T16:08:00.449147-05:00", 
        "created": "2018-01-26T15:52:56.877384-05:00", 
        "id": 103, 
        "profit": -1, 
        "sold": 367.91, 
        "symbol": "BIIB", 
        "total_shares": 13, 
        "type": "DOWN"
    }, 
    {
        "bought": 368.36, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-26T15:48:45.538403-05:00", 
        "created": "2018-01-26T15:33:11.925442-05:00", 
        "id": 102, 
        "profit": 7, 
        "sold": 367.75, 
        "symbol": "BIIB", 
        "total_shares": 13, 
        "type": "DOWN"
    }, 
    {
        "bought": 368.36, 
        "bought_more": 0, 
        "business_id": 7, 
        "completed": "2018-01-26T15:48:45.538403-05:00", 
        "created": "2018-01-26T15:33:11.925442-05:00", 
        "id": 28, 
        "profit": 7, 
        "sold": 367.75, 
        "symbol": "BIIB", 
        "total_shares": 13, 
        "type": "DOWN"
    }, 
    {
        "bought": 369.4712, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-26T15:29:00.612242-05:00", 
        "created": "2018-01-26T15:13:56.473984-05:00", 
        "id": 101, 
        "profit": 23, 
        "sold": 367.7, 
        "symbol": "BIIB", 
        "total_shares": 13, 
        "type": "DOWN"
    }, 
    {
        "bought": 369.4712, 
        "bought_more": 0, 
        "business_id": 7, 
        "completed": "2018-01-26T15:29:00.612242-05:00", 
        "created": "2018-01-26T15:13:56.473984-05:00", 
        "id": 27, 
        "profit": 23, 
        "sold": 367.7, 
        "symbol": "BIIB", 
        "total_shares": 13, 
        "type": "DOWN"
    }, 
    {
        "bought": 368.74, 
        "bought_more": 0, 
        "business_id": 7, 
        "completed": "2018-01-26T15:09:45.576066-05:00", 
        "created": "2018-01-26T14:54:11.869738-05:00", 
        "id": 26, 
        "profit": -11, 
        "sold": 369.62, 
        "symbol": "BIIB", 
        "total_shares": 13, 
        "type": "DOWN"
    }, 
    {
        "bought": 368.74, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-26T15:09:45.576066-05:00", 
        "created": "2018-01-26T14:54:11.869738-05:00", 
        "id": 100, 
        "profit": -11, 
        "sold": 369.62, 
        "symbol": "BIIB", 
        "total_shares": 13, 
        "type": "DOWN"
    }, 
    {
        "bought": 368.13, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-26T14:50:00.560133-05:00", 
        "created": "2018-01-26T14:34:56.228089-05:00", 
        "id": 77, 
        "profit": -11, 
        "sold": 369.03, 
        "symbol": "BIIB", 
        "total_shares": 13, 
        "type": "DOWN"
    }, 
    {
        "bought": 368.13, 
        "bought_more": 0, 
        "business_id": 7, 
        "completed": "2018-01-26T14:50:00.560133-05:00", 
        "created": "2018-01-26T14:34:56.228089-05:00", 
        "id": 3, 
        "profit": -11, 
        "sold": 369.03, 
        "symbol": "BIIB", 
        "total_shares": 13, 
        "type": "DOWN"
    }, 
    {
        "bought": 368.09, 
        "bought_more": 0, 
        "business_id": 7, 
        "completed": "2018-01-26T14:27:00.386514-05:00", 
        "created": "2018-01-26T14:26:56.859543-05:00", 
        "id": 24, 
        "profit": 0, 
        "sold": 368.09, 
        "symbol": "BIIB", 
        "total_shares": 13, 
        "type": "DOWN"
    }, 
    {
        "bought": 368.09, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-26T14:27:00.386514-05:00", 
        "created": "2018-01-26T14:26:56.859543-05:00", 
        "id": 98, 
        "profit": 0, 
        "sold": 368.09, 
        "symbol": "BIIB", 
        "total_shares": 13, 
        "type": "DOWN"
    }, 
    {
        "bought": 368.65, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-26T14:18:01.453259-05:00", 
        "created": "2018-01-26T14:02:56.575330-05:00", 
        "id": 82, 
        "profit": 7, 
        "sold": 368.05, 
        "symbol": "BIIB", 
        "total_shares": 13, 
        "type": "DOWN"
    }, 
    {
        "bought": 368.65, 
        "bought_more": 0, 
        "business_id": 7, 
        "completed": "2018-01-26T14:18:01.453259-05:00", 
        "created": "2018-01-26T14:02:56.575330-05:00", 
        "id": 8, 
        "profit": 7, 
        "sold": 368.05, 
        "symbol": "BIIB", 
        "total_shares": 13, 
        "type": "DOWN"
    }, 
    {
        "bought": 368.89, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-26T13:58:45.337950-05:00", 
        "created": "2018-01-26T13:43:11.362424-05:00", 
        "id": 81, 
        "profit": 6, 
        "sold": 368.425, 
        "symbol": "BIIB", 
        "total_shares": 13, 
        "type": "DOWN"
    }, 
    {
        "bought": 368.89, 
        "bought_more": 0, 
        "business_id": 7, 
        "completed": "2018-01-26T13:58:45.337950-05:00", 
        "created": "2018-01-26T13:43:11.362424-05:00", 
        "id": 7, 
        "profit": 6, 
        "sold": 368.425, 
        "symbol": "BIIB", 
        "total_shares": 13, 
        "type": "DOWN"
    }, 
    {
        "bought": 369.87, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-26T13:38:45.811051-05:00", 
        "created": "2018-01-26T13:23:11.762170-05:00", 
        "id": 80, 
        "profit": 6, 
        "sold": 369.38, 
        "symbol": "BIIB", 
        "total_shares": 13, 
        "type": "DOWN"
    }, 
    {
        "bought": 369.87, 
        "bought_more": 0, 
        "business_id": 7, 
        "completed": "2018-01-26T13:38:45.811051-05:00", 
        "created": "2018-01-26T13:23:11.762170-05:00", 
        "id": 6, 
        "profit": 6, 
        "sold": 369.38, 
        "symbol": "BIIB", 
        "total_shares": 13, 
        "type": "DOWN"
    }, 
    {
        "bought": 369.15, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-26T13:19:00.468934-05:00", 
        "created": "2018-01-26T13:03:56.897093-05:00", 
        "id": 79, 
        "profit": -9, 
        "sold": 369.87, 
        "symbol": "BIIB", 
        "total_shares": 13, 
        "type": "DOWN"
    }, 
    {
        "bought": 369.15, 
        "bought_more": 0, 
        "business_id": 7, 
        "completed": "2018-01-26T13:19:00.468934-05:00", 
        "created": "2018-01-26T13:03:56.897093-05:00", 
        "id": 5, 
        "profit": -9, 
        "sold": 369.87, 
        "symbol": "BIIB", 
        "total_shares": 13, 
        "type": "DOWN"
    }, 
    {
        "bought": 368.9, 
        "bought_more": 0, 
        "business_id": 7, 
        "completed": "2018-01-26T12:59:45.663992-05:00", 
        "created": "2018-01-26T12:44:11.880302-05:00", 
        "id": 4, 
        "profit": -14, 
        "sold": 370.04, 
        "symbol": "BIIB", 
        "total_shares": 13, 
        "type": "DOWN"
    }, 
    {
        "bought": 368.9, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-26T12:59:45.663992-05:00", 
        "created": "2018-01-26T12:44:11.880302-05:00", 
        "id": 78, 
        "profit": -14, 
        "sold": 370.04, 
        "symbol": "BIIB", 
        "total_shares": 13, 
        "type": "DOWN"
    }, 
    {
        "bought": 369.25, 
        "bought_more": 0, 
        "business_id": 7, 
        "completed": "2018-01-26T12:39:45.963507-05:00", 
        "created": "2018-01-26T12:24:12.018528-05:00", 
        "id": 17, 
        "profit": 4, 
        "sold": 368.93, 
        "symbol": "BIIB", 
        "total_shares": 13, 
        "type": "DOWN"
    }, 
    {
        "bought": 369.25, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-26T12:39:45.963507-05:00", 
        "created": "2018-01-26T12:24:12.018528-05:00", 
        "id": 91, 
        "profit": 4, 
        "sold": 368.93, 
        "symbol": "BIIB", 
        "total_shares": 13, 
        "type": "DOWN"
    }, 
    {
        "bought": 79.68, 
        "bought_more": 0, 
        "business_id": 7, 
        "completed": "2018-01-29T09:44:48.898852-05:00", 
        "created": "2018-01-26T14:29:01.571905-05:00", 
        "id": 35, 
        "profit": 50, 
        "sold": 80.49, 
        "symbol": "C", 
        "total_shares": 62, 
        "type": "UP"
    }, 
    {
        "bought": 79.68, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-29T09:44:48.898852-05:00", 
        "created": "2018-01-26T14:29:01.571905-05:00", 
        "id": 116, 
        "profit": 50, 
        "sold": 80.49, 
        "symbol": "C", 
        "total_shares": 62, 
        "type": "UP"
    }, 
    {
        "bought": 79.68, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-26T14:22:46.621134-05:00", 
        "created": "2018-01-26T12:20:03.231753-05:00", 
        "id": 90, 
        "profit": 11, 
        "sold": 79.865, 
        "symbol": "C", 
        "total_shares": 62, 
        "type": "UP"
    }, 
    {
        "bought": 79.68, 
        "bought_more": 0, 
        "business_id": 7, 
        "completed": "2018-01-26T14:22:46.621134-05:00", 
        "created": "2018-01-26T12:20:03.231753-05:00", 
        "id": 16, 
        "profit": 11, 
        "sold": 79.865, 
        "symbol": "C", 
        "total_shares": 62, 
        "type": "UP"
    }, 
    {
        "bought": 52.61, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T13:45:46.042627-05:00", 
        "created": "2018-01-30T13:40:11.359448-05:00", 
        "id": 120, 
        "profit": 5, 
        "sold": 52.67, 
        "symbol": "CC", 
        "total_shares": 95, 
        "type": "UP"
    }, 
    {
        "bought": 52.535, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T13:36:00.363034-05:00", 
        "created": "2018-01-30T13:30:56.650186-05:00", 
        "id": 183, 
        "profit": 4, 
        "sold": 52.58, 
        "symbol": "CC", 
        "total_shares": 95, 
        "type": "UP"
    }, 
    {
        "bought": 52.6, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T13:26:45.664899-05:00", 
        "created": "2018-01-30T13:21:11.661048-05:00", 
        "id": 176, 
        "profit": -6, 
        "sold": 52.53, 
        "symbol": "CC", 
        "total_shares": 95, 
        "type": "UP"
    }, 
    {
        "bought": 52.57, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T13:17:00.511654-05:00", 
        "created": "2018-01-30T13:11:56.728431-05:00", 
        "id": 166, 
        "profit": 0, 
        "sold": 52.58, 
        "symbol": "CC", 
        "total_shares": 95, 
        "type": "UP"
    }, 
    {
        "bought": 52.6, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T13:07:45.483446-05:00", 
        "created": "2018-01-30T13:02:11.902645-05:00", 
        "id": 158, 
        "profit": -13, 
        "sold": 52.46, 
        "symbol": "CC", 
        "total_shares": 95, 
        "type": "UP"
    }, 
    {
        "bought": 52.5852, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T12:58:00.673974-05:00", 
        "created": "2018-01-30T12:52:56.336367-05:00", 
        "id": 145, 
        "profit": 0, 
        "sold": 52.59, 
        "symbol": "CC", 
        "total_shares": 95, 
        "type": "UP"
    }, 
    {
        "bought": 52.565, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T12:48:45.433713-05:00", 
        "created": "2018-01-30T12:43:11.814062-05:00", 
        "id": 118, 
        "profit": -1, 
        "sold": 52.55, 
        "symbol": "CC", 
        "total_shares": 95, 
        "type": "UP"
    }, 
    {
        "bought": 52.545, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T12:39:00.744353-05:00", 
        "created": "2018-01-30T12:33:56.741891-05:00", 
        "id": 115, 
        "profit": 2, 
        "sold": 52.57, 
        "symbol": "CC", 
        "total_shares": 95, 
        "type": "UP"
    }, 
    {
        "bought": 52.58, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T12:29:45.655935-05:00", 
        "created": "2018-01-30T12:24:11.330661-05:00", 
        "id": 182, 
        "profit": -3, 
        "sold": 52.54, 
        "symbol": "CC", 
        "total_shares": 95, 
        "type": "UP"
    }, 
    {
        "bought": 52.58, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T12:20:00.347894-05:00", 
        "created": "2018-01-30T12:14:56.446953-05:00", 
        "id": 175, 
        "profit": 2, 
        "sold": 52.605, 
        "symbol": "CC", 
        "total_shares": 95, 
        "type": "UP"
    }, 
    {
        "bought": 52.64, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T12:10:45.431096-05:00", 
        "created": "2018-01-30T12:05:11.325441-05:00", 
        "id": 174, 
        "profit": -2, 
        "sold": 52.615, 
        "symbol": "CC", 
        "total_shares": 94, 
        "type": "UP"
    }, 
    {
        "bought": 52.65, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T12:00:46.195411-05:00", 
        "created": "2018-01-30T11:55:11.677582-05:00", 
        "id": 164, 
        "profit": 0, 
        "sold": 52.66, 
        "symbol": "CC", 
        "total_shares": 94, 
        "type": "UP"
    }, 
    {
        "bought": 52.745, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T11:51:00.375304-05:00", 
        "created": "2018-01-30T11:45:57.102664-05:00", 
        "id": 157, 
        "profit": -8, 
        "sold": 52.65, 
        "symbol": "CC", 
        "total_shares": 94, 
        "type": "UP"
    }, 
    {
        "bought": 52.63, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T11:41:45.388103-05:00", 
        "created": "2018-01-30T11:36:11.627437-05:00", 
        "id": 144, 
        "profit": 3, 
        "sold": 52.67, 
        "symbol": "CC", 
        "total_shares": 95, 
        "type": "UP"
    }, 
    {
        "bought": 52.62, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T11:32:00.344311-05:00", 
        "created": "2018-01-30T11:26:56.791366-05:00", 
        "id": 181, 
        "profit": -2, 
        "sold": 52.59, 
        "symbol": "CC", 
        "total_shares": 95, 
        "type": "UP"
    }, 
    {
        "bought": 52.59, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T11:22:45.630022-05:00", 
        "created": "2018-01-30T11:17:11.171979-05:00", 
        "id": 172, 
        "profit": -1, 
        "sold": 52.57, 
        "symbol": "CC", 
        "total_shares": 95, 
        "type": "UP"
    }, 
    {
        "bought": 52.61, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T11:12:45.723178-05:00", 
        "created": "2018-01-30T11:07:11.266902-05:00", 
        "id": 163, 
        "profit": -4, 
        "sold": 52.56, 
        "symbol": "CC", 
        "total_shares": 95, 
        "type": "UP"
    }, 
    {
        "bought": 52.58, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T11:02:45.930930-05:00", 
        "created": "2018-01-30T10:57:11.681582-05:00", 
        "id": 143, 
        "profit": 6, 
        "sold": 52.65, 
        "symbol": "CC", 
        "total_shares": 95, 
        "type": "UP"
    }, 
    {
        "bought": 52.37, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T10:53:00.449527-05:00", 
        "created": "2018-01-30T10:47:57.060431-05:00", 
        "id": 109, 
        "profit": 4, 
        "sold": 52.42, 
        "symbol": "CC", 
        "total_shares": 95, 
        "type": "UP"
    }, 
    {
        "bought": 52.52, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T10:39:45.588457-05:00", 
        "created": "2018-01-30T10:34:11.448930-05:00", 
        "id": 170, 
        "profit": 0, 
        "sold": 52.52, 
        "symbol": "CC", 
        "total_shares": 95, 
        "type": "UP"
    }, 
    {
        "bought": 52.2005, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T10:30:00.405292-05:00", 
        "created": "2018-01-30T10:24:55.871793-05:00", 
        "id": 154, 
        "profit": 12, 
        "sold": 52.33, 
        "symbol": "CC", 
        "total_shares": 95, 
        "type": "UP"
    }, 
    {
        "bought": 52.31, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T10:20:00.885616-05:00", 
        "created": "2018-01-30T10:14:56.639658-05:00", 
        "id": 152, 
        "profit": 1, 
        "sold": 52.33, 
        "symbol": "CC", 
        "total_shares": 95, 
        "type": "UP"
    }, 
    {
        "bought": 52.3, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T10:10:02.752313-05:00", 
        "created": "2018-01-30T10:04:58.615894-05:00", 
        "id": 139, 
        "profit": -2, 
        "sold": 52.2711, 
        "symbol": "CC", 
        "total_shares": 95, 
        "type": "UP"
    }, 
    {
        "bought": 52.75, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T10:00:01.762175-05:00", 
        "created": "2018-01-30T09:30:46.914093-05:00", 
        "id": 161, 
        "profit": -35, 
        "sold": 52.37, 
        "symbol": "CC", 
        "total_shares": 94, 
        "type": "UP"
    }, 
    {
        "bought": 53.28159879215937, 
        "bought_more": 30, 
        "business_id": 7, 
        "completed": "2018-01-29T10:17:02.384475-05:00", 
        "created": "2018-01-26T14:29:01.451444-05:00", 
        "id": 34, 
        "profit": 1583, 
        "sold": 53.83, 
        "symbol": "CC", 
        "total_shares": 2887, 
        "type": "UP"
    }, 
    {
        "bought": 53.28159879215937, 
        "bought_more": 30, 
        "business_id": 1, 
        "completed": "2018-01-29T10:17:02.384475-05:00", 
        "created": "2018-01-26T14:29:01.451444-05:00", 
        "id": 114, 
        "profit": 1583, 
        "sold": 53.83, 
        "symbol": "CC", 
        "total_shares": 2887, 
        "type": "UP"
    }, 
    {
        "bought": 53.18516336760372, 
        "bought_more": 30, 
        "business_id": 1, 
        "completed": "2018-01-26T14:22:46.623093-05:00", 
        "created": "2018-01-26T12:20:02.200852-05:00", 
        "id": 93, 
        "profit": 450, 
        "sold": 53.34, 
        "symbol": "CC", 
        "total_shares": 2912, 
        "type": "UP"
    }, 
    {
        "bought": 53.18516336760372, 
        "bought_more": 30, 
        "business_id": 7, 
        "completed": "2018-01-26T14:22:46.623093-05:00", 
        "created": "2018-01-26T12:20:02.200852-05:00", 
        "id": 19, 
        "profit": 450, 
        "sold": 53.34, 
        "symbol": "CC", 
        "total_shares": 2912, 
        "type": "UP"
    }, 
    {
        "bought": 16.035, 
        "bought_more": 0, 
        "business_id": 7, 
        "completed": "2018-01-29T10:27:46.242215-05:00", 
        "created": "2018-01-26T14:29:01.479545-05:00", 
        "id": 38, 
        "profit": 51, 
        "sold": 16.2, 
        "symbol": "GE", 
        "total_shares": 311, 
        "type": "UP"
    }, 
    {
        "bought": 16.035, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-29T10:27:46.242215-05:00", 
        "created": "2018-01-26T14:29:01.479545-05:00", 
        "id": 123, 
        "profit": 51, 
        "sold": 16.2, 
        "symbol": "GE", 
        "total_shares": 311, 
        "type": "UP"
    }, 
    {
        "bought": 1169.9175, 
        "bought_more": 0, 
        "business_id": 7, 
        "completed": "2018-01-29T09:37:03.570617-05:00", 
        "created": "2018-01-26T14:30:46.599259-05:00", 
        "id": 36, 
        "profit": 20, 
        "sold": 1175.0, 
        "symbol": "GOOG", 
        "total_shares": 4, 
        "type": "UP"
    }, 
    {
        "bought": 1169.9175, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-29T09:37:03.570617-05:00", 
        "created": "2018-01-26T14:30:46.599259-05:00", 
        "id": 117, 
        "profit": 20, 
        "sold": 1175.0, 
        "symbol": "GOOG", 
        "total_shares": 4, 
        "type": "UP"
    }, 
    {
        "bought": 1166.87, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-26T14:22:46.708669-05:00", 
        "created": "2018-01-26T12:20:03.611707-05:00", 
        "id": 95, 
        "profit": 20, 
        "sold": 1171.88, 
        "symbol": "GOOG", 
        "total_shares": 4, 
        "type": "UP"
    }, 
    {
        "bought": 1166.87, 
        "bought_more": 0, 
        "business_id": 7, 
        "completed": "2018-01-26T14:22:46.708669-05:00", 
        "created": "2018-01-26T12:20:03.611707-05:00", 
        "id": 21, 
        "profit": 20, 
        "sold": 1171.88, 
        "symbol": "GOOG", 
        "total_shares": 4, 
        "type": "UP"
    }, 
    {
        "bought": 50.38, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-30T13:56:45.642860-05:00", 
        "created": "2018-01-30T13:46:47.895277-05:00", 
        "id": 122, 
        "profit": 10, 
        "sold": 50.49, 
        "symbol": "HOG", 
        "total_shares": 99, 
        "type": "UP"
    }, 
    {
        "bought": 50.53, 
        "bought_more": 0, 
        "business_id": 7, 
        "completed": "2018-01-26T14:22:46.562686-05:00", 
        "created": "2018-01-26T14:10:47.265013-05:00", 
        "id": 15, 
        "profit": 27, 
        "sold": 50.81, 
        "symbol": "HOG", 
        "total_shares": 98, 
        "type": "UP"
    }, 
    {
        "bought": 2.29, 
        "bought_more": 0, 
        "business_id": 7, 
        "completed": "2018-01-29T09:48:48.132516-05:00", 
        "created": "2018-01-26T14:30:45.981656-05:00", 
        "id": 33, 
        "profit": 109, 
        "sold": 2.34, 
        "symbol": "HVBTF", 
        "total_shares": 2183, 
        "type": "UP"
    }, 
    {
        "bought": 2.29, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-29T09:48:48.132516-05:00", 
        "created": "2018-01-26T14:30:45.981656-05:00", 
        "id": 108, 
        "profit": 109, 
        "sold": 2.34, 
        "symbol": "HVBTF", 
        "total_shares": 2183, 
        "type": "UP"
    }, 
    {
        "bought": 2.31, 
        "bought_more": 0, 
        "business_id": 7, 
        "completed": "2018-01-26T14:22:45.567188-05:00", 
        "created": "2018-01-26T12:20:00.589245-05:00", 
        "id": 9, 
        "profit": -55, 
        "sold": 2.2844, 
        "symbol": "HVBTF", 
        "total_shares": 2164, 
        "type": "UP"
    }, 
    {
        "bought": 2.31, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-26T14:22:45.567188-05:00", 
        "created": "2018-01-26T12:20:00.589245-05:00", 
        "id": 83, 
        "profit": -55, 
        "sold": 2.2844, 
        "symbol": "HVBTF", 
        "total_shares": 2164, 
        "type": "UP"
    }, 
    {
        "bought": 9.475, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-29T09:39:48.783933-05:00", 
        "created": "2018-01-26T14:30:46.728562-05:00", 
        "id": 124, 
        "profit": 164, 
        "sold": 9.788, 
        "symbol": "KODK", 
        "total_shares": 527, 
        "type": "UP"
    }, 
    {
        "bought": 9.475, 
        "bought_more": 0, 
        "business_id": 7, 
        "completed": "2018-01-29T09:39:48.783933-05:00", 
        "created": "2018-01-26T14:30:46.728562-05:00", 
        "id": 39, 
        "profit": 164, 
        "sold": 9.788, 
        "symbol": "KODK", 
        "total_shares": 527, 
        "type": "UP"
    }, 
    {
        "bought": 9.655, 
        "bought_more": 0, 
        "business_id": 7, 
        "completed": "2018-01-26T14:22:46.547289-05:00", 
        "created": "2018-01-26T12:20:02.100812-05:00", 
        "id": 13, 
        "profit": -43, 
        "sold": 9.5716, 
        "symbol": "KODK", 
        "total_shares": 517, 
        "type": "UP"
    }, 
    {
        "bought": 9.655, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-26T14:22:46.547289-05:00", 
        "created": "2018-01-26T12:20:02.100812-05:00", 
        "id": 87, 
        "profit": -43, 
        "sold": 9.5716, 
        "symbol": "KODK", 
        "total_shares": 517, 
        "type": "UP"
    }, 
    {
        "bought": 27.15, 
        "bought_more": 0, 
        "business_id": 7, 
        "completed": "2018-01-29T09:37:48.916807-05:00", 
        "created": "2018-01-26T14:29:01.570944-05:00", 
        "id": 37, 
        "profit": 31, 
        "sold": 27.32, 
        "symbol": "M", 
        "total_shares": 184, 
        "type": "UP"
    }, 
    {
        "bought": 27.15, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-29T09:37:48.916807-05:00", 
        "created": "2018-01-26T14:29:01.570944-05:00", 
        "id": 119, 
        "profit": 31, 
        "sold": 27.32, 
        "symbol": "M", 
        "total_shares": 184, 
        "type": "UP"
    }, 
    {
        "bought": 26.955, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-26T14:22:46.545716-05:00", 
        "created": "2018-01-26T12:20:02.305611-05:00", 
        "id": 86, 
        "profit": 33, 
        "sold": 27.135, 
        "symbol": "M", 
        "total_shares": 185, 
        "type": "UP"
    }, 
    {
        "bought": 26.955, 
        "bought_more": 0, 
        "business_id": 7, 
        "completed": "2018-01-26T14:22:46.545716-05:00", 
        "created": "2018-01-26T12:20:02.305611-05:00", 
        "id": 12, 
        "profit": 33, 
        "sold": 27.135, 
        "symbol": "M", 
        "total_shares": 185, 
        "type": "UP"
    }, 
    {
        "bought": 7.78, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-29T10:00:03.148653-05:00", 
        "created": "2018-01-26T16:29:45.852041-05:00", 
        "id": 126, 
        "profit": -83, 
        "sold": 7.65, 
        "symbol": "NETE", 
        "total_shares": 642, 
        "type": "UP"
    }, 
    {
        "bought": 7.78, 
        "bought_more": 0, 
        "business_id": 7, 
        "completed": "2018-01-29T10:00:03.148653-05:00", 
        "created": "2018-01-26T16:29:45.852041-05:00", 
        "id": 41, 
        "profit": -83, 
        "sold": 7.65, 
        "symbol": "NETE", 
        "total_shares": 642, 
        "type": "UP"
    }, 
    {
        "bought": 242.13, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-29T14:03:46.165153-05:00", 
        "created": "2018-01-26T14:34:57.062868-05:00", 
        "id": 127, 
        "profit": -103, 
        "sold": 247.32, 
        "symbol": "NVDA", 
        "total_shares": 20, 
        "type": "DOWN"
    }, 
    {
        "bought": 242.13, 
        "bought_more": 0, 
        "business_id": 7, 
        "completed": "2018-01-29T14:03:46.165153-05:00", 
        "created": "2018-01-26T14:34:57.062868-05:00", 
        "id": 42, 
        "profit": -103, 
        "sold": 247.32, 
        "symbol": "NVDA", 
        "total_shares": 20, 
        "type": "DOWN"
    }, 
    {
        "bought": 241.216, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-26T14:22:46.358979-05:00", 
        "created": "2018-01-26T12:27:56.795992-05:00", 
        "id": 84, 
        "profit": -21, 
        "sold": 242.29, 
        "symbol": "NVDA", 
        "total_shares": 20, 
        "type": "DOWN"
    }, 
    {
        "bought": 241.216, 
        "bought_more": 0, 
        "business_id": 7, 
        "completed": "2018-01-26T14:22:46.358979-05:00", 
        "created": "2018-01-26T12:27:56.795992-05:00", 
        "id": 10, 
        "profit": -21, 
        "sold": 242.29, 
        "symbol": "NVDA", 
        "total_shares": 20, 
        "type": "DOWN"
    }, 
    {
        "bought": 275.03, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-29T11:25:02.637985-05:00", 
        "created": "2018-01-26T14:30:46.299519-05:00", 
        "id": 131, 
        "profit": -30, 
        "sold": 273.32, 
        "symbol": "ORLY", 
        "total_shares": 18, 
        "type": "UP"
    }, 
    {
        "bought": 275.03, 
        "bought_more": 0, 
        "business_id": 7, 
        "completed": "2018-01-29T11:25:02.637985-05:00", 
        "created": "2018-01-26T14:30:46.299519-05:00", 
        "id": 46, 
        "profit": -30, 
        "sold": 273.32, 
        "symbol": "ORLY", 
        "total_shares": 18, 
        "type": "UP"
    }, 
    {
        "bought": 274.08, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-26T14:22:46.823018-05:00", 
        "created": "2018-01-26T12:20:01.826055-05:00", 
        "id": 96, 
        "profit": 24, 
        "sold": 275.46, 
        "symbol": "ORLY", 
        "total_shares": 18, 
        "type": "UP"
    }, 
    {
        "bought": 274.08, 
        "bought_more": 0, 
        "business_id": 7, 
        "completed": "2018-01-26T14:22:46.823018-05:00", 
        "created": "2018-01-26T12:20:01.826055-05:00", 
        "id": 22, 
        "profit": 24, 
        "sold": 275.46, 
        "symbol": "ORLY", 
        "total_shares": 18, 
        "type": "UP"
    }, 
    {
        "bought": 40.73, 
        "bought_more": 0, 
        "business_id": 7, 
        "completed": "2018-01-29T14:03:46.316085-05:00", 
        "created": "2018-01-26T14:30:46.942666-05:00", 
        "id": 48, 
        "profit": -17, 
        "sold": 40.87, 
        "symbol": "SKX", 
        "total_shares": 122, 
        "type": "DOWN"
    }, 
    {
        "bought": 40.73, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-29T14:03:46.316085-05:00", 
        "created": "2018-01-26T14:30:46.942666-05:00", 
        "id": 133, 
        "profit": -17, 
        "sold": 40.87, 
        "symbol": "SKX", 
        "total_shares": 122, 
        "type": "DOWN"
    }, 
    {
        "bought": 40.74, 
        "bought_more": 0, 
        "business_id": 7, 
        "completed": "2018-01-26T14:22:46.360839-05:00", 
        "created": "2018-01-26T12:20:01.964961-05:00", 
        "id": 11, 
        "profit": -1, 
        "sold": 40.75, 
        "symbol": "SKX", 
        "total_shares": 122, 
        "type": "DOWN"
    }, 
    {
        "bought": 40.74, 
        "bought_more": 0, 
        "business_id": 1, 
        "completed": "2018-01-26T14:22:46.360839-05:00", 
        "created": "2018-01-26T12:20:01.964961-05:00", 
        "id": 85, 
        "profit": -1, 
        "sold": 40.75, 
        "symbol": "SKX", 
        "total_shares": 122, 
        "type": "DOWN"
    }
]
```


GET CSV profit details
------
<code request-method="GET">**GET** /execute-status/profit/details.csv</code>

Get all executed transactions profits detail symbol

### Example
```http
GET http://localhost:6789/execute-status/profit/details.csv
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
Content-Type: text/csv
Date: Fri, 02 Feb 2018 14:13:57 GMT
Expires: 0
Server: TwistedWeb/16.6.0
Transfer-Encoding: chunked
Vary: Origin

"bought","bought_more","business_id","completed","completed_date","created","id","profit","sold","symbol","total_shares","type"
358.48,0,1,"2018-01-30 14:46:06.307693","2018-01-30","2018-01-30 14:30:04.793414",150,76,352.5719,"BIIB",13,"DOWN"
1417.68,0,1,"2018-01-30 14:30:47.162525","2018-01-30","2018-01-30 14:30:06.271396",149,71,1394.0001,"AMZN",3,"DOWN"
198.9,0,1,"2018-01-30 15:00:48.108927","2018-01-30","2018-01-30 14:30:06.601707",151,-25,197.9,"BABA",25,"UP"
52.75,0,1,"2018-01-30 15:00:01.762175","2018-01-30","2018-01-30 14:30:46.914093",161,-35,52.37,"CC",94,"UP"
1402.75,0,1,"2018-01-30 15:00:01.853561","2018-01-30","2018-01-30 14:35:57.356648",169,15,1408.0,"AMZN",3,"UP"
352.2199,0,1,"2018-01-30 15:01:00.504263","2018-01-30","2018-01-30 14:50:57.003302",179,10,352.975,"BIIB",14,"UP"
52.3,0,1,"2018-01-30 15:10:02.752313","2018-01-30","2018-01-30 15:04:58.615894",139,-2,52.2711,"CC",95,"UP"
1406.8489,0,1,"2018-01-30 15:11:46.388014","2018-01-30","2018-01-30 15:04:58.784661",141,9,1409.9705,"AMZN",3,"UP"
352.39,0,1,"2018-01-30 15:11:00.903426","2018-01-30","2018-01-30 15:05:58.968399",140,17,353.63,"BIIB",14,"UP"
52.31,0,1,"2018-01-30 15:20:00.885616","2018-01-30","2018-01-30 15:14:56.639658",152,1,52.33,"CC",95,"UP"
354.0,0,1,"2018-01-30 15:21:45.615626","2018-01-30","2018-01-30 15:15:57.325112",153,10,354.73,"BIIB",14,"UP"
1412.04,0,1,"2018-01-30 15:43:00.505442","2018-01-30","2018-01-30 15:16:13.411477",155,10,1415.67,"AMZN",3,"UP"
52.2005,0,1,"2018-01-30 15:30:00.405292","2018-01-30","2018-01-30 15:24:55.871793",154,12,52.33,"CC",95,"UP"
355.62,0,1,"2018-01-30 15:31:00.857597","2018-01-30","2018-01-30 15:25:56.582663",162,16,356.8,"BIIB",14,"UP"
52.52,0,1,"2018-01-30 15:39:45.588457","2018-01-30","2018-01-30 15:34:11.448930",170,0,52.52,"CC",95,"UP"
356.21,0,1,"2018-01-30 15:42:45.724105","2018-01-30","2018-01-30 15:35:56.021571",171,11,357.05,"BIIB",14,"UP"
52.37,0,1,"2018-01-30 15:53:00.449527","2018-01-30","2018-01-30 15:47:57.060431",109,4,52.42,"CC",95,"UP"
1413.882,0,1,"2018-01-30 15:56:45.731635","2018-01-30","2018-01-30 15:47:57.247726",110,13,1418.23,"AMZN",3,"UP"
356.85,0,1,"2018-01-30 16:24:00.945376","2018-01-30","2018-01-30 15:48:12.206966",111,11,357.6899,"BIIB",14,"UP"
52.58,0,1,"2018-01-30 16:02:45.930930","2018-01-30","2018-01-30 15:57:11.681582",143,6,52.65,"CC",95,"UP"
1421.555,0,1,"2018-01-30 16:09:46.140003","2018-01-30","2018-01-30 16:01:11.784045",156,13,1426.165,"AMZN",3,"UP"
52.61,0,1,"2018-01-30 16:12:45.723178","2018-01-30","2018-01-30 16:07:11.266902",163,-4,52.56,"CC",95,"UP"
1427.705,0,1,"2018-01-30 16:53:46.148407","2018-01-30","2018-01-30 16:14:12.323876",173,9,1430.9985,"AMZN",3,"UP"
52.59,0,1,"2018-01-30 16:22:45.630022","2018-01-30","2018-01-30 16:17:11.171979",172,-1,52.57,"CC",95,"UP"
52.62,0,1,"2018-01-30 16:32:00.344311","2018-01-30","2018-01-30 16:26:56.791366",181,-2,52.59,"CC",95,"UP"
52.63,0,1,"2018-01-30 16:41:45.388103","2018-01-30","2018-01-30 16:36:11.627437",144,3,52.67,"CC",95,"UP"
52.745,0,1,"2018-01-30 16:51:00.375304","2018-01-30","2018-01-30 16:45:57.102664",157,-8,52.65,"CC",94,"UP"
52.65,0,1,"2018-01-30 17:00:46.195411","2018-01-30","2018-01-30 16:55:11.677582",164,0,52.66,"CC",94,"UP"
1428.8308,0,1,"2018-01-30 17:23:00.441460","2018-01-30","2018-01-30 16:58:12.040941",165,9,1431.8835,"AMZN",3,"UP"
52.64,0,1,"2018-01-30 17:10:45.431096","2018-01-30","2018-01-30 17:05:11.325441",174,-2,52.615,"CC",94,"UP"
52.58,0,1,"2018-01-30 17:20:00.347894","2018-01-30","2018-01-30 17:14:56.446953",175,2,52.605,"CC",95,"UP"
52.58,0,1,"2018-01-30 17:29:45.655935","2018-01-30","2018-01-30 17:24:11.330661",182,-3,52.54,"CC",95,"UP"
52.545,0,1,"2018-01-30 17:39:00.744353","2018-01-30","2018-01-30 17:33:56.741891",115,2,52.57,"CC",95,"UP"
52.565,0,1,"2018-01-30 17:48:45.433713","2018-01-30","2018-01-30 17:43:11.814062",118,-1,52.55,"CC",95,"UP"
52.5852,0,1,"2018-01-30 17:58:00.673974","2018-01-30","2018-01-30 17:52:56.336367",145,0,52.59,"CC",95,"UP"
52.6,0,1,"2018-01-30 18:07:45.483446","2018-01-30","2018-01-30 18:02:11.902645",158,-13,52.46,"CC",95,"UP"
52.57,0,1,"2018-01-30 18:17:00.511654","2018-01-30","2018-01-30 18:11:56.728431",166,0,52.58,"CC",95,"UP"
52.6,0,1,"2018-01-30 18:26:45.664899","2018-01-30","2018-01-30 18:21:11.661048",176,-6,52.53,"CC",95,"UP"
52.535,0,1,"2018-01-30 18:36:00.363034","2018-01-30","2018-01-30 18:30:56.650186",183,4,52.58,"CC",95,"UP"
52.61,0,1,"2018-01-30 18:45:46.042627","2018-01-30","2018-01-30 18:40:11.359448",120,5,52.67,"CC",95,"UP"
50.38,0,1,"2018-01-30 18:56:45.642860","2018-01-30","2018-01-30 18:46:47.895277",122,10,50.49,"HOG",99,"UP"
53.28159879215937,30,1,"2018-01-29 15:17:02.384475","2018-01-29","2018-01-26 19:29:01.451444",114,1583,53.83,"CC",2887,"UP"
16.035,0,1,"2018-01-29 15:27:46.242215","2018-01-29","2018-01-26 19:29:01.479545",123,51,16.2,"GE",311,"UP"
27.15,0,1,"2018-01-29 14:37:48.916807","2018-01-29","2018-01-26 19:29:01.570944",119,31,27.32,"M",184,"UP"
79.68,0,1,"2018-01-29 14:44:48.898852","2018-01-29","2018-01-26 19:29:01.571905",116,50,80.49,"C",62,"UP"
2.29,0,1,"2018-01-29 14:48:48.132516","2018-01-29","2018-01-26 19:30:45.981656",108,109,2.34,"HVBTF",2183,"UP"
32.08,0,1,"2018-01-29 16:25:02.704483","2018-01-29","2018-01-26 19:30:46.164594",132,35,32.31,"BAC",155,"UP"
275.03,0,1,"2018-01-29 16:25:02.637985","2018-01-29","2018-01-26 19:30:46.299519",131,-30,273.32,"ORLY",18,"UP"
170.87,0,1,"2018-01-29 15:32:49.397762","2018-01-29","2018-01-26 19:30:46.324520",129,-91,167.725,"AAPL",29,"UP"
254.90480810286832,30,1,"2018-01-29 19:03:46.163043","2018-01-29","2018-01-26 19:30:46.327345",184,-73,255.03,"BIDU",589,"DOWN"
1169.9175,0,1,"2018-01-29 14:37:03.570617","2018-01-29","2018-01-26 19:30:46.599259",117,20,1175.0,"GOOG",4,"UP"
9.475,0,1,"2018-01-29 14:39:48.783933","2018-01-29","2018-01-26 19:30:46.728562",124,164,9.788,"KODK",527,"UP"
203.381,0,1,"2018-01-29 15:30:01.966158","2018-01-29","2018-01-26 19:30:46.844361",128,52,205.5765,"BABA",24,"UP"
40.73,0,1,"2018-01-29 19:03:46.316085","2018-01-29","2018-01-26 19:30:46.942666",133,-17,40.87,"SKX",122,"DOWN"
1397.71,0,1,"2018-01-29 19:03:46.376476","2018-01-29","2018-01-26 19:34:56.731418",125,-78,1423.7656,"AMZN",3,"DOWN"
242.13,0,1,"2018-01-29 19:03:46.165153","2018-01-29","2018-01-26 19:34:57.062868",127,-103,247.32,"NVDA",20,"DOWN"
7.78,0,1,"2018-01-29 15:00:03.148653","2018-01-29","2018-01-26 21:29:45.852041",126,-83,7.65,"NETE",642,"UP"
366.44841890193675,30,1,"2018-01-29 15:59:48.920356","2018-01-29","2018-01-26 21:31:56.962123",130,1503,362.7175,"BIIB",403,"DOWN"
168.17,0,1,"2018-01-29 19:31:01.098335","2018-01-29","2018-01-29 19:25:56.313848",135,-2,168.0852,"AAPL",29,"UP"
167.95,0,1,"2018-01-29 19:41:00.615265","2018-01-29","2018-01-29 19:35:56.154369",147,-4,167.79,"AAPL",29,"UP"
167.97,0,1,"2018-01-29 19:50:45.551180","2018-01-29","2018-01-29 19:45:11.468890",159,4,168.11,"AAPL",29,"UP"
168.0,0,1,"2018-01-29 20:00:00.578571","2018-01-29","2018-01-29 19:54:56.419456",167,6,168.21,"AAPL",29,"UP"
168.21,0,1,"2018-01-29 20:09:45.498895","2018-01-29","2018-01-29 20:04:11.636150",177,5,168.405,"AAPL",29,"UP"
168.3,0,1,"2018-01-29 20:19:00.470518","2018-01-29","2018-01-29 20:13:56.468639",105,6,168.519,"AAPL",29,"UP"
168.4,0,1,"2018-01-29 20:28:45.577458","2018-01-29","2018-01-29 20:23:11.231230",136,-7,168.14,"AAPL",29,"UP"
168.16,0,1,"2018-01-29 20:38:00.494667","2018-01-29","2018-01-29 20:32:56.562495",148,-5,167.9801,"AAPL",29,"UP"
168.15,0,1,"2018-01-29 20:47:45.577596","2018-01-29","2018-01-29 20:42:11.429427",160,-4,168.01,"AAPL",29,"UP"
168.14,0,1,"2018-01-29 20:57:00.495427","2018-01-29","2018-01-29 20:51:56.308682",168,3,168.27,"AAPL",29,"UP"
167.96,0,1,"2018-01-29 21:06:45.323305","2018-01-29","2018-01-29 21:01:11.531854",63,0,167.96,"AAPL",29,"UP"
167.96,0,1,"2018-01-29 21:06:45.323305","2018-01-29","2018-01-29 21:01:11.531854",178,0,167.96,"AAPL",29,"UP"
167.96,0,1,"2018-01-29 21:16:00.444527","2018-01-29","2018-01-29 21:10:56.192653",106,58,169.96,"AAPL",29,"UP"
168.96,0,1,"2018-01-29 21:25:45.582757","2018-01-29","2018-01-29 21:20:11.478952",137,-29,167.96,"AAPL",29,"UP"
2.31,0,1,"2018-01-26 19:22:45.567188","2018-01-26","2018-01-26 17:20:00.589245",83,-55,2.2844,"HVBTF",2164,"UP"
274.08,0,1,"2018-01-26 19:22:46.823018","2018-01-26","2018-01-26 17:20:01.826055",96,24,275.46,"ORLY",18,"UP"
40.74,0,1,"2018-01-26 19:22:46.360839","2018-01-26","2018-01-26 17:20:01.964961",85,-1,40.75,"SKX",122,"DOWN"
203.65154809265363,30,1,"2018-01-26 19:22:46.556665","2018-01-26","2018-01-26 17:20:01.999917",88,207,203.93,"BABA",744,"UP"
9.655,0,1,"2018-01-26 19:22:46.547289","2018-01-26","2018-01-26 17:20:02.100812",87,-43,9.5716,"KODK",517,"UP"
12.865,0,1,"2018-01-26 17:21:46.869848","2018-01-26","2018-01-26 17:20:02.113178",76,5,12.88,"AMD",388,"UP"
53.18516336760372,30,1,"2018-01-26 19:22:46.623093","2018-01-26","2018-01-26 17:20:02.200852",93,450,53.34,"CC",2912,"UP"
26.955,0,1,"2018-01-26 19:22:46.545716","2018-01-26","2018-01-26 17:20:02.305611",86,33,27.135,"M",185,"UP"
170.75,0,1,"2018-01-26 17:20:46.816094","2018-01-26","2018-01-26 17:20:02.383154",75,0,170.775,"AAPL",29,"DOWN"
32.08,0,1,"2018-01-26 19:22:46.710314","2018-01-26","2018-01-26 17:20:02.501869",94,7,32.13,"BAC",155,"UP"
79.68,0,1,"2018-01-26 19:22:46.621134","2018-01-26","2018-01-26 17:20:03.231753",90,11,79.865,"C",62,"UP"
1166.87,0,1,"2018-01-26 19:22:46.708669","2018-01-26","2018-01-26 17:20:03.611707",95,20,1171.88,"GOOG",4,"UP"
12.875,0,1,"2018-01-26 19:22:46.964043","2018-01-26","2018-01-26 17:22:46.426109",97,5,12.86,"AMD",388,"DOWN"
369.25,0,1,"2018-01-26 17:39:45.963507","2018-01-26","2018-01-26 17:24:12.018528",91,4,368.93,"BIIB",13,"DOWN"
170.77,0,1,"2018-01-26 19:22:46.620946","2018-01-26","2018-01-26 17:24:47.066662",92,-13,171.2488,"AAPL",29,"DOWN"
241.216,0,1,"2018-01-26 19:22:46.358979","2018-01-26","2018-01-26 17:27:56.795992",84,-21,242.29,"NVDA",20,"DOWN"
368.9,0,1,"2018-01-26 17:59:45.663992","2018-01-26","2018-01-26 17:44:11.880302",78,-14,370.04,"BIIB",13,"DOWN"
369.15,0,1,"2018-01-26 18:19:00.468934","2018-01-26","2018-01-26 18:03:56.897093",79,-9,369.87,"BIIB",13,"DOWN"
369.87,0,1,"2018-01-26 18:38:45.811051","2018-01-26","2018-01-26 18:23:11.762170",80,6,369.38,"BIIB",13,"DOWN"
368.89,0,1,"2018-01-26 18:58:45.337950","2018-01-26","2018-01-26 18:43:11.362424",81,6,368.425,"BIIB",13,"DOWN"
368.65,0,1,"2018-01-26 19:18:01.453259","2018-01-26","2018-01-26 19:02:56.575330",82,7,368.05,"BIIB",13,"DOWN"
259.5,0,1,"2018-01-26 19:22:46.562686","2018-01-26","2018-01-26 19:10:47.265013",89,-11,260.1,"BIDU",19,"DOWN"
368.09,0,1,"2018-01-26 19:27:00.386514","2018-01-26","2018-01-26 19:26:56.859543",98,0,368.09,"BIIB",13,"DOWN"
368.13,0,1,"2018-01-26 19:50:00.560133","2018-01-26","2018-01-26 19:34:56.228089",77,-11,369.03,"BIIB",13,"DOWN"
368.74,0,1,"2018-01-26 20:09:45.576066","2018-01-26","2018-01-26 19:54:11.869738",100,-11,369.62,"BIIB",13,"DOWN"
369.4712,0,1,"2018-01-26 20:29:00.612242","2018-01-26","2018-01-26 20:13:56.473984",101,23,367.7,"BIIB",13,"DOWN"
368.36,0,1,"2018-01-26 20:48:45.538403","2018-01-26","2018-01-26 20:33:11.925442",102,7,367.75,"BIIB",13,"DOWN"
367.8,0,1,"2018-01-26 21:08:00.449147","2018-01-26","2018-01-26 20:52:56.877384",103,-1,367.91,"BIIB",13,"DOWN"
367.91,0,1,"2018-01-26 21:27:45.668015","2018-01-26","2018-01-26 21:12:11.618914",104,0,367.91,"BIIB",13,"DOWN"

```

