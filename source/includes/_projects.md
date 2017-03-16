# Projects

## List Projects

```shell
curl \
 -H "Accept: application/json" \
 -H "Authorization: {{token}}" \
 -X GET 'http://{{url}}/v1/Projects'
```
### HTTP Request

`GET http://{{url}}/v1/Projects`

### Response Attributes

Parameter                 | Type   | Default | Description
--------------------------| ------ | ------- | -----------
id                        | string |  -      | Project ID
type                      | string | Project | Object Type
links                     | object | {}      | Related objects
meta                      | object | {}      | Metadata
name                      | string | -       | Name
scm_type                  | string | manual,git,hg,svn | Scm Type
organization              | string | -       | Organization ID      
description               | string |""       | Description       
local_path                | string |""       | Local path
scm_url                   | string |""       | Scm Url
kind                      | string |ansible,terraform| Project kind       
scm_branch                | string |""       | Scm branch  
scm_clean                 | bool   | false    | Scm clean
scm_delete_on_update      | bool   | false    | Scm delete on update
credential                | string |""        |  Credential Id
scm_delete_on_next_update | bool   | false    | Scm delete on next update
scm_update_on_launch      | bool   | false    | Scm update on launch
scm_update_cache_timeout  | int    | -        | Scm update cache timeout
last_job                  | string | ""        | Last job
last_job_run              | Timestamp | -     | UTC timestamp       
last_job_failed           | bool  | false     | Last job failed
has_schedules             | bool  | false     | Has schedules
next_job_run              | Timestamp | -      | UTC timestamp
status                    | string | ""        | Status
last_update_failed        | bool   | false     | Last update failed
last_updated              | Timestamp |-     |  UTC timestamp
created                   | Timestamp |-     |  UTC timestamp
modified                  | Timestamp |-     | UTC timestamp

##  Fetch Project

```shell
curl \
 -H "Accept: application/json" \
 -H "Authorization: {{token}}" \
 -X GET 'http://{{url}}/v1/Projects/{{Project_id}}'
```
### HTTP Request

`GET http://{{url}}/v1/Projects/{{Project_id}}`

### Response Attributes

Parameter                 | Type   | Default | Description
--------------------------| ------ | ------- | -----------
id                        | string |  -      | Project ID
type                      | string | Project | Object Type
links                     | object | {}      | Related objects
meta                      | object | {}      | Metadata
name                      | string | -       | Name
scm_type                  | string | manual,git,hg,svn | Scm Type
organization              | string | -       | Organization ID      
description               | string |""       | Description       
local_path                | string |""       | Local path
scm_url                   | string |""       | Scm Url
kind                      | string |ansible,terraform| Project kind       
scm_branch                | string |""       | Scm branch  
scm_clean                 | bool   | false    | Scm clean
scm_delete_on_update      | bool   | false    | Scm delete on update
credential                | string |""        |  Credential Id
scm_delete_on_next_update | bool   | false     | Scm delete on next update
scm_update_on_launch      | bool   | false     | Scm update on launch
scm_update_cache_timeout  | int    | -        | Scm update cache timeout
last_job                  | string | ""        | Last job
last_job_run              | Timestamp | -     | UTC timestamp       
last_job_failed           | bool  | false     | Last job failed
has_schedules             | bool  | false     | Has schedules
next_job_run              | Timestamp | -      | UTC timestamp
status                    | string | ""        | Status
last_update_failed        | bool   | false     | Last update failed
last_updated              | Timestamp |-     |  UTC timestamp
created                   | Timestamp |-     |  UTC timestamp
modified                  | Timestamp |-     | UTC timestamp

## Create Project

### HTTP Request

`POST http://{{url}}/v1/Projects`

### Request Attributes

Parameter                | Type   | Default | Description
--------- | ------ | ------- | -----------
name                      | string | -       | Name
organization              | string | -       | Organization ID      
description               | string |""       | Description  
scm_type                  | string | manual,git,hg,svn | Scm Type
scm_url                   | string |""       | Scm Url
credential                | string |-        |  Credential Id
scm_branch                | string |""       | Scm branch  
scm_clean                 | bool   | false     | Scm clean
scm_delete_on_update      | bool   | false     | Scm delete on update
scm_delete_on_next_update | bool   | false     | Scm delete on next update
scm_update_on_launch      | bool   | false     | Scm update on launch
scm_update_cache_timeout  | int    | -        | Scm update cache timeout

### Response Attributes

Parameter | Type   | Default | Description
--------- | ------ | ------- | -----------
id                        | string |  -      | Project ID
type                      | string | Project | Object Type
links                     | object | {}      | Related objects
meta                      | object | {}      | Metadata
name                      | string | -       | Name
scm_type                  | string | manual,git,hg,svn | Scm Type
organization              | string | -       | Organization ID      
description               | string |""       | Description       
local_path                | string |""       | Local path
scm_url                   | string |""       | Scm Url
kind                      | string |ansible,terraform| Project kind       
scm_branch                | string |""       | Scm branch  
scm_clean                 | bool   | false     | Scm clean
scm_delete_on_update      | bool   | false     | Scm delete on update
credential                | string |""        |  Credential Id
scm_delete_on_next_update | bool   | false     | Scm delete on next update
scm_update_on_launch      | bool   | false     | Scm update on launch
scm_update_cache_timeout  | int    | -        | Scm update cache timeout
last_job                  | string | ""        | Last job
last_job_run              | Timestamp | -     | UTC timestamp       
last_job_failed           | bool  | false     | Last job failed
has_schedules             | bool  | false     | Has schedules
next_job_run              | Timestamp | -      | UTC timestamp
status                    | string | ""        | Status
last_update_failed        | bool   | false     | Last update failed
last_updated              | Timestamp |-     |  UTC timestamp
created                   | Timestamp |-     |  UTC timestamp
modified                  | Timestamp |-     | UTC timestamp


## Update Project

### HTTP Request

`PUT http://{{url}}/v1/Projects/{{Project_id}}`

### Request Attributes

Parameter | Type   | Default | Description
--------- | ------ | ------- | -----------
name                      | string | -       | Name
organization              | string | -       | Organization ID      
description               | string |""       | Description  
scm_type                  | string | manual,git,hg,svn | Scm Type
scm_url                   | string |""       | Scm Url
credential                | string |-        |  Credential Id
scm_branch                | string |""       | Scm branch  
scm_clean                 | bool   | false     | Scm clean
scm_delete_on_update      | bool   | false     | Scm delete on update
scm_delete_on_next_update | bool   | false     | Scm delete on next update
scm_update_on_launch      | bool   | false     | Scm update on launch
scm_update_cache_timeout  | int    | -        | Scm update cache timeout


### Response Attributes

Parameter | Type   | Default | Description
--------- | ------ | ------- | -----------
id                        | string |  -      | Project ID
type                      | string | Project | Object Type
links                     | object | {}      | Related objects
meta                      | object | {}      | Metadata
name                      | string | -       | Name
scm_type                  | string | manual,git,hg,svn | Scm Type
organization              | string | -       | Organization ID      
description               | string |""       | Description       
local_path                | string |""       | Local path
scm_url                   | string |""       | Scm Url
kind                      | string |ansible,terraform| Project kind       
scm_branch                | string |""       | Scm branch  
scm_clean                 | bool   | false     | Scm clean
scm_delete_on_update      | bool   | false     | Scm delete on update
credential                | string |""        |  Credential Id
scm_delete_on_next_update | bool   | false     | Scm delete on next update
scm_update_on_launch      | bool   | false     | Scm update on launch
scm_update_cache_timeout  | int    | -        | Scm update cache timeout
last_job                  | string | ""        | Last job
last_job_run              | Timestamp | -     | UTC timestamp       
last_job_failed           | bool  | false     | Last job failed
has_schedules             | bool  | false     | Has schedules
next_job_run              | Timestamp | -      | UTC timestamp
status                    | string | ""        | Status
last_update_failed        | bool   | false     | Last update failed
last_updated              | Timestamp |-     |  UTC timestamp
created                   | Timestamp |-     |  UTC timestamp
modified                  | Timestamp |-     | UTC timestamp

## Delete Project

```shell
curl \
 -H "Accept: application/json" \
 -H "Authorization: {{token}}" \
 -X DELETE 'http://{{url}}/v1/Projects/{{Project_id}}'
```
### HTTP Request

`DELETE http://{{url}}/v1/Projects/{{Project_id}}`