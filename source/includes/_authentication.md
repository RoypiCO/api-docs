# Authentication

 1. [Get access token](#get-access-token)
 2. [Refresh access token](#refresh-access-token)
 3. [Verify access token](#verify-access-token)




## Get access token

```http
POST /auth/access_token/ HTTP/1.1
Host: api.roypi.com
Content-Type: application/json; charset=utf-8

{ "username":"indestructible","password":"terminator123" }
```
```http
HTTP/1.1 200 OK
Content-Type: application/json

{
    "access_token":"eyJhbsfrgfedGciOi.JIUzdfdfdfdI1NiI.sInR5cCI6g54rewfgref",
    "expires_in":"2015-04-29T13:29:25.595Z",
    "user":"indestructible"
}
```

> Now in order to access protected api urls you must include the Authorization: Token header like this:

```http
POST /protected-url/ HTTP/1.1
Host: api.roypi.com
Authorization: Token eyJhbsfrgfedGciOi.JIUzdfdfdfdI1NiI.sInR5cCI6g54rewfgref
...
```

Get a token that can be used for authenticated requests. Expiration time for tokens is **5 days**.

`POST /auth/access_token/`

### Input

Name | Type | Description
---- | ---- | -----------
username | string | Username - **Required**.
password | string | Password - **Required**.





## Refresh access token

> Pass in an existing token to the refresh endpoint as follows:

```http
POST /auth/refresh_token/ HTTP/1.1
Host: api.roypi.com
Content-Type: application/json; charset=utf-8

{ "token": "SkE9PSIsIm9yaWdfaWF0IjoxNDM4Mzc5ODA1LCJ1c2VyX2lkIjoxMTY1LCJlbWFpbCI6InF1emVtbWF3YS02NjY4QHlvcG" }
```
```http
HTTP/1.1 200 OK
Content-Type: application/json

{
    "token":"eyJhbGciOiJ.eyJ1c2VybmFtZSI6IllbWFpbCI6InF1emVtbWF3YS02M4ODExOTQ2fQ.462gbEfvxuH24",
    "expires_in":"2015-08-05T21:59:06.912Z",
    "user":{
        "username":"RMdJ05M1RJ-uFuRPjnnNJA==",
        "id":1165
    }
}
```


Get a a refreshed token (with new expiration) based on existing token.
Note that you can only keep refreshing tokens up to **10 days**.

`POST /auth/refresh_token/`

<aside class="notice">
Only non-expired tokens will work. The JSON response looks the same as the normal access token endpoint with a new token.
</aside>

### Input

Name | Type | Description
---- | ---- | -----------
token | string | Current and active token - **Required**.



## Verify access token

> Passing a token to the verification endpoint will return a 200 response and the token if it is valid.
> Otherwise, it will return a 400 Bad Request as well as an error identifying why the token was invalid.

```http
POST /auth/verify_token/ HTTP/1.1
Host: api.roypi.com
Content-Type: application/json; charset=utf-8

{ "token": "eyJhbGciOiJ.eyJ1c2VybmFtZSI6IllbWFpbmVt02M4ODExOTQ2fQ.462gbEfvxuH24" }
```
```http
HTTP/1.1 200 OK
Content-Type: application/json

{
    "token":"eyJhbGciOiJ.eyJ1c2VybmFtZSI6IllbWFpbmVt02M4ODExOTQ2fQ.462gbEfvxuH24",
    "expires_in":"2015-08-05T21:59:06.912Z",
    "user":{
        "username":"RMdJ05M1RJ-uFuRPjnnNJA==",
        "id":1165
    }
}
```

Checks the veracity of a token, returning the token if it is valid.

`POST /auth/verify_token/`

### Input

Name | Type | Description
---- | ---- | -----------
token | string | Current and active token - **Required**.
