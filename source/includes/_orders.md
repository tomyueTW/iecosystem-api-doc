# Orders

## [POST] User close order

User關閉聊聊

### HTTP Request

`POST https://iecosystem-api.tomyue.cc/api/orders/{orderId}/close`

> Request body:

```json
{

}
```

 - Header Parameter

Parameter | Default | Description
--------- | ------- | -----------
Authorization | string | Bearer {TOKEN}

 - Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
orderId | int | 

 - Body Parameter

Parameter | Default | Description
--------- | ------- | -----------



### HTTP Response

> Response:

```json
{
   "message":"Successful.",
   "data":{
      "id":4,
      "user_id":25,
      "number":"#2021102800001",
      "status":2,
      "assign_id":26,
      "created_at":"2021-10-28 14:10:58",
      "updated_at":"2021-10-28 16:10:52"
   }
}
```

<!-- -- User store messages [localStorage] end-- -->