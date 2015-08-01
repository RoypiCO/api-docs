# Products

 1. [List products of a buyer](#list-products-of-a-buyer)
 2. [List categories](#list-categories)




## List products of a buyer

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

List products that belongs to the current authenticated buyer (owner of requested products)
The category name is translated accordingly to current language (only on session)

`GET /buyers/:buyer_id/products/`




## List categories

```http
GET /categories/ HTTP/1.1
Host: api.roypi.com
```
```http
HTTP/1.1 200 OK
Content-Type: application/json

{
    "count": 33,
    "next": null,
    "previous": null,
    "results": [
        {
            "id": 173,
            "category_name": "Prendas de vestir"
        },
        {
            "id": 271,
            "category_name": "Chaquetas"
        },
        {
            "id": 273,
            "category_name": "Tops/Blusa"
        },
        {
            "id": 1422,
            "category_name": "Accesorio de cabeza"
        },
        {
            "id": 1455,
            "category_name": "Corbata"
        },
        {
            "id": 1456,
            "category_name": "Bufandas & Chales"
        },
        {
            "id": 2517,
            "category_name": "Bolsas de asas"
        },
        {
            "id": 2535,
            "category_name": "Bolsas de mano & Bolsas de Mensajero"
        },
        {
            "id": 2536,
            "category_name": "Bolsos de noche"
        },
        {
            "id": 2537,
            "category_name": "Bolsos de mano"
        },
        {
            "id": 2556,
            "category_name": "Bolsos de compras"
        },
        {
            "id": 2558,
            "category_name": "Mochilas"
        },
        {
            "id": 2569,
            "category_name": "Billeteras"
        },
        {
            "id": 2586,
            "category_name": "Ropa de maquinaría"
        },
        {
            "id": 4372,
            "category_name": "Pulseras & Brazaletes"
        },
        {
            "id": 4373,
            "category_name": "Pendientes"
        },
        {
            "id": 4376,
            "category_name": "Handbags"
        },
        {
            "id": 4390,
            "category_name": "Joyería"
        },
        {
            "id": 4391,
            "category_name": "Bolsas de Embrague"
        },
        {
            "id": 4392,
            "category_name": "Tobilleras"
        },
        {
            "id": 4393,
            "category_name": "Bolsas Cross-body"
        },
        {
            "id": 4396,
            "category_name": "Broches"
        },
        {
            "id": 4397,
            "category_name": "Bolso de Hombro"
        },
        {
            "id": 4400,
            "category_name": "Bolsas Top-Handle"
        },
        {
            "id": 4401,
            "category_name": "Pulseras"
        },
        {
            "id": 4402,
            "category_name": "Carteras"
        },
        {
            "id": 4403,
            "category_name": "Messenger Bags"
        },
        {
            "id": 4414,
            "category_name": "Riñoneras"
        },
        {
            "id": 4415,
            "category_name": "Bolsas de Hobo"
        },
        {
            "id": 4416,
            "category_name": "Cueros"
        },
        {
            "id": 4418,
            "category_name": "Dresses"
        },
        {
            "id": 4509,
            "category_name": "Collar"
        },
        {
            "id": 4530,
            "category_name": "Prensa Térmica"
        }
    ]
}
```

List all categories. The category name is translated accordingly to current language (only on session)

`GET /categories/`
