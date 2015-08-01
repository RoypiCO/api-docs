# Invoices

 1. [List invoices of a buyer](#list-invoices-of-a-buyer)




## List invoices of a buyer

```http
GET /buyers/380/inventory/ HTTP/1.1
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
            "id": 880,
            "buyer": {
                "id": 380,
                "company_name": "Nayra INC",
                "contact_name": "contacto nayra",
                "telephone": "455566743",
                "address": "Las Palmeras",
                "logo": "http://media.roypi.s3.amazonaws.com/buyer/logo/Screen_Shot_2015-04-15_at_2.32.11_AM.png",
                "logo_thumb": "http://media.roypi.s3.amazonaws.com/buyer/logo/download.thumbnail.jpeg",
                "country": 2,
                "state": 180,
                "city": 32824,
                "current_currency": 6,
                "created": "2014-06-18T19:24:07Z",
                "modified": "2015-04-22T00:58:59Z"
            },
            "client": {
                "id": 11,
                "name": "Gean Carlos",
                "email": "rivaspahuachogeancarlo@gmail.com",
                "created": "2013-08-05T23:28:10Z",
                "modified": "2014-11-09T11:34:32Z"
            },
            "sale_type": 1,
            "order": 1,
            "currency": {
                "id": 1,
                "symbol": "$",
                "code": "USD",
                "status": 1
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
            "items": [
                {
                    "quantity": 1,
                    "price": "1.80"
                }
            ],
            "total": "1.80",
            "created": "2014-11-09T00:00:00Z",
            "modified": "2014-11-09T11:34:32Z"
        },
        {
            "id": 952,
            "buyer": {
                "id": 380,
                "company_name": "Nayra INC",
                "contact_name": "contacto nayra",
                "telephone": "455566743",
                "address": "Las Palmeras",
                "logo": "http://media.roypi.s3.amazonaws.com/buyer/logo/Screen_Shot_2015-04-15_at_2.32.11_AM.png",
                "logo_thumb": "http://media.roypi.s3.amazonaws.com/buyer/logo/download.thumbnail.jpeg",
                "country": 2,
                "state": 180,
                "city": 32824,
                "current_currency": 6,
                "created": "2014-06-18T19:24:07Z",
                "modified": "2015-04-22T00:58:59Z"
            },
            "client": {
                "id": 684,
                "name": "George",
                "email": "hi.geoom@gmail.com",
                "created": "2015-01-07T02:01:08Z",
                "modified": "2015-04-22T00:59:13Z"
            },
            "sale_type": 1,
            "order": 2,
            "currency": {
                "id": 1,
                "symbol": "$",
                "code": "USD",
                "status": 1
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
            "items": [
                {
                    "quantity": 1,
                    "price": "1.80"
                }
            ],
            "total": "1.80",
            "created": "2015-02-03T00:00:00Z",
            "modified": "2015-02-02T22:03:03Z"
        },
        {
            "id": 953,
            "buyer": {
                "id": 380,
                "company_name": "Nayra INC",
                "contact_name": "contacto nayra",
                "telephone": "455566743",
                "address": "Las Palmeras",
                "logo": "http://media.roypi.s3.amazonaws.com/buyer/logo/Screen_Shot_2015-04-15_at_2.32.11_AM.png",
                "logo_thumb": "http://media.roypi.s3.amazonaws.com/buyer/logo/download.thumbnail.jpeg",
                "country": 2,
                "state": 180,
                "city": 32824,
                "current_currency": 6,
                "created": "2014-06-18T19:24:07Z",
                "modified": "2015-04-22T00:58:59Z"
            },
            "client": {
                "id": 684,
                "name": "George",
                "email": "hi.geoom@gmail.com",
                "created": "2015-01-07T02:01:08Z",
                "modified": "2015-04-22T00:59:13Z"
            },
            "sale_type": 2,
            "order": 3,
            "currency": {
                "id": 1,
                "symbol": "$",
                "code": "USD",
                "status": 1
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
            "items": [
                {
                    "quantity": 8,
                    "price": "12.80"
                }
            ],
            "total": "12.80",
            "created": "2015-02-03T00:00:00Z",
            "modified": "2015-02-02T22:03:47Z"
        }
    ]
}
```

List invoices that belongs to the current authenticated buyer.

`GET /buyers/:buyer_id/invoices/`
