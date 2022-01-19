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

## [GET] Order types

問題種類清單

### HTTP Request

`GET https://iecosystem-api.tomyue.cc/api/orders/types`

> Request body:

```json
{

}
```

 - Header Parameter

Parameter | Default | Description
--------- | ------- | -----------

 - Query Parameters

Parameter | Default | Description
--------- | ------- | -----------

 - Body Parameter

Parameter | Default | Description
--------- | ------- | -----------



### HTTP Response

> Response:

```json
{
   "message": "成功",
   "data": [
      {
         "id": 1,
         "name": "法律篇"
      },
      {
         "id": 2,
         "name": "醫療篇"
      },
      {
         "id": 3,
         "name": "經濟篇"
      }
   ]
}
```

<!-- -- Order types end-- -->

## [GET] User orders

歷程總覽

### HTTP Request

`GET https://iecosystem-api.tomyue.cc/api/orders`

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

 - Body Parameter

Parameter | Default | Description
--------- | ------- | -----------



### HTTP Response

> Response:

```json
{
   "message": "成功",
   "data": [
      {
         "id": 2,
         "number": "#2022010500009",
         "created_at": "2022/01/08",
         "order_type_name": "醫療篇",
         "assign": "XX基金會",
         "status": "進行中"
      },
      {
         "id": 1,
         "number": "#2022010500008",
         "created_at": "2022/01/07",
         "order_type_name": "法律篇",
         "assign": "XX基金會",
         "status": "已結束"
      },
   ]
}
```

<!-- -- User orders end-- -->