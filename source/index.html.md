---
title: Tensor API Reference

language_tabs:
  - shell

toc_footers:
  - <a href='https://github.com/pearsonappeng/tensor'>Tensor</a>

includes:
  - users
  - credentials
  - errors
  - organizations
  - projects
  - teams

search: true
---

# Introduction

Welcome to the Tensor API! You can use our API to access Tensor API endpoints.

We have language bindings in Shell, Ruby, and Python! You can view code examples in the dark area to the right, and you can switch the programming language of the examples with the tabs in the top right.

# Authentication

> To authorize, use this code:

```shell
curl \
 -H "Accept: application/json" \
 -H "Content-Type: application/json" \
 -X POST \
 -d '{"username":"{{password}}","password":"{{password}}"}' 'http://{{url}}/v1/authtoken'
```

> Make sure to replace `username` & `password` with your username & password.

Tensor uses JWT token to allow access to the API.

### HTTP Request

`POST http://{{url}}/v1/authtoken`

### Request Attributes

Parameter | Type   | Default | Description
--------- |------- | ------- | -----------
username  | string | ""      | Username is required
password  | string | ""      | Password is required

### Response Attributes

Parameter | Type   | Default | Description
--------- | ------ | ------- | -----------
token     | string |  -      | JWT token

Tensor expects for the API key to be included in all API requests to the server in a header that looks like the following:

`Authorization: token`

## Refresh token

> To get a refresh token, use this code:

```shell
curl \
 -H "Accept: application/json" \
 -H "Authorization: {{token}}" \
 -X GET  'http://{{url}}/v1/authtoken'
```

> Make sure to replace `token` with your JWT token.

### Request Attributes

`GET http://{{url}}/v1/refresh_token`

### Response Attributes

Parameter | Type   | Default | Description
--------- |------- | ------- | -----------
token     | string | -       | JWT token