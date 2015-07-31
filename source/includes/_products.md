# Products

 1. [List products of the authenticated buyer](#list-products-of-the-authenticated-buyer)




## List products of the authenticated buyer

```http
GET /buyers/380/clients/ HTTP/1.1
Host: api.roypi.com
```
```http
HTTP/1.1 200 OK
Content-Type: application/json

{
    "count": 2,
    "next": null,
    "previous": null,
    "results": [
        {
            "id": 1513,
            "name": "detergente",
            "category": {
                "id": 203,
                "category_name": "Vestidos de club"
            },
            "sku": null,
            "created": "2014-10-22T20:37:32Z",
            "modified": "2015-04-25T12:51:14Z"
        },
        {
            "id": 1583,
            "name": "tv",
            "category": {
                "id": 1799,
                "category_name": "Stands de TV"
            },
            "sku": null,
            "created": "2015-03-23T22:31:41Z",
            "modified": "2015-03-23T22:31:41Z"
        }
    ]
}
```

List products that belongs to a specific buyer (owner of requested products)
The category name is translated accordingly to current language only on session

`GET /buyers/:buyer_id/products/`
