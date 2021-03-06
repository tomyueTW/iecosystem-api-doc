# Authentication

## Register

Register the member.

### HTTP Request

`POST https://iecosystem-api.tomyue.cc/api/register`

> Request body:

```json
{
  "email":"tomyue@com.tw",
  "email_confirmation":"tomyue@com.tw",
  "password":"1234567",
  "name":"王大明",
  "account":"a0007",
  "password_confirmation":"1234567",
  "gender":"female",
  "birthday":"2000-07-09",
  "city":"台北"
}
```

 - Query Parameters

Parameter | Default | Description
--------- | ------- | -----------

 - Body Parameter

Parameter | Default | Description
--------- | ------- | -----------
email     | eamil   |
email_confirmation     | eamil   |
password     | string   |
password_confirmation     | string   |
name     | string   |
account     | string   |
gender     | string   | ['male', 'female', 'other']
birthday     | date   |
city     | string   |


### HTTP Response

> Response:

```json
{
  "user":{
    "name":"王大明",
    "email":"tomyue@com.tw",
    "account":"a0007",
    "gender":"female",
    "birthday":"2000-07-09",
    "city":"台北",
    "updated_at":"2021-10-24T12:20:12.000000Z",
    "created_at":"2021-10-24T12:20:12.000000Z",
    "id":13
  },
  "token":"8|qo5nShLeqvl1QhpaGqOLZxbEn5RyVL1jyfFu7R13"
}
```

<!-- -- Register end-- -->

## Login

Login the system.

### HTTP Request

`POST https://iecosystem-api.tomyue.cc/api/login`

> Request body:

```json
{
  "email":"tomyue@com.tw",
  "password":"1234567"
}
```

 - Query Parameters

Parameter | Default | Description
--------- | ------- | -----------

 - Body Parameter

Parameter | Default | Description
--------- | ------- | -----------
email     | eamil   |
password     | string   |


### HTTP Response

> Response:

```json
{
  "user":{
    "name":"王大明",
    "email":"tomyue@com.tw",
    "account":"a0007",
    "gender":"female",
    "birthday":"2000-07-09",
    "city":"台北",
    "updated_at":"2021-10-24T12:20:12.000000Z",
    "created_at":"2021-10-24T12:20:12.000000Z",
    "id":13
  },
  "token":"8|qo5nShLeqvl1QhpaGqOLZxbEn5RyVL1jyfFu7R13"
}
```

<!-- -- Login end-- -->

## Get user profile

Get user profile

### HTTP Request

`GET https://iecosystem-api.tomyue.cc/api/user`

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
  "user":{
    "name":"王大明",
    "email":"tomyue@com.tw",
    "account":"a0007",
    "gender":"female",
    "birthday":"2000-07-09",
    "city":"台北",
    "updated_at":"2021-10-24T12:20:12.000000Z",
    "created_at":"2021-10-24T12:20:12.000000Z",
    "id":13
  },
  "token":"8|qo5nShLeqvl1QhpaGqOLZxbEn5RyVL1jyfFu7R13"
}
```

<!-- -- Get user profile end-- -->

## Reset password

### HTTP Request

`POST https://iecosystem-api.tomyue.cc/api/user/reset-password`

> Request body:

```json
{
  "password":"1234567",
  "password_confirmation":"1234567"
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
password | string | 
password_confirmation | string | 

### HTTP Response

> Response:

```json
{
    "message":"Change password successful"
}
```

<!-- -- Logout end-- -->

## Logout

### HTTP Request

`POST https://iecosystem-api.tomyue.cc/api/logout`

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
    "message": "Tokens Revoked"
}
```

<!-- -- Logout end-- -->

## Facebook login

### HTTP Request

`GET https://iecosystem-api.tomyue.cc/api/facebook/auth`

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
  "user":{
    "id":2,
    "name":"李大明",
    "email":"hello@yahoo.com.tw",
    "email_verified_at":"2021-10-26T05:08:55.000000Z",
    "created_at":"2021-10-24T10:17:20.000000Z",
    "updated_at":"2021-10-26T05:08:55.000000Z",
    "account":null,
    "gender":null,
    "birthday":null,
    "city":null
  },
  "token":"24|nIebgseVZFzVGKmSrpab00BgpFlY6mU19JFgy7dL"
}
```

<!-- -- Facebook login end-- -->

## Edit user profile

Edit user profile

### HTTP Request

`POST https://iecosystem-api.tomyue.cc/api/user/profile`

> Request body:

```json
{
   "name":"1236",
   "gender":"other",
   "birthday":"2020-1-1",
   "city":"台中",
   "password":"123456",
   "password_confirmation":"123456"
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
password | string
name | string
gender | string   | ['male', 'female', 'other']
birthday | date
city | string

### HTTP Response

> Response:

```json
{
   "user":{
      "id":32,
      "name":"1236",
      "email":"admin5@gmail.com",
      "email_verified_at":null,
      "created_at":"2021-12-25 00:12:34",
      "updated_at":"2021-12-25 10:12:35",
      "account":null,
      "gender":"other",
      "birthday":"2020-01-01",
      "city":"台北"
   },
   "success":true
}
```

<!-- -- Edit user profile end-- -->

## Forgot password

Forgot password

### HTTP Request

`POST https://iecosystem-api.tomyue.cc/api/forgot-password`

> Request body:

```json
{
   "email":"test@gmail.com"
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
email | email

### HTTP Response

> Response:

```json
{
   "message": "密碼重設郵件已發送！",
   "success":true
}
```

<!-- -- Forgot password end-- -->

## Reset password

Reset password

### HTTP Request

`POST https://iecosystem-api.tomyue.cc/api/reset-password`

> Request body:

```json
{
   "token": "38a2dwovmvepkwepvmewwekve08aba7fb032d37056",
   "email": "test@gmail.com",
   "password": "123456",
   "password_confirmation": "123456"
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
token | string
email | email
password | string
password_confirmation | string

### HTTP Response

> Response:

```json
{
   "message": "密碼已成功重設！",
   "success":true
}
```

<!-- -- Reset password end-- -->