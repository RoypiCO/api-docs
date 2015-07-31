# Inventory

 1. [List inventory of a buyer](#list-inventory-of-a-buyer)




## List inventory of a buyer

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
            "id": 2611,
            "inventory_item": 727,
            "product_model": {
                "id": 2624,
                "name": "bolivar",
                "product": {
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
                "features": [],
                "min_qty": 13,
                "production_cost": "0.00",
                "price": "1.50",
                "volume": "0.0000",
                "weight": "1.0000",
                "height": "1.00",
                "length": "1.00",
                "width": "1.00",
                "volumetric_weight": "0.0002",
                "status": 0,
                "created": "2014-11-04T20:43:17Z",
                "modified": "2014-11-09T04:45:25Z",
                "complete_data": false,
                "rank": 0,
                "type": 0,
                "code": "00000000MjYyNA==",
                "maximum_order": null,
                "available_in_private": true,
                "available_in_group": true,
                "brand": null,
                "sku": null,
                "minimum_price": null,
                "created_in": 1,
                "original_product": null
            },
            "variant_inventory_item": {
                "id": 521,
                "quantity": 2,
                "additional_cost": "0.00"
            },
            "status": 1,
            "retail_price": "5.40",
            "wholesale_price": "4.80",
            "cost_price": "4.50",
            "quantity": 2,
            "update_url": "http://roypi.com/buyer/inventory/727/",
            "product_update_url": "http://roypi.com/buyer/inventory/product/edit/1513/",
            "favorite_url": null,
            "favorite_icon_class": "icon-ban-circle",
            "container_url": null,
            "container_status": "In Destination",
            "container_icon_class": "icon-ban-circle",
            "image_url": "http://media.roypi.s3.amazonaws.com/pictures/Screen_Shot_2015-06-24_at_10.04.12_PM.png.200x170_q100_crop_key-1_text-small.png",
            "search_url": "http://roypi.com/search/result/0/203/0/0/0/0/0/bolivar",
            "selected": true,
            "favorite_message": "Can't set as Favorite",
            "can_assign": true,
            "origin_manufacturer": false,
            "show_stock_control": 1
        },
        {
            "id": 2612,
            "inventory_item": 891,
            "product_model": {
                "id": 2796,
                "name": "LCD",
                "product": {
                    "id": 1583,
                    "name": "tv",
                    "category": {
                        "id": 1799,
                        "category_name": "Stands de TV"
                    },
                    "sku": null,
                    "created": "2015-03-23T22:31:41Z",
                    "modified": "2015-03-23T22:31:41Z"
                },
                "features": [
                    {
                        "unit": null,
                        "id": 71,
                        "value": "azul",
                        "feature": "Color"
                    }
                ],
                "min_qty": 50,
                "production_cost": "0.00",
                "price": "400.00",
                "volume": "0.0000",
                "weight": "1.0000",
                "height": "1.00",
                "length": "1.00",
                "width": "1.00",
                "volumetric_weight": "0.0002",
                "status": 0,
                "created": "2015-03-23T22:31:41Z",
                "modified": "2015-03-23T22:31:41Z",
                "complete_data": false,
                "rank": 0,
                "type": 0,
                "code": "00000000Mjc5Ng==",
                "maximum_order": null,
                "available_in_private": true,
                "available_in_group": true,
                "brand": null,
                "sku": null,
                "minimum_price": null,
                "created_in": 1,
                "original_product": null
            },
            "variant_inventory_item": {
                "id": 1023,
                "quantity": 46,
                "additional_cost": "0.00"
            },
            "status": 1,
            "retail_price": "480.00",
            "wholesale_price": "440.00",
            "cost_price": "400.00",
            "quantity": 46,
            "update_url": "http://roypi.com/buyer/inventory/891/",
            "product_update_url": "http://roypi.com/buyer/inventory/product/edit/1583/",
            "favorite_url": null,
            "favorite_icon_class": "icon-ban-circle",
            "container_url": null,
            "container_status": "In Destination",
            "container_icon_class": "icon-ban-circle",
            "image_url": "http://static.roypi.s3.amazonaws.com/website/images/icon/default_product.png",
            "search_url": "http://roypi.com/search/result/0/1799/0/0/0/0/0/LCD",
            "selected": true,
            "favorite_message": "Can't set as Favorite",
            "can_assign": true,
            "origin_manufacturer": false,
            "show_stock_control": 1
        },
        {
            "id": 2613,
            "inventory_item": 892,
            "product_model": {
                "id": 2797,
                "name": "PLASMA",
                "product": {
                    "id": 1583,
                    "name": "tv",
                    "category": {
                        "id": 1799,
                        "category_name": "Stands de TV"
                    },
                    "sku": null,
                    "created": "2015-03-23T22:31:41Z",
                    "modified": "2015-03-23T22:31:41Z"
                },
                "features": [],
                "min_qty": 120,
                "production_cost": "0.00",
                "price": "300.00",
                "volume": "0.0000",
                "weight": "1.0000",
                "height": "1.00",
                "length": "1.00",
                "width": "1.00",
                "volumetric_weight": "0.0002",
                "status": 0,
                "created": "2015-03-23T22:31:41Z",
                "modified": "2015-03-23T22:31:41Z",
                "complete_data": false,
                "rank": 0,
                "type": 0,
                "code": "00000000Mjc5Nw==",
                "maximum_order": null,
                "available_in_private": true,
                "available_in_group": true,
                "brand": null,
                "sku": null,
                "minimum_price": null,
                "created_in": 1,
                "original_product": null
            },
            "variant_inventory_item": {
                "id": 1024,
                "quantity": 119,
                "additional_cost": "0.00"
            },
            "status": 1,
            "retail_price": "360.00",
            "wholesale_price": "330.00",
            "cost_price": "300.00",
            "quantity": 119,
            "update_url": "http://roypi.com/buyer/inventory/892/",
            "product_update_url": "http://roypi.com/buyer/inventory/product/edit/1583/",
            "favorite_url": null,
            "favorite_icon_class": "icon-ban-circle",
            "container_url": null,
            "container_status": "In Destination",
            "container_icon_class": "icon-ban-circle",
            "image_url": "http://static.roypi.s3.amazonaws.com/website/images/icon/default_product.png",
            "search_url": "http://roypi.com/search/result/0/1799/0/0/0/0/0/PLASMA",
            "selected": true,
            "favorite_message": "Can't set as Favorite",
            "can_assign": true,
            "origin_manufacturer": false,
            "show_stock_control": 1
        }
    ]
}
```

List inventory that belongs to the current authenticated buyer (owner of requested inventory)
The category name is translated accordingly to current language (only on session)

`GET /buyers/:buyer_id/inventory/`
