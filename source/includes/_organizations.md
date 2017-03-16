# Organizations

## List Organizations

```shell
curl \
 -H "Accept: application/json" \
 -H "Authorization: {{token}}" \
 -X GET 'http://{{url}}/v1/organizations'
```
### HTTP Request

`GET http://{{url}}/v1/organizations`

### Response Attributes

Parameter | Type   | Default | Description
--------- | ------ | ------- | -----------
id        | string |  -      | Organization ID
type      | string | organization | Object Type
links     | object | {}      | Related objects
meta      | object | {}      | Metadata
name      | string | -       | Name
description | string | ""      | Description
created    | Timestamp | -        | UTC timestamp
modified  | Timestamp | -        | UTC timestamp

##  Fetch Organization

```shell
curl \
 -H "Accept: application/json" \
 -H "Authorization: {{token}}" \
 -X GET 'http://{{url}}/v1/organizations/{{organization_id}}'
```
### HTTP Request

`GET http://{{url}}/v1/organizations/{{organization_id}}`

### Response Attributes

Parameter | Type   | Default | Description
--------- | ------ | ------- | -----------
id        | string |  -      | Organization ID
type      | string | organization | Object Type
links     | object | {}      | Related objects
meta      | object | {}      | Metadata
name      | string | -       | Name
description | string | ""      | Description
created    | Timestamp | -        | UTC timestamp
modified  | Timestamp | -        | UTC timestamp

## Create Organization

### HTTP Request

`POST http://{{url}}/v1/organizations`

### Request Attributes

Parameter | Type   | Default | Description
--------- | ------ | ------- | -----------
name      | string | -       | Name
description | string | ""      | Description

### Response Attributes

Parameter | Type   | Default | Description
--------- | ------ | ------- | -----------
id        | string |  -      | Organization ID
type      | string | organization | Object Type
links     | object | {}      | Related objects
meta      | object | {}      | Metadata
name      | string | -       | Name
description | string | ""      | Description
created    | Timestamp | -        | UTC timestamp
modified  | Timestamp | -        | UTC timestamp



## Update Organization

### HTTP Request

`PUT http://{{url}}/v1/organizations/{{organization_id}}`

### Request Attributes

Parameter | Type   | Default | Description
--------- | ------ | ------- | -----------
name      | string | -       | Name
description | string | ""      | Description

### Response Attributes

Parameter | Type   | Default | Description
--------- | ------ | ------- | -----------
id        | string |  -      | Organization ID
type      | string | organization | Object Type
links     | object | {}      | Related objects
meta      | object | {}      | Metadata
name      | string | -       | Name
description | string | ""      | Description
created    | Timestamp | -        | UTC timestamp
modified  | Timestamp | -        | UTC timestamp


## Delete Organization

```shell
curl \
 -H "Accept: application/json" \
 -H "Authorization: {{token}}" \
 -X DELETE 'http://{{url}}/v1/organizations/{{organization_id}}'
```
### HTTP Request

`DELETE http://{{url}}/v1/organizations/{{organization_id}}`