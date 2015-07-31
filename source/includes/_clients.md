# Clients

 1. [List clients](#list-clients)
 2. [Get a client](#get-a-client)
 3. [List clients of a buyer](#list-clients-of-a-buyer)
 4. [Create a client for a buyer](#create-a-client-for-a-buyer)




## List clients

```http
GET /clients/ HTTP/1.1
Host: api.roypi.com
```
```http
HTTP/1.1 200 OK
Content-Type: application/json

{
    "count": 1707,
    "next": "http://api.roypi.com/clients/?page=2",
    "previous": null,
    "results": [
        {
            "id": 1,
            "name": "gustavo",
            "email": "email@email.email",
            "created": "2013-07-19T05:00:00Z",
            "modified": "2013-07-19T05:00:00Z"
        },
        {
            "id": 2,
            "name": "Client 1",
            "email": "email@email.email",
            "created": "2013-07-19T05:00:00Z",
            "modified": "2013-07-19T05:00:00Z"
        },
        {
            "id": 3,
            "name": "chris",
            "email": "email@email.email",
            "created": "2013-07-19T05:00:00Z",
            "modified": "2013-07-19T05:00:00Z"
        },

        ...

        {
            "id": 100,
            "name": "Oscar Luis Nolasco Marcelo",
            "email": "intex.maquinarias@gmail.com",
            "created": "2014-04-16T18:36:26Z",
            "modified": "2014-04-16T18:36:26Z"
        }
    ]
}
```

Anyone can list clients

`POST /clients/`




## Get a client

```http
GET /clients/456/ HTTP/1.1
Host: api.roypi.com
```
```http
HTTP/1.1 200 OK
Content-Type: application/json

{
    "id": 456,
    "name": "jonathan test",
    "email": "test address",
    "created": "2014-07-08T00:50:48Z",
    "modified": "2014-07-08T00:50:48Z"
}
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
Content-Type: application/json; charset=utf-8
Authorization: Token <YOUR_TOKEN>

{ "name": "juanito", "email": "juanito@email.com" }
```
```http
HTTP/1.1 201 CREATED
Content-Type: application/json

{
    "id":1738,
    "name":"juanito",
    "email":"juanito@email.com",
    "created":"2015-07-31T18:04:28.558834Z",
    "modified":"2015-07-31T18:04:28.558865Z"
}
```

Only an authenticated buyer can create a new client for itself

`POST /buyers/:buyer_id/clients/`

### Input

Name | Type | Description
---- | ---- | -----------
name | string | The name for a new client - **Required**.
email | string | The unique email for a new client with an strict format of email like *foo@email.com*.
