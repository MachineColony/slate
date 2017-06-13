---
title: Spire-Broker API Reference

language_tabs:
  - shell
  - python

toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>
  - <a href='https://github.com/tripit/slate'>Documentation Powered by Slate</a>

includes:
  - errors

search: true
---

# Introduction

Here is the introduction.

# Authentication

> To authorize, use this code:

```python
```

```shell
# With shell, you can just pass the correct header with each request
curl "api_endpoint_here"
  -H "Authorization: meowmeowmeow"
```

# User Profile

## Update User Profile Picture

```shell
curl -X POST \ 
   -H 'Authorization: ... ' \ 
   -F 'picfile=@profile.jpg' \
   https://spire.machinecolony.com/api/user-profile-picture
```

```python
# python code here
```

> Response

```json
{
  "profile_url": "https://modelsdataprod.s3.amazonaws.com/4ec9f7bf-4bde-4d4e-a318-3396de6992da.py?Signature=llkGq%2FlMFviZ11vXnfTbPViXdVo%3D&Expires=1810954189&AWSAccessKeyId=AKIAIJKB7NL6DXVI46OQ"
}
```

### HTTP Request

`POST https://spire.machinecolony.com/api/user-profile-picture`

### Query Parameters


## Get User Profile
```shell
curl -X GET \
-H 'Authorization: ... ' \
http://spire.machinecolony.com/api/user-profile
```

```python
```

> Response

```json
{
   "top_topic_tags" : [],
   "last_name" : "wang",
   "username" : 'gcwang',
   "email" : "wgcemail@gmail.com",
   "status" : "...",
   "top_broker_tags" : [],
   "first_name" : "guangcheng",
   "profile_url" : "https://modelsdataprod.s3.amazonaws.com/4ec9f7bf-4bde-4d4e-a318-3396de6992da.py?Signature=llkGq%2FlMFviZ11vXnfTbPViXdVo%3D&Expires=1810954189&AWSAccessKeyId=AKIAIJKB7NL6DXVI46OQ",
   "posts_count" : 0,
   "avg_comments_rate" : 0
}
```

### HTTP Request

`GET http://spire.machinecolony.com/api/user-profile`


## Update User Profile
```shell
curl -X PUT \
  -H 'Authorization: ...' \
  -d '{"first_name":"guangcheng", "last_name":"wang"}' \
http://spire.machinecolony.com/api/user-profile
```

```python
```

> Response

```json
{}
```

### HTTP Request
`PUT http://spire.machinecolony.com/api/user-profile`

# Question

## Create Question

```shell
curl -X POST \
  -H 'Authorization: ... ' \
  -d '{"content":"HELLO", "privacy":"public", "tags": ["A", "B", "C"]}' \
  http://spire.machinecolony.com/api/question
```

```python
```

> Response

```json
{}
```

### HTTP Request
`POST http://spire.machinecolony.com/api/question`
