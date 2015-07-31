# Users

 1. [Get a user](#get-a-user)
 2. [Get the authenticated user](#get-the-authenticated-user)




## Get a user

```http
GET /users/300/ HTTP/1.1
Host: api.roypi.com
```
```http
HTTP/1.1 200 OK
Content-Type: application/json

{
    "id": 300,
    "username": "user_300",
    "email": "email300@gmail.com",
    "first_name": "",
    "last_name": "",
    "profiles": {}
}
```

Get any user by id

`GET /users/:user_id/`




## Get the authenticated user

```http
GET /users/me/ HTTP/1.1
Host: api.roypi.com
```
```http
HTTP/1.1 200 OK
Content-Type: application/json

{
    "id": 1165,
    "username": "RMdJ05M1RJ-uFuRPjnnNJA==",
    "email": "quzemmawa@email.com",
    "first_name": "",
    "last_name": "",
    "profiles": {
        "buyer_url": "http://api.roypi.com/buyers/528/",
        "supplier_url": "http://api.roypi.com/suppliers/991/"
    }
}
```

Get user only if user exists in the current session

`GET /users/me/`
