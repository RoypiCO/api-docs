# Stores

  1. [List stores of a buyer](#list-stores-of-a-buyer)




## List stores of a buyer

```http
GET /buyers/380/stores/ HTTP/1.1
Host: api.roypi.com
```
```http
HTTP/1.1 200 OK
Content-Type: application/json

{
    "count": 1,
    "next": null,
    "previous": null,
    "results": [
        {
            "id": 253,
            "name": "test store",
            "priority": 1
        }
    ]
}
```

List stores of an authenticated buyer.

`GET /buyers/:buyer_id/stores/`
