# Introduction

Welcome to the Roypi API! You can use our API to access to our API endpoints.
This section describes the resources that make up the official Roypi API v1.

 1. [Current version](#current-version)
 2. [Schema](#schema)
 3. [Parameters](#parameters)

## Current version

Currently, we are building on the v1 version of the API.


## Schema

```shell
$ curl -i http://api.roypi.com
```
```http
HTTP/1.1 200 OK
Server: nginx/1.1.19
Date: Fri, 31 Jul 2015 06:54:52 GMT
Content-Type: application/javascript; charset=utf8
Transfer-Encoding: chunked
Connection: keep-alive
Vary: Host, Accept-Language, Cookie, Accept-Encoding
X-Frame-Options: SAMEORIGIN
Content-Language: en
Set-Cookie: sessionid=ogrfjqw1dwbs2szka7mf8zhdgrlghn82; Domain=.roypi.com; expires=Fri, 14-Aug-2015 06:54:52 GMT; httponly; Max-Age=1209600; Path=/

...
```

All API access is accessed from the `api.roypi.com` domain. All data is sent and received as JSON by default.

Blank fields are included as `null` instead of being omitted.

All timestamps are returned in ISO 8601 format:

<aside class="notice">YYYY-MM-DDTHH:MM:SSZ.</aside>


## Values as parameters

Many API methods take optional parameters. For GET requests, any parameters not specified as a segment
in the path can be passed as an HTTP query string parameter:

`$ curl -i "https://api.roypi.com/buyers/toni/products?state=closed"`

In this example, the ‘toni’ value is provided for the :buyer parameter in the path
while :state is passed in the query string.

## Values as input

For POST, PATCH, PUT, and DELETE requests, values not included in the URL should be encoded as JSON
with a Content-Type of ‘application/json’ like below:

`$ curl -i -u username -d '{"scopes":["public_repo"]}' https://api.roypi.com/authorizations`


