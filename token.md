
Token Login
======

`/token`

Get token per log in: this is important to know how you are, what stock you are monitoring

### Methods

Method | URL | Description
--- | --- | ---
**[POST](/documentation/endpoint/token#login-token)** | `token` | LOGIN TOKEN

### Object Attributes

Attribute | Type | Readonly | Nullable | Has Default
--- | --- | --- | --- | ---
`business_id` | integer | &nbsp; | &bullet; | &nbsp;
`data` | text | &nbsp; | &bullet; | &nbsp;
`id` | text | &nbsp; | &nbsp; | &nbsp;
`lifetime` | integer | &nbsp; | &bullet; | &nbsp;
`modified` | timestamp | &nbsp; | &bullet; | &nbsp;
`set_cookie` | boolean | &nbsp; | &nbsp; | &bullet;

LOGIN TOKEN
------
<code request-method="POST">**POST** token</code>

Get token from login

### Example
```http
POST http://localhost:6789/token
Authorization: Basic YW5kcmVpOmFuZHJlaTEyMzQ1IQ==
Content-Length: 61
Content-Type: application/json
Host: localhost:6789
Origin: http://localhost:6789

{
    "password": "andrei12345!", 
    "username": "andrei"
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
    "business_id": 5, 
    "id": "xBVrAlenLRyFNOWpvmuIgcizZYofsDGX", 
    "lifetime": 2592000, 
    "modified": "2017-12-09T03:56:03+00:00", 
    "set_cookie": false
}
```

