# Teams

## List Teams

```shell
curl \
 -H "Accept: application/json" \
 -H "Authorization: {{token}}" \
 -X GET 'http://{{url}}/v1/Teams'
```
### HTTP Request

`GET http://{{url}}/v1/Teams`

### Response Attributes

Parameter | Type   | Default | Description
--------- | ------ | ------- | -----------
id        | string |  -      | Team ID
type      | string | Team | Object Type
links     | object | {}      | Related objects
meta      | object | {}      | Metadata
name      | string | -       | Name
organization_id    | string | -       | Organization ID
description | string | ""      | Description
created    | Timestamp | -        | UTC timestamp
modified  | Timestamp | -        | UTC timestamp

##  Fetch Team

```shell
curl \
 -H "Accept: application/json" \
 -H "Authorization: {{token}}" \
 -X GET 'http://{{url}}/v1/Teams/{{Team_id}}'
```
### HTTP Request

`GET http://{{url}}/v1/Teams/{{Team_id}}`

### Response Attributes

Parameter | Type   | Default | Description
--------- | ------ | ------- | -----------
id        | string |  -      | Team ID
type      | string | Team | Object Type
links     | object | {}      | Related objects
meta      | object | {}      | Metadata
name      | string | -       | Name
organization_id    | string | -       | Organization ID
description | string | ""      | Description
created    | Timestamp | -        | UTC timestamp
modified  | Timestamp | -        | UTC timestamp


## Create Team

### HTTP Request

`POST http://{{url}}/v1/Teams`

### Request Attributes

Parameter | Type   | Default | Description
--------- | ------ | ------- | -----------
name      | string | -       | Name
description | string | ""      | Description
organization| string | -       | Organization ID

### Response Attributes

Parameter | Type   | Default | Description
--------- | ------ | ------- | -----------
id        | string |  -      | Team ID
type      | string | Team | Object Type
links     | object | {}      | Related objects
meta      | object | {}      | Metadata
name      | string | -       | Name
organization_id    | string | -       | Organization ID
description | string | ""      | Description
created    | Timestamp | -        | UTC timestamp
modified  | Timestamp | -        | UTC timestamp



## Update Team

### HTTP Request

`PUT http://{{url}}/v1/Teams/{{Team_id}}`

### Request Attributes

Parameter | Type   | Default | Description
--------- | ------ | ------- | -----------
name      | string | -       | Name
description | string | ""      | Description
organization| string | -       | Organization ID


### Response Attributes

Parameter | Type   | Default | Description
--------- | ------ | ------- | -----------
id        | string |  -      | Team ID
type      | string | Team | Object Type
links     | object | {}      | Related objects
meta      | object | {}      | Metadata
name      | string | -       | Name
organization_id    | string | -       | Organization ID
description | string | ""      | Description
created    | Timestamp | -        | UTC timestamp
modified  | Timestamp | -        | UTC timestamp


## Delete Team

```shell
curl \
 -H "Accept: application/json" \
 -H "Authorization: {{token}}" \
 -X DELETE 'http://{{url}}/v1/Teams/{{Team_id}}'
```
### HTTP Request

`DELETE http://{{url}}/v1/Teams/{{Team_id}}`