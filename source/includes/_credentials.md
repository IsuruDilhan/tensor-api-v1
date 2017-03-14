# Credentials

## List Credentials

```shell
curl \
 -H "Accept: application/json" \
 -H "Authorization: {{token}}" \
 -X GET 'http://{{url}}/v1/credentials'
```
### HTTP Request

`GET http://{{url}}/v1/credentials`

### Response Attributes

Parameter   | Type   | Default | Description
----------- | ------ | ------- | -----------
id          | string |  -      | User ID
type        | string | credential    | Object Type
links       | object | {}      | Related objects
meta       | object | {}      | Metadata
name        | string | -       | Name
kind        | string | windows,ssh,net,scm,aws,rax,vmware,gce,azure,openstack | Credential type
cloud       | bool   | false     | Is a cloud credential
description | string | ""      | Description
host        | string | ""  | Host
username    | string | "" | Username
password    | string | $encrypted$ | password
security_token | string | $encrypted$ | security token
project    | string | -        | Project ID
email      | string | ""       | Email
domain     | string | ""       | Domain
ssh_key_data | string | $encrypted$ | SSH key
ssh_key_unlock | string | $encrypted$ | SSH key unlock password
become_method  | string | sudo,su,pburn,pfexec,runas,doas,dzdo | Become method
become_username | string | ""  | Become username
become_password | string | $encrypted$ | Become password
vault_password  | string | $encrypted$ | Vault password
subscription    | string | ""          | Subscription
tenant          | string | ""          | Tenant ID
secret          | string | $encrypted$ | Secret
Client          | string | ""           | Client
authorize       | bool   | false        | Authorize
authorize_password | string | $encrypted$ | Authorize Password
organization    | string | -          | Organization ID
create   | Timestamp | -        | UTC timestamp
modified | Timestamp | -        | UTC timestamp

##  Fetch Credential

```shell
curl \
 -H "Accept: application/json" \
 -H "Authorization: {{token}}" \
 -X GET 'http://{{url}}/v1/credentials/{{credential_id}}'
```
### HTTP Request

`GET http://{{url}}/v1/credentials/{{credential_id}}`

### Response Attributes

Parameter   | Type   | Default | Description
----------- | ------ | ------- | -----------
id          | string |  -      | User ID
type        | string | credential    | Object Type
links       | object | {}      | Related objects
meta       | object | {}      | Metadata
name        | string | -       | Name
kind        | string | windows,ssh,net,scm,aws,rax,vmware,gce,azure,openstack | Credential type
cloud       | bool   | false     | Is a cloud credential
description | string | ""      | Description
host        | string | ""  | Host
username    | string | "" | Username
password    | string | $encrypted$ | password
security_token | string | $encrypted$ | security token
project    | string | -        | Project ID
email      | string | ""       | Email
domain     | string | ""       | Domain
ssh_key_data | string | $encrypted$ | SSH key
ssh_key_unlock | string | $encrypted$ | SSH key unlock password
become_method  | string | sudo,su,pburn,pfexec,runas,doas,dzdo | Become method
become_username | string | ""  | Become username
become_password | string | $encrypted$ | Become password
vault_password  | string | $encrypted$ | Vault password
subscription    | string | ""          | Subscription
tenant          | string | ""          | Tenant ID
secret          | string | $encrypted$ | Secret
Client          | string | ""           | Client
authorize       | bool   | false        | Authorize
authorize_password | string | $encrypted$ | Authorize Password
organization    | string | -          | Organization ID
create   | Timestamp | -        | UTC timestamp
modified | Timestamp | -        | UTC timestamp

## Update Credential

### HTTP Request

`PUT http://{{url}}/v1/credentials/{{credential_id}}`

### Request Attributes

Parameter   | Type   | Default | Description
----------- | ------ | ------- | -----------
name        | string | -       | Name
kind        | string | windows,ssh,net,scm,aws,rax,vmware,gce,azure,openstack | Credential type
cloud       | bool   | false     | Is a cloud credential
description | string | ""      | Description
host        | string | ""  | Host
username    | string | "" | Username
password    | string | $encrypted$ | password
security_token | string | $encrypted$ | security token
project    | string | -        | Project ID
email      | string | ""       | Email
domain     | string | ""       | Domain
ssh_key_data | string | $encrypted$ | SSH key
ssh_key_unlock | string | $encrypted$ | SSH key unlock password
become_method  | string | sudo,su,pburn,pfexec,runas,doas,dzdo | Become method
become_username | string | ""  | Become username
become_password | string | $encrypted$ | Become password
vault_password  | string | $encrypted$ | Vault password
subscription    | string | ""          | Subscription
tenant          | string | ""          | Tenant ID
secret          | string | $encrypted$ | Secret
Client          | string | ""           | Client
authorize       | bool   | false        | Authorize
authorize_password | string | $encrypted$ | Authorize Password
organization    | string | -          | Organization ID


### Response Attributes

Parameter   | Type   | Default | Description
----------- | ------ | ------- | -----------
id          | string |  -      | User ID
type        | string | credential    | Object Type
links       | object | {}      | Related objects
meta       | object | {}      | Metadata
name        | string | -       | Name
kind        | string | windows,ssh,net,scm,aws,rax,vmware,gce,azure,openstack | Credential type
cloud       | bool   | false     | Is a cloud credential
description | string | ""      | Description
host        | string | ""  | Host
username    | string | "" | Username
password    | string | $encrypted$ | password
security_token | string | $encrypted$ | security token
project    | string | -        | Project ID
email      | string | ""       | Email
domain     | string | ""       | Domain
ssh_key_data | string | $encrypted$ | SSH key
ssh_key_unlock | string | $encrypted$ | SSH key unlock password
become_method  | string | sudo,su,pburn,pfexec,runas,doas,dzdo | Become method
become_username | string | ""  | Become username
become_password | string | $encrypted$ | Become password
vault_password  | string | $encrypted$ | Vault password
subscription    | string | ""          | Subscription
tenant          | string | ""          | Tenant ID
secret          | string | $encrypted$ | Secret
Client          | string | ""           | Client
authorize       | bool   | false        | Authorize
authorize_password | string | $encrypted$ | Authorize Password
organization    | string | -          | Organization ID
create   | Timestamp | -        | UTC timestamp
modified | Timestamp | -        | UTC timestamp


## Delete Credential

```shell
curl \
 -H "Accept: application/json" \
 -H "Authorization: {{token}}" \
 -X DELTE 'http://{{url}}/v1/credentials/{{credential_id}}'
```
### HTTP Request

`DELTE http://{{url}}/v1/credentials/{{credential_id}}`