# Users

## List Users

```shell
curl \
 -H "Accept: application/json" \
 -H "Authorization: {{token}}" \
 -X GET 'http://{{url}}/v1/users'
```
### HTTP Request

`GET http://{{url}}/v1/users`

### Response Attributes

Parameter | Type   | Default | Description
--------- | ------ | ------- | -----------
id        | string |  -      | User ID
type      | string | user    | Object Type
links     | object | {}      | Related objects
username  | string | -       | Username (unique)
first_name | string | ""     | First name
last_name  | string | ""     | Last name
email      | string | -      | Email (unique)
is_superuser | bool | false  | Root account
is_system_auditor | bool | false | Global read accout
password | string | $encrypted$ | Password
create   | Timestamp | -        | UTC timestamp
modified | Timestamp | -        | UTC timestamp

##  Fetch User

```shell
curl \
 -H "Accept: application/json" \
 -H "Authorization: {{token}}" \
 -X GET 'http://{{url}}/v1/users/{{user_id}}'
```
### HTTP Request

`GET http://{{url}}/v1/users/{{user_id}}`

### Response Attributes

Parameter | Type   | Default | Description
--------- | ------ | ------- | -----------
id        | string |  -      | User ID
type      | string | user    | Object Type
links     | object | {}      | Related objects
username  | string | -       | Username (unique)
first_name | string | ""     | First name
last_name  | string | ""     | Last name
email      | string | -      | Email (unique)
is_superuser | bool | false  | Root account
is_system_auditor | bool | false | Global read account
password | string | $encrypted$ | Password
create   | Timestamp | -        | UTC timestamp
modified | Timestamp | -        | UTC timestamp

## Update User

### HTTP Request

`PUT http://{{url}}/v1/users/{{user_id}}`

### Request Attributes

Parameter | Type   | Default | Description
--------- | ------ | ------- | -----------
username  | string | -       | Username (unique)
first_name | string | ""     | First name
last_name  | string | ""     | Last name
email      | string | -      | Email (unique)
is_superuser | bool | false  | Root account
is_system_auditor | bool | false | Global read account
password | string | $encrypted$ | Password


### Response Attributes

Parameter | Type   | Default | Description
--------- | ------ | ------- | -----------
id        | string |  -      | User ID
type      | string | user    | Object Type
links     | object | {}      | Related objects
username  | string | -       | Username (unique)
first_name | string | ""     | First name
last_name  | string | ""     | Last name
email      | string | -      | Email (unique)
is_superuser | bool | false  | Root account
is_system_auditor | bool | false | Global read account
password | string | $encrypted$ | Password
create   | Timestamp | -        | UTC timestamp
modified | Timestamp | -        | UTC timestamp


## Delete User

```shell
curl \
 -H "Accept: application/json" \
 -H "Authorization: {{token}}" \
 -X DELTE 'http://{{url}}/v1/users/{{user_id}}'
```
### HTTP Request

`DELTE http://{{url}}/v1/users/{{user_id}}`