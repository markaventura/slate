# Sessions

## Create Session

```shell
curl -X POST \
  http://localhost:3000/api/sessions \
  -F 'credentials[email]=foo@pngtrucking.com' \
  -F 'credentials[password]=password'
```

> The above command returns JSON structured like this:

```json
{
  "access_token": "K3zSryrTsYsssgkbVawn5MmxzUoozxX6hUoTJ7Re9wE"
}
```

This endpoint creates new session.

### HTTP Request

`GET http://pngtrucking.com/api/sessions`

### Query Parameters

Parameter | Description
--------- | -----------
email | The email of the user.
password | The password of the user.
