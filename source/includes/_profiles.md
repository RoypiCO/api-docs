# Profiles

 1. [Create a account (Signup)](#create-an-account-signup)
 2. [Get a buyer](#get-a-buyer)
 3. [Get a supplier](#get-a-supplier)




## Create an account (Signup)

```http
POST /auth/signup/ HTTP/1.1
Host: api.roypi.com
Content-Type: application/json

{"email": "juanito@email.com", "profile": "buyer"}
```
```http
HTTP/1.1 201 CREATED
Content-Type: application/json

{
    "token":"eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VybmFtZSI6ImljZnVucnItUWs2NWdETjA3ZUtEVUE9PSIsIm9yaWdfaWF0IjoxNDM4MzY4NzM0LCJ1c2VyX2lkIjoxMTY2LCJlbWFpbCI6Imp1YW5pdG9AZW1haWwuY29tIiwiZXhwIjoxNDM4ODAwNzM0fQ.YP79INmuHzkfxFpTJS2bsA5xQhDPkmEWntG5djNJZ2c",
    "expires_in":"2015-08-05T18:52:14.310Z",
    "user":{
        "username":"icfunrr-Qk65gDN07eKDUA==",
        "id":1166
    }
}
```

Create a buyer or supplier

`POST /auth/signup/`

### Input

Name | Type | Description
---- | ---- | -----------
profile | string | Type of profile. Can be `buyer` or `supplier` - **Required**.
email | string | The email for a new account with an strict format of email like *foo@email.com* - **Required**.




## Get a buyer

```http
GET /buyers/380/ HTTP/1.1
Host: api.roypi.com
```
```http
HTTP/1.1 200 OK
Content-Type: application/json

{
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
}
```

Get any buyer.

`GET /buyers/:buyer_id/`



## Get a supplier

```http
GET /supplier/849/ HTTP/1.1
Host: api.roypi.com
```
```http
HTTP/1.1 200 OK
Content-Type: application/json

{
    "id": 849,
    "manufacturing": 1,
    "name": "",
    "key": "",
    "is_active": false,
    "created": "2014-06-18T19:24:07Z",
    "modified": "2014-06-18T19:24:07Z",
    "status": 3,
    "legal_address": null,
    "factory_address": null,
    "contact_name": null,
    "contact_phone_country_code": null,
    "contact_phone": null,
    "contact_phone_type": 1,
    "unpublishing_date": null,
    "type_publication": 1,
    "type_price_product": 4,
    "exporter_name": null,
    "bic_number": null,
    "customized_boxes": false,
    "customized_labels": false,
    "logo": null,
    "logo_thumb": null,
    "sample_price_factor": 3,
    "local_price_product_include": 0,
    "filled_basic_information": 0,
    "subdomain": null,
    "available_for_designers": false,
    "mail_chimp_access_token": null,
    "survey_monkey_access_token": null,
    "country": null,
    "state": null,
    "city": null,
    "letterhead": null,
    "bic_document": null,
    "destinations": []
}
```

Get any supplier.

`GET /supplier/:supplier_id/`
