---
title: Tangent MicroServices

language_tabs:
  - shell
  - ruby
  - python
  - javascript

toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>
  - <a href='https://github.com/tripit/slate'>Documentation Powered by Slate</a>

includes:
  - projectservice
  - kittens
  - errors

search: true
---

# Introduction

Welcome to the Tangent MicroServices&trade; project. This is a MicroService eco-system aiming to provide useful services for managing a small company. 

# Authentication

> To authorize, use this code:

```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
```

```python
import requests

# get a token:
data = {
	"username": "..",
	"password": "..",
}
response = requests.post("http://api.tngnt.co/userservice/auth/", data)
token = response.json().get("token", None)
```

```shell
# With shell, you can just pass the correct header with each request
curl "api_endpoint_here"
  -H "Authorization: meowmeowmeow"
```

```javascript

$http.authorize("meowmeowmeow");

```


> Make sure to replace `meowmeowmeow` with your API key.

Microservices support the following authentication methods: 

* Token Authentication (implemented)
* OAuth (coming soon)
* JWT (coming soon)

`Authorization: meowmeowmeow`

<aside class="notice">
You must replace <code>meowmeowmeow</code> with your personal API key.
</aside>

