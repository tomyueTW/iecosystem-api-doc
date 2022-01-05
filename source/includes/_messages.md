# Messages

## [POST] User store messages [localStorage]

發送`localStorage`裡的資訊

### HTTP Request

`POST https://iecosystem-api.tomyue.cc/api/messages/storage`

> Request body:

```json
{
  "body": [
    "Hello, I'm Tom1.",
    "Hello, I'm Tom2.",
    "Hello, I'm Tom3.",
  ]
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
body     | array   |


### HTTP Response

> Response:

```json
{
   "message":"Successful.",
   "data":[
      {
         "id":29,
         "order_id":4,
         "user_id":25,
         "body":"Hello, I'm Tom1.",
         "created_at":"2021-10-28 15:10:59",
         "updated_at":"2021-10-28 15:10:59"
      },
      {
         "id":30,
         "order_id":4,
         "user_id":25,
         "body":"Hello, I'm Tom2.",
         "created_at":"2021-10-28 15:10:59",
         "updated_at":"2021-10-28 15:10:59"
      }
   ]
}
```

<!-- -- User store messages [localStorage] end-- -->

## [GET] User get message history

取得歷史紀錄

### HTTP Request

`GET https://iecosystem-api.tomyue.cc/api/messages?page=2&perPage=2&sort=desc`

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
page | int | 
perPage | int |
sort | string | ['asc', 'desc']

 - Body Parameter

Parameter | Default | Description
--------- | ------- | -----------
body     | array   |


### HTTP Response

> Response:

```json
{
   "message":"Successful.",
   "data":[
      {
         "id":4,
         "user_id":25,
         "body":"你好",
         "created_at":"2021-10-28 14:10:43"
      },
      {
         "id":3,
         "user_id":25,
         "body":"123",
         "created_at":"2021-10-28 14:10:18"
      }
   ]
}
```

<!-- -- User get message history end-- -->

## [POST] User post messages to admin

發訊息

### HTTP Request

`POST https://iecosystem-api.tomyue.cc/api/messages`

> Request body:

```json
{
  "body": "Hello, I'm Tom."
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
body     | string   |


### HTTP Response

> Response:

```json
{
   "message":"Successful.",
   "data":{
      "id":28,
      "order_id":4,
      "user_id":25,
      "body":"Hello, I'm Tom.",
      "created_at":"2021-10-28 15:10:56",
      "updated_at":"2021-10-28 15:10:56"
   }
}
```

<!-- -- User post messages to admin end-- -->