---
title: API Reference

toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>
  - <a href='https://github.com/tripit/slate'>Documentation Powered by Slate</a>

includes:
  - sessions
  - trucks
  - errors

search: true
---

<!-- # Introduction

Welcome to the PNG-trucking API! You can use our API to access Trucking API endpoints.

This example API documentation page was created with [Slate](https://github.com/tripit/slate). Feel free to edit it and use it as a base for your own API's documentation.
 -->
# Authentication

> To authorize, use this code:

<!-- ```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
```

```python
import kittn

api = kittn.authorize('meowmeowmeow')
``` -->

```shell
# With shell, you can just pass the correct header with each request
curl "<API_ENDPOINT_HERE>"
  -H "AcessToken: <YOUR_API_TOKEN>"
```
<!-- 
```javascript
const kittn = require('kittn');

let api = kittn.authorize('meowmeowmeow');
```
 -->
> Make sure to replace <YOUR_API_TOKEN> with your API key.

PNG-Trucking uses API keys to allow access to the API. 

PNG-Trucking expects for the API key to be included in all API requests to the server in a header that looks like the following:

`Authorization: <YOUR_API_TOKEN>`

# Users

## Create User

```shell
curl -X POST \
  http://localhost:3000/api/users \
  -F 'resource[email]=foo@pngtrucking.com' \
  -F 'resource[password]=password' \
  -F 'resource[first_name]=foo' \
  -F 'resource[last_name]=bar' \
  -F 'resource[username]=foobar'
```

> The above command returns JSON structured like this:

```json
{
  "id": 5,
  "first_name": "foo",
  "last_name": "bar",
  "email": "foo@pngtrucking.com",
  "username": "foobar",
  "encrypted_password": "$2a$10$egwjxQxyD3UVZuDgOjZrB.jAFbPv.s6vCMDV3EZsTpYE/Fo.sgc3a",
  "is_active": true,
  "created_at": "2017-05-29T17:56:38.761Z",
  "updated_at": "2017-05-29T17:56:38.761Z",
  "is_locked": false,
  "is_deleted": false
}
```

This endpoint creates new user.

### HTTP Request

`GET http://pngtrucking.com/api/users`

### Query Parameters

Parameter | Description
--------- | -----------
email | The email of the user to create (Should be Unique).
password | The password of the user to create.
first_name | The email of the user to create.
last_name | The email of the user to create.
username | The email of the user to create (Should be unique).




<!-- ################### -->



