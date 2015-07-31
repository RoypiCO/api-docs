# Clients

 1. [List clients](#list-clients)
 1. [Get a client](#get-a-client)
 1. [List clients of a buyer](#list-clients-of-a-buyer)
 1. [Create a client for a buyer](#create-a-client-for-a-buyer)



## List clients

```http
GET /clients/ HTTP/1.1
Host: api.roypi.com
```

Anyone can list clients

`POST /clients/`



## Get a client

```http
GET /clients/1234/ HTTP/1.1
Host: api.roypi.com
```

Anyone can list clients

`POST /clients/:client_id/`



## List clients of a buyer

```http
GET /buyers/380/clients/ HTTP/1.1
Host: api.roypi.com
```
```http
HTTP/1.1 200 OK
Content-Type: application/json

{
    "count": 3,
    "next": null,
    "previous": null,
    "results": [
        {
            "id": 684,
            "name": "George",
            "email": "hi.geoom@gmail.com",
            "created": "2015-01-07T02:01:08Z",
            "modified": "2015-04-22T00:59:13Z"
        },
        {
            "id": 1370,
            "name": "new client",
            "email": "asdas@sakjkd.com",
            "created": "2015-04-22T00:58:44Z",
            "modified": "2015-04-22T00:58:44Z"
        },
        {
            "id": 1371,
            "name": "jajajajaj",
            "email": "dsljfljdf@gmail.com",
            "created": "2015-04-22T00:59:47Z",
            "modified": "2015-04-22T00:59:47Z"
        }
    ]
}
```

List the authenticated buyer's clients. The clients are final customers for buyers,
they are recorded in a invoice when a purchase is made or when a proforma is requested.

`GET /buyers/:buyer_id/clients/`



## Create a client for a buyer

```http
POST /buyers/111/clients/ HTTP/1.1
Host: api.roypi.com
```

Only an authenticated buyer can create a new client for itself

`POST /buyers/:buyer_id/clients/`

### Input

Name | Type | Description
---- | ---- | -----------
name | String | The unique name for a new client - **Required**.
email | String | The unique email for a new client with an strict format of email like *foo@email.com*.
