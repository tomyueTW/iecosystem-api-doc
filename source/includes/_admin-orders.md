## [GET] orders

admin 取得所有orders

### HTTP Request

`GET https://iecosystem-api.tomyue.cc/api/admin/orders?page=1&perPage=10`

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
page | int
perPage | int

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
         "user": "Tom",
         "number": "#2022010500009",
         "created_at": "2022/01/08",
         "order_type_name": "醫療篇",
         "assign": "XX基金會",
         "status": "進行中"
      },
      {
         "id": 1,
         "user": "Tom",
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