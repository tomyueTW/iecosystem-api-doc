# Admin messages

## [POST] Admin post messages to user

Admin發送訊息給用戶

### HTTP Request

`POST https://iecosystem-api.tomyue.cc/api/users/{userId}/messages`

> Request body:

```json
{
  "body": "Hello, I'm iEcosystem admin."
}
```

 - Header Parameter

Parameter | Default | Description
--------- | ------- | -----------
Authorization | string | Bearer {TOKEN}

 - Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
userId | int | 

 - Body Parameter

Parameter | Default | Description
--------- | ------- | -----------
body     | string   |


### HTTP Response

> Response:

```json
{
   "message":"Successful.",
   "data":{
      "id":31,
      "order_id":4,
      "user_id":26,
      "body":"Hello, I'm iEcosystem admin.",
      "created_at":"2021-10-28 15:10:08",
      "updated_at":"2021-10-28 15:10:08"
   }
}
```

<!-- -- Admin post messages to user end-- -->

## [GET] Admin get messages from user

Admin取得用戶訊息

### HTTP Request

`GET https://iecosystem-api.tomyue.cc/api/users/{userId}/messages?page=1&perPage=10&sort=desc`

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
pages | int | 分頁頁數
perPage | int | 分頁筆數
sort | string | ['asc', 'desc']

 - Body Parameter

Parameter | Default | Description
--------- | ------- | -----------



### HTTP Response

> Response:

```json
{
	"message":"Successful.",
	"data": [
      {
         "id": 3,
         "body": "Hello, I'm Tom3.",
         "create_at": "2021-10-28 10:00:00",
         "user_id": 2,
      },
      {
         "id": 2,
         "body": "Hello, I'm Tom2.",
         "create_at": "2021-10-28 09:00:00",
         "user_id": 2,
      },
		{
			"id": 1,
			"body": "Hello, I'm Tom1.",
			"create_at": "2021-10-28 08:00:00",
			"user_id": 2,
		}
	]
}
```

<!-- -- Admin post messages to user end-- -->

## [POST] Admin assign order

Admin指派

### HTTP Request

`POST https://iecosystem-api.tomyue.cc/api/orders/{orderId}/assign`

> Request body:

```json
{
  "user_id": 3
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
user_id | int | 


### HTTP Response

> Response:

```json
{
   "message":"Successful.",
   "data":{
      "id":4,
      "user_id":25,
      "number":"#2021102800001",
      "status":0,
      "assign_id":3,
      "created_at":"2021-10-28 14:10:58",
      "updated_at":"2021-10-28 15:10:47"
   }
}
```

<!-- -- Admin assign order end-- -->

## [GET] Admin get order list

Admin取得自己被指派的order

### HTTP Request

`GET https://iecosystem-api.tomyue.cc/api/orders/assign`

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
   "message":"Successful.",
   "data":[
      {
         "id":4,
         "user_id":25,
         "number":"#2021102800001",
         "status":0,
         "assign_id":26,
         "created_at":"2021-10-28 14:10:58",
         "updated_at":"2021-10-28 15:10:47"
      }
   ]
}
```

<!-- -- Admin get order list end-- -->

## [GET] Admin get orders messages

Admin取得自己被指派order的訊息

### HTTP Request

`GET https://iecosystem-api.tomyue.cc/api/orders/{orderId}/messages?page=1&perPage=10`

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
pages | int | 分頁頁數
perPage | int | 分頁筆數

 - Body Parameter

Parameter | Default | Description
--------- | ------- | -----------


### HTTP Response

> Response:

```json
{
   "message":"Successful.",
   "data":[
      {
         "id":3,
         "user_id":25,
         "body":"123",
         "created_at":"2021-10-28 14:10:18"
      },
      {
         "id":4,
         "user_id":25,
         "body":"你好",
         "created_at":"2021-10-28 14:10:43"
      }
   ]
}
```

<!-- -- Admin get order list end-- -->