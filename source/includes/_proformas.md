# Proformas

 1. [List proformas of a buyer](#list-proformas-of-a-buyer)
 2. [Create a proforma for a buyer](#create-a-proforma-for-a-buyer)




## List proformas of a buyer

```http
GET /buyers/380/proformas/ HTTP/1.1
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
            "id": 112,
            "created": "2015-01-06T00:00:00Z",
            "proforma_type": 1,
            "client": {
                "id": 684,
                "name": "George",
                "email": "hi.geoom@gmail.com",
                "created": "2015-01-07T02:01:08Z",
                "modified": "2015-04-22T00:59:13Z"
            },
            "store": {
                "id": 253,
                "name": "test store",
                "priority": 1,
                "latlng": null,
                "city": null,
                "state": null,
                "country": null,
                "status": 1,
                "default": 1,
                "visible_in_api": false,
                "created": "2014-06-18T19:24:07Z",
                "modified": "2014-06-18T19:24:07Z",
                "buyer": 380
            },
            "currency": {
                "id": 1,
                "symbol": "$",
                "code": "USD",
                "status": 1
            },
            "items": [
                {
                    "variant": 521,
                    "quantity": 1,
                    "price": "1.80"
                }
            ]
        },
        {
            "id": 113,
            "created": "2015-01-20T00:00:00Z",
            "proforma_type": 1,
            "client": {
                "id": 684,
                "name": "George",
                "email": "hi.geoom@gmail.com",
                "created": "2015-01-07T02:01:08Z",
                "modified": "2015-04-22T00:59:13Z"
            },
            "store": {
                "id": 253,
                "name": "test store",
                "priority": 1,
                "latlng": null,
                "city": null,
                "state": null,
                "country": null,
                "status": 1,
                "default": 1,
                "visible_in_api": false,
                "created": "2014-06-18T19:24:07Z",
                "modified": "2014-06-18T19:24:07Z",
                "buyer": 380
            },
            "currency": {
                "id": 1,
                "symbol": "$",
                "code": "USD",
                "status": 1
            },
            "items": [
                {
                    "variant": 521,
                    "quantity": 1,
                    "price": "1.80"
                }
            ]
        },
        {
            "id": 463,
            "created": "2015-04-22T00:00:00Z",
            "proforma_type": 1,
            "client": {
                "id": 684,
                "name": "George",
                "email": "hi.geoom@gmail.com",
                "created": "2015-01-07T02:01:08Z",
                "modified": "2015-04-22T00:59:13Z"
            },
            "store": {
                "id": 253,
                "name": "test store",
                "priority": 1,
                "latlng": null,
                "city": null,
                "state": null,
                "country": null,
                "status": 1,
                "default": 1,
                "visible_in_api": false,
                "created": "2014-06-18T19:24:07Z",
                "modified": "2014-06-18T19:24:07Z",
                "buyer": 380
            },
            "currency": {
                "id": 6,
                "symbol": "S/.",
                "code": "PEN",
                "status": 2
            },
            "items": [
                {
                    "variant": 1023,
                    "quantity": 1,
                    "price": "480.00"
                }
            ]
        }
    ]
}
```

List proformas of the authenticated buyer.

`GET /buyers/:buyer_id/proformas/`




## Create a proforma for a buyer

```http
POST /buyers/380/proformas/ HTTP/1.1
Host: api.roypi.com
Content-Type: application/json; charset=utf-8

{"created": "2011-04-14T16:00:00-05:00", "items": [{"variant": 1, "quantity": 5392, "price": "717.09"}], "currency": 2, "proforma_type": 1, "client": 2, "store": 1}
```
```http
HTTP/1.1 201 CREATED
Content-Type: application/json

{
    "created": "2011-04-14T16:00:00-05:00",
    "items":[
        {
            "variant":1,
            "quantity":5392,
            "price":"717.09"
        }
    ],
    "currency": 2,
    "proforma_type": 1,
    "client": 2,
    "store": 1
}
```

Create a proforma with items for the authenticated buyer.

`GET /buyers/:buyer_id/proformas/`

### Input

Name | Type | Description
---- | ---- | -----------
created | string | Datetime of creation, this field uses a strict format like 2011-04-14T16:00 (ISO 8601 format) - **Required**.
proforma_type | integer | Type may be 1 for `retail` or 2 for `wholesale` - **Required**.
client | integer | Client id - **Required**.
store | integer | Store id - **Required**.
currency | integer | Currency id - **Required**.
items | array | Items with fields: variant (integer: variant id), price (string: item price as decimal format) and quantity (integer: item quantity) - **Required**.

