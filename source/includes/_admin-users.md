# Admin users

## [GET] Admin get user list

Admin取得用戶清單

### HTTP Request

`GET https://iecosystem-api.tomyue.cc/api/users?page=1&perPage=10`

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
         "id":1,
         "name":"王大明",
         "email":"yue.kun.ting@gmail.com"
      },
      {
         "id":2,
         "name":"王小明",
         "email":"admin@gmail.com"
      }
   ]
}
```

<!-- -- Admin get user list end-- -->