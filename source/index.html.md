---
title: Tensor API Reference

language_tabs:
  - shell

toc_footers:
  - <a href='https://github.com/pearsonappeng/tensor'>Tensor</a>

includes:
  - errors

search: false
---

# Introduction

Welcome to the Tensor API! You can use our API to access Tensor API endpoints.

We have language bindings in Shell, Ruby, and Python! You can view code examples in the dark area to the right, and you can switch the programming language of the examples with the tabs in the top right.

# Authentication

> To authorize, use this code:

```shell
curl 
 -H "Accept: application/json"
 -H "Content-Type: application/json"
 -X POST 
 -d '{"username":"example","password":"example"}' http://{{url}}/v1/authtoken
```

> Make sure to replace `username` & `password` with your username & password.

Tensor uses JWT token to allow access to the API.

### HTTP Request

`GET http://{{url}}/v1/authtoken`

### Request Body

Parameter | Default | Description
--------- | ------- | -----------
username | "" | Username is required
password | "" | Password is required

### Response Body

Parameter | Description
--------- | -----------
token | Username is required

Tensor expects for the API key to be included in all API requests to the server in a header that looks like the following:

`Authorization: token`