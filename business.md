
Stock is business
======

`/business`

Everyone has its own business through login, ADMIN can create a new business

### Methods

Method | URL | Description
--- | --- | ---
**[GET](/documentation/endpoint/business#get-your-business-info)** | `business` | GET YOUR BUSINESS INFO
**[PUT](/documentation/endpoint/business#update-your-business-info)** | `business` | UPDATE YOUR BUSINESS INFO
**[POST](/documentation/endpoint/business#insert-new-business-info)** | `business` | INSERT NEW BUSINESS INFO

### Object Attributes

Attribute | Type | Readonly | Nullable | Has Default
--- | --- | --- | --- | ---
`business_role` | text | &nbsp; | &bullet; | &nbsp;
`created` | timestamp | &nbsp; | &nbsp; | &bullet;
`email` | text | &nbsp; | &nbsp; | &nbsp;
`hash_recovery` | text | &nbsp; | &bullet; | &nbsp;
`id` | integer | &bullet; | &nbsp; | &bullet;
`password` | text | &nbsp; | &nbsp; | &nbsp;
`phone` | text | &nbsp; | &bullet; | &nbsp;
`username` | text | &nbsp; | &nbsp; | &nbsp;

GET YOUR BUSINESS INFO
------
<code request-method="GET">**GET** business</code>

Get token from login

### Example
```http
GET http://localhost:6789/business/5
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
Date: Sat, 09 Dec 2017 15:58:15 GMT
Expires: 0
Server: TwistedWeb/17.1.0
Transfer-Encoding: chunked
Vary: Origin

{
    "business_role": "ADMIN", 
    "created": "2017-12-09T13:30:15.793683+00:00", 
    "email": "andreiradulescu@ymail.com", 
    "hash_recovery": null, 
    "id": 5, 
    "password": "3f2ca95425b52c7f40f3eab995bd9faa3ecda682", 
    "phone": "702-281-8629", 
    "username": "andrei"
}
```


UPDATE YOUR BUSINESS INFO
------
<code request-method="PUT">**PUT** business</code>

You can update email, phone, or even password and username. Business's id must be included

### Example
```http
PUT http://localhost:6789/business
Authorization: Basic YW5kcmVpOmFuZHJlaTEyMzQ1IQ==
Content-Length: 179
Content-Type: application/json
Host: localhost:6789
Origin: http://localhost:6789

{
    "business_role": "ADMIN", 
    "email": "andreiradulescu@ymail.com", 
    "id": 5, 
    "password": "andrei12345!", 
    "phone": "702-281-8629", 
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
Date: Sat, 09 Dec 2017 15:58:15 GMT
Expires: 0
Server: TwistedWeb/17.1.0
Transfer-Encoding: chunked
Vary: Origin

{
    "business_role": "ADMIN", 
    "created": "2017-12-09T13:30:15.793683+00:00", 
    "email": "andreiradulescu@ymail.com", 
    "hash_recovery": null, 
    "id": 5, 
    "password": "3f2ca95425b52c7f40f3eab995bd9faa3ecda682", 
    "phone": "702-281-8629", 
    "username": "andrei"
}
```


INSERT NEW BUSINESS INFO
------
<code request-method="POST">**POST** business</code>

You can update email, phone, or even password and username. Business's id must be included

### Example
```http
POST http://localhost:6789/business
Authorization: Basic YW5kcmVpOmFuZHJlaTEyMzQ1IQ==
Content-Length: 150
Content-Type: application/json
Host: localhost:6789
Origin: http://localhost:6789

{
    "business_role": "USERS", 
    "email": "test@ymail.com", 
    "password": "test12345!", 
    "phone": "702-281-8629", 
    "username": "test"
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
Date: Sat, 09 Dec 2017 15:58:16 GMT
Expires: 0
Server: TwistedWeb/17.1.0
Transfer-Encoding: chunked
Vary: Origin

{
    "business_role": "USERS", 
    "created": "2017-12-09T15:58:16.297225+00:00", 
    "email": "test@ymail.com", 
    "hash_recovery": null, 
    "id": 10, 
    "password": "cac933391b3df6244f5aa86fa93425f67e42c59f", 
    "phone": "702-281-8629", 
    "username": "test"
}
```

